---
title: "Quantifying Heart Rate with Laser Speckle Imaging"
excerpt: "Image processing with MATLAB to quanitfy heart rate from the finger and wrist."
number: 3
header:
    teaser: "/images/portfolio/laser_speckle/teaser.png"
toc: true
toc_sticky: true


gallery_finger_32:
  - image_path: /images/portfolio/laser_speckle/finger-contrast-32.png
    url: /images/portfolio/laser_speckle/finger-contrast-32.png
  - image_path: /images/portfolio/laser_speckle/finger-roi-32.png
    url: /images/portfolio/laser_speckle/finger-roi-32.png

gallery_finger_60:
  - image_path: /images/portfolio/laser_speckle/finger-contrast-60.png
    url: /images/portfolio/laser_speckle/finger-contrast-60.png
  - image_path: /images/portfolio/laser_speckle/finger-roi-60.png
    url: /images/portfolio/laser_speckle/finger-roi-60.png


gallery_finger_daniel:
  - image_path: /images/portfolio/laser_speckle/finger-frequency-nd.png
    url: /images/portfolio/laser_speckle/finger-frequency-nd.png
  - image_path: /images/portfolio/laser_speckle/finger-frequency-nf.png
    url: /images/portfolio/laser_speckle/finger-frequency-nf.png
  - image_path: /images/portfolio/laser_speckle/finger-contrast-nd.png
    url: /images/portfolio/laser_speckle/finger-contrast-nd.png
  - image_path: /images/portfolio/laser_speckle/finger-contrast-nf.png
    url: /images/portfolio/laser_speckle/finger-contrast-nf.png
  - image_path: /images/portfolio/laser_speckle/finger-roi-nd.png
    url: /images/portfolio/laser_speckle/finger-roi-nd.png
  - image_path: /images/portfolio/laser_speckle/finger-roi-nf.png
    url: /images/portfolio/laser_speckle/finger-roi-nf.png

gallery_finger_shin:
  - image_path: /images/portfolio/laser_speckle/finger-frequency-nd-2.png
    url: /images/portfolio/laser_speckle/finger-frequency-nd-2.png
  - image_path: /images/portfolio/laser_speckle/finger-frequency-nf-2.png
    url: /images/portfolio/laser_speckle/finger-frequency-nf-2.png
  - image_path: /images/portfolio/laser_speckle/finger-contrast-nd-2.png
    url: /images/portfolio/laser_speckle/finger-contrast-nd-2.png
  - image_path: /images/portfolio/laser_speckle/finger-contrast-nf-2.png
    url: /images/portfolio/laser_speckle/finger-contrast-nf-2.png
  - image_path: /images/portfolio/laser_speckle/finger-roi-nd-2.png
    url: /images/portfolio/laser_speckle/finger-roi-nd-2.png
  - image_path: /images/portfolio/laser_speckle/finger-roi-nf-2.png
    url: /images/portfolio/laser_speckle/finger-roi-nf-2.png


gallery_wrist:
  - image_path: /images/portfolio/laser_speckle/wrist-frequency-nd.png
    url: /images/portfolio/laser_speckle/wrist-frequency-nd.png
  - image_path: /images/portfolio/laser_speckle/wrist-frequency-nf.png
    url: /images/portfolio/laser_speckle/wrist-frequency-nf.png
  - image_path: /images/portfolio/laser_speckle/wrist-contrast-nd.png
    url: /images/portfolio/laser_speckle/wrist-contrast-nd.png
  - image_path: /images/portfolio/laser_speckle/wrist-contrast-nf.png
    url: /images/portfolio/laser_speckle/wrist-contrast-nf.png


---

{% include figure image_path="/images/portfolio/laser_speckle/splash.png" %}

## Background
I worked with Shinnosuke Fukazawa at the Microvascular Therapeutics and 
Imaging Laboratory. 

Our project consisted of investigating laser speckle
imaging to quantify heart rate from the finger or wrist (think of the
Apple Watch or other smartwatches).
<br>


