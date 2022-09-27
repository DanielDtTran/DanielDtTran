---
title: "Embrylux (Senior Design Project)"
excerpt: "An embryo screening device for in-vitro fertilization."
number: 2
header:
    teaser: /images/portfolio/embrylux/embrylux-teaser-2.png
toc: true
toc_sticky: true

gallery:
  - image_path: /images/portfolio/embrylux/gantt-chart.png
    url: /images/portfolio/embrylux/gantt-chart.png
---


{% include figure image_path="/images/portfolio/embrylux/embrylux-2.png" %}

## Team Website
I designed the team's website where we elaborate upon our solution, 
business model, regulatory strategy, and other aspects of the project.

[You can read more about Embrylux here.](http://www.embrylux.uci.design/)
<br><br>


## Motivation
{% include figure image_path="/images/portfolio/embrylux/ivf-journey.png" %}

**There is a 70% chance of failure for couples trying to start a family by
in-vitro fertilization (IVF).**

The IVF journey is not only time consuming, but also expensive and emotionally 
taxing on couples. During this time, couples experience doubt, false hope, 
and other emotions that are detrimental to their relationship and mental health.

A major contribution to such a high failure rate results from the current 
embryo screening method, which entails taking out the embryo out of the 
incubator, looking at it under the microscope, and then putting it back into 
the incubator. The decision is based only on looking at the morphology or 
physical appearance of the embryo.

**This is a subjective way of selecting embryos and we see an opportunity to 
improve upon current methods.**
<br><br>


## Solution
{% include figure image_path="/images/portfolio/embrylux/solution.png" %}

Our device determines the health of the embryo by monitoring its metabolism.
Specifically, the device will target NADH, an important biomolecule involved in
cellular production of energy.

The embryo's metabolic information can be analyzed by leveraging NADH's
ability to autofluoresce after being illuminated. The device will specifically 
measure the biomolecule's lifetime (time between illumination and autofluoresence), 
a technique known as fluorescence lifetime imaging microscopy (FLIM).

By analyzing FLIM signatures, a reference library of viable embryos can be generated.
Comparison to our reference library will ultimately determine the embryo's health and 
probability of conception when implanted.
<br><br>


## Internal Design of Prototype
{% include figure image_path="/images/portfolio/embrylux/prototype-internal.png" %}
{% include video id="RpJcl8cliTU" provider="youtube" %}
{% include video id="U_AJ2xm2Vkc" provider="youtube" %}
<br>


## How It Works
{% include figure image_path="/images/portfolio/embrylux/how-it-works.png" %}

1. The embryo is illuminated with blue light.
2. NADH within the embryo will autofluoresce and the emitted light is collected.
3. The field-programmable gate array (FPGA) processes data with our algorithm; the FPGA
   is essential as its parallelism provides low latency.
4. A phasor plot is generated (Analogous to a fingerprint).
5. The fingerprint is compared to a reference library.
6. Embryo is determined to be either viable or non-viable.
<br><br>


## Project Progression

<div>
{% include gallery %}
<i>Click on the image to get a closer look.</i>
</div>{: .notice}

One of many Gantt charts I drafted to maintain the project timeline.
<br><br>


## Awards
{% include figure image_path="/images/portfolio/embrylux/awards.png" %}

1<sup>st</sup> place - Life Sciences/Clean Tech
{: .notice--success}

1<sup>st</sup> place - Tech Surge
{: .notice--success}

Embrylux was awarded *$15,000* after competing in the 2016 Business Plan 
Competition at the Paul Merage School of Business at UC Irvine, with over 80+
teams of undergraduate and graduate students competing that year.

We presented a pitch deck of our go-to-market strategy, target market, 
and business model to a judging panel consisting of licensing officers, industry
experts, entrepreneurs in residence, venture capitalists, and angel investors.

[You can read more about Embrylux here.](http://www.embrylux.uci.design/)