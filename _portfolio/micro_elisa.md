---
title: "Micro-ELISA Prototype"
excerpt: "Microfluidic device for reducing reagent costs with the ELISA technique."
header:
    teaser: /images/portfolio/micro_elisa/plate-full_teaser.png
toc: true
toc_sticky: true

gallery_overview:
  - image_path: /images/portfolio/micro_elisa/device-front.jpg
  - image_path: /images/portfolio/micro_elisa/plate-full.jpg
  - image_path: /images/portfolio/micro_elisa/channel-serpentine.PNG
  - image_path: /images/portfolio/micro_elisa/channel-straight.PNG

gallery_device_images:
  - image_path: /images/portfolio/micro_elisa/device-tips.jpg
  - image_path: /images/portfolio/micro_elisa/device-tips-close.jpg
  - image_path: /images/portfolio/micro_elisa/device-tips-blue.jpg
  - image_path: /images/portfolio/micro_elisa/device-tips-yellow.jpg

---

[Read PDF for additional details.](/documents/MicroELISA.pdf)
<br><br>
{% include gallery id="gallery_overview" layout="half" %}

## Device Images
{% include figure image_path="/images/portfolio/micro_elisa/device-front.jpg" %}
{% include gallery id="gallery_device_images" layout="half" %}
<br>


## Motivation
An ELISA (enzyme-linked immunosorbent assay) is a well-established technique to measure
analytes; however, several disadvantages of the technique include reagent costs and tedious pipetting.

In this regard, would it be possible to leverage and adapt the Hughes Laboratory’s microfluidic
devices for use with ELISA? 

Specifically, the use of microfluidics would decrease the amount of
required reagent and, thereby, both the cost and pipetting required.<br><br>


## Benefits
The device poses not only as a reduction in costs and pipetting, but also familiarity with known
technology (microfluidics) but applied in a new application (ELISA). The benefits above stand to
ultimately facilitate the further adoption of ELISA into the workflow of the Hughes Laboratory.<br><br>


## Design Goals
I established the follow design guidelines, each followed by my reasoning:

1. Adapt the design of the Hughes Laboratory’s current microfluidic devices.

   *A familiar design reduces the time required by researchers to learn how to fabricate the new
   device.* <br><br>
  
2. Minimize the costs needed to fabricate one device.

   *The device must optimize the limited budget I had available, a maximum of $200 for any
    additional materials not already found within the Hughes Laboratory.* <br><br>

3. The device must be analogous to a standard 96-well plate used with ELISA.

   *The device must be compatible with the microscopy equipment currently used within the
    Hughes Laboratory; new equipment would increase costs and violate the 2nd guideline.* <br><br>

4. The device must be as translucent as possible to maximize the accuracy of absorbency
measurements.

   *ELISA is a technique that depends on microscopy; therefore, opaque materials would only
    sabotage the purpose of the micro-ELISA device.* <br><br>

5. Minimize the time required to fabricate the device to within 1-2 days.
Faster fabrication facilitates maximizing my allotted time on the project: 3 months.

   *Faster fabrication facilitates maximizing my allotted time on the project: 3 months* <br><br>


## Design Results
1. The device combines the PDMS construction of the lab’s current devices with newly
designed channels and a polystyrene base sheet.

2. Aside from already available lab materials, the device requires polystyrene sheets and
tools to cut the sheets; both are cheap and easily found at arts and crafts stores.

3. The polystyrene sheet is cut to the dimensions of a 96-well plate.

4. The additional polystyrene base sheet and the rest of the device’s construction (PDMS)
is both translucent.

5. The device can be constructed within 2 hours and then prepared overnight. Total
fabrication time is 24 hours.

6. **The straight channels seem to be more effective than the serpentine design.** <br><br>


## Project Progression
{% include figure image_path="/images/portfolio/micro_elisa/project_progression.PNG" %}


## Design of Micro-Well Channels
Several micro-well channels were prototyped within SolidWorks and AutoCad.

The straight channel was chosen as a starting point, a generic baseline. Conversely, I
designed the serpentine channels as an antithesis to see how narrower chambers and an
increase in total surface area affect the baseline’s behavior.<br><br>

1. **Serpentine**
   {% include figure image_path="/images/portfolio/micro_elisa/channel-serpentine.PNG" %}

2. **Straight**
   {% include figure image_path="/images/portfolio/micro_elisa/channel-straight.PNG" %}


## Design of the Half Plate (Half of 96-Well Plate)
The designs for half of the 96-Well Plates were intended to fit within a standard petri dish.

Additionally, I added guiding lines to 3 sides of the design; because each half of the device is
not symmetrical, the orientation of the halves is critical for correct assembly of the complete
device. The absence of guiding lines indicates where the two halves should be joined.<br><br>

1. **Serpentine**
   {% include figure image_path="/images/portfolio/micro_elisa/half-serpentine.png" %}

2. **Straight**
   {% include figure image_path="/images/portfolio/micro_elisa/half-straight.png" %}


## Design of the Full Plate (96-Well Plate)
Plastic molds were created from each of the half plate designs. PDMS can then be poured into
the mold to construct half of the device.

{% include figure image_path="/images/portfolio/micro_elisa/plate-half-2.PNG" %}

By employing two of the half plate designs, the complete top-layer of the device (analogous to a
standard 96-well plate typically used in ELISA) can be constructed.<br><br>

{% include figure image_path="/images/portfolio/micro_elisa/plate-full.jpg" %}

The circles found in the designs above serve as landmarks. Each of them exactly corresponds
to a standard well found on a 96-well plate. Therefore, the landmarks ensure that the
polystyrene base layer can be correctly positioned and fused to the device.
<br><br>


## Fabrication
[Read PDF for full protocol.](/documents/MicroELISA.pdf)
<br><br>


## Antibody Binding Test

**Goal** <br><br> Determine which buffer, that is also readily available within the Hughes Laboratory, is most
effective at binding antibodies to the device. <br><br> Additionally, determine whether the device 
is capable of ELISA as the technique requires the binding of antibodies.
{: .notice}

<div>
<b>Results</b>
{% include figure image_path="/images/portfolio/micro_elisa/binding-graph.PNG" %}
</div>{: .notice--info}

The results suggested that a **bicarbonate buffer yields the greatest binding strength** and
confirmed that use of ELISA is possible.
<br><br>


## Channel Comparison

**Goal** <br><br> Determine which channel design is more effective with the ELISA technique.
{: .notice}

<div>
<b>Results</b>
{% include figure image_path="/images/portfolio/micro_elisa/fitc_dextran-graph.PNG" %}
</div>{: .notice--info}

Micro-wells with the straight channel returned greater absorbency readings, suggesting that the
**straight design is more effective**.
<br><br>