## Laser Speckle Imaging
The theory behind laser speckle imaging consists of a phenomenon where
speckles are produced when coherent light (lasers) is directed at biological
tissue. Also important is the fact that the movement of blood causes these
speckles to blur.

**Image processing of the blurring of speckles can reveal valuable
physiological information**.

Furthermore, there are several techniques involved with laser speckle imaging 
such as spatial or temporal.

**Our project consisted of employing temporal contrast**.
<br><br>


## The Math: Speckle Contrast
Speckle contrast $K$ can be defined as follows:

$$K=\frac{\sigma}{<I>},$$

where $\sigma$ is the standard deviation of an $n$x$n$ window of pixels and
$\<I\>$ is the average intensity.
<br><br>

*So how does this work in practice?*
<br><br>


## Imaging Processing for Heart Rate
In order to quanitfy heart rate, Shin and I directed a near-infrared laser
at a finger or wrist and collected a video.

{% include figure image_path="/images/portfolio/laser_speckle/processing-roi.png" %}

Once we have a video, then we can being to process the images:

1. The speckle contrast of each pixel is calculated using a 7x7 window.
2. Repeat *Step 1* for all images within the video.
3. Now, we have a series of images composed of speckle contrast.
4. A region of interest (ROI) is chosen for each video, as shown in 
   yellow above.
5. We then calculate the average speckle contrast over time within the ROI.
6. Smoothen the signal by applying an 11-point moving average window to the 
   average speckle contrast.
7. Detrend the data.
8. Normalize the average speckle contrast from -1 to 1.
   Which gives us the result below.
   {% include figure image_path="/images/portfolio/laser_speckle/processing-contrast.png" %}

9. Convert the data to the frequency domain.
   {% include figure image_path="/images/portfolio/laser_speckle/processing-frequency.png" %}

10. Finally, the frequency (Hz) of the peaks in the image above can be converted
    to beats per minute (bpm) to quanity heart rate.
<br>


## Finger Measurements
### Investigating the Effects of FPS
As part of our project, we investigated the effects of the video's frames per
second (fps) on the measured heart rate.
<br><br><br>

**32 FPS**
{: .text-center}
{% include figure image_path="/images/portfolio/laser_speckle/finger-frequency-32.png" %}
{% include gallery id="gallery_finger_32" layout="half" %}
<br>

**60 FPS**
{: .text-center}
{% include figure image_path="/images/portfolio/laser_speckle/finger-frequency-60.png" %}
{% include gallery id="gallery_finger_60" layout="half" %}

In this particular experiment, we observed a stronger signal for the 32 fps 
trial; the peaks within the frequency domain are much more prominent than
the peaks in the 60 fps trial, when compared to the rest of the signal. 

This suggests that the measured heart rate may have been more accurate in the 
32 fps trial.
<br><br>


### Investigating the Effects of a Lens Filter
We likewise investigated the effects of a neutral-density (ND) filter on the
measured heart rate. An ND filter, when applied to the camera, reduces the
intensity of all recorded light.
<br><br><br>

**Daniel's Finger**
{: .text-center}
{% include gallery id="gallery_finger_daniel" layout="half" %}

In an experiment with my finger, both trials resulted in approximately the same
heart rate, but the trial with the ND filter had less noise overall. 

**However, we then proceeded to observe the opposite behavior in an experiment with Shin's finger.**
<br><br><br>

**Shin's Finger**
{: .text-center}
{% include gallery id="gallery_finger_shin" layout="half" %}

In the experiment with Shin's finger, the trial without a filter had less
noise.

*We hypothesized that the difference in observed behavior may have
originated from our choice of ROI in the no filter trial.* 

The ROI chosen is shifted further to the right than the ROI in the 
corresponding trial for my finger.
<br><br>


## Wrist Measurements
We replicated the same experiment for the wrist concerning an ND filter.
{% include gallery id="gallery_wrist" layout="half" %}

*Here, we observed much noisier signals than from the finger.*

This observation may derive from how there is less bloodflow in the wrist than in the finger,
thereby resulting in a noisier signal.