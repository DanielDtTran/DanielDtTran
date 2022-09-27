---
title: "Monte Carlo Simulations for Protein Folding"
excerpt: "Investigating protein folding with Monte Carlo simulations in MATLAB."
number: 4
header:
    teaser: "/images/portfolio/monte_carlo/teaser.png"
toc: true
toc_sticky: true


gallery_initial_structures:
  - image_path: "/images/portfolio/monte_carlo/structure-1.png"
    url: "/images/portfolio/monte_carlo/structure-1.png"
  - image_path: "/images/portfolio/monte_carlo/structure-2.png"
    url: "/images/portfolio/monte_carlo/structure-2.png"
  - image_path: "/images/portfolio/monte_carlo/structure-3.png"
    url: "/images/portfolio/monte_carlo/structure-3.png"


gallery_a1:
  - image_path: "/images/portfolio/monte_carlo/A-11.png"
    url: "/images/portfolio/monte_carlo/A-11.png"
  - image_path: "/images/portfolio/monte_carlo/A-12.png"
    url: "/images/portfolio/monte_carlo/A-12.png"
  - image_path: "/images/portfolio/monte_carlo/A-13.png"
    url: "/images/portfolio/monte_carlo/A-13.png"
  - image_path: "/images/portfolio/monte_carlo/A-14.png"
    url: "/images/portfolio/monte_carlo/A-14.png"
  - image_path: "/images/portfolio/monte_carlo/A-15.png"
    url: "/images/portfolio/monte_carlo/A-15.png"
  - image_path: "/images/portfolio/monte_carlo/A-16.png"
    url: "/images/portfolio/monte_carlo/A-16.png"

gallery_a2:
  - image_path: "/images/portfolio/monte_carlo/A-21.png"
    url: "/images/portfolio/monte_carlo/A-21.png"
  - image_path: "/images/portfolio/monte_carlo/A-22.png"
    url: "/images/portfolio/monte_carlo/A-22.png"
  - image_path: "/images/portfolio/monte_carlo/A-23.png"
    url: "/images/portfolio/monte_carlo/A-23.png"
  - image_path: "/images/portfolio/monte_carlo/A-24.png"
    url: "/images/portfolio/monte_carlo/A-24.png"
  - image_path: "/images/portfolio/monte_carlo/A-25.png"
    url: "/images/portfolio/monte_carlo/A-25.png"
  - image_path: "/images/portfolio/monte_carlo/A-26.png"
    url: "/images/portfolio/monte_carlo/A-26.png"

gallery_a3:
  - image_path: "/images/portfolio/monte_carlo/A-31.png"
    url: "/images/portfolio/monte_carlo/A-31.png"
  - image_path: "/images/portfolio/monte_carlo/A-32.png"
    url: "/images/portfolio/monte_carlo/A-32.png"
  - image_path: "/images/portfolio/monte_carlo/A-33.png"
    url: "/images/portfolio/monte_carlo/A-33.png"
  - image_path: "/images/portfolio/monte_carlo/A-34.png"
    url: "/images/portfolio/monte_carlo/A-34.png"
  - image_path: "/images/portfolio/monte_carlo/A-35.png"
    url: "/images/portfolio/monte_carlo/A-35.png"
  - image_path: "/images/portfolio/monte_carlo/A-36.png"
    url: "/images/portfolio/monte_carlo/A-36.png"


gallery_b:
  - image_path: "/images/portfolio/monte_carlo/B-1.png"
    url: "/images/portfolio/monte_carlo/B-1.png"
  - image_path: "/images/portfolio/monte_carlo/B-2.png"
    url: "/images/portfolio/monte_carlo/B-2.png"
  - image_path: "/images/portfolio/monte_carlo/B-3.png"
    url: "/images/portfolio/monte_carlo/B-3.png"
  - image_path: "/images/portfolio/monte_carlo/structure-1.png"
    url: "/images/portfolio/monte_carlo/structure-1.png"
  - image_path: "/images/portfolio/monte_carlo/structure-2.png"
    url: "/images/portfolio/monte_carlo/structure-2.png"
  - image_path: "/images/portfolio/monte_carlo/structure-3.png"
    url: "/images/portfolio/monte_carlo/structure-3.png"


gallery_d1:
  - image_path: "/images/portfolio/monte_carlo/D-11.png"
    url: "/images/portfolio/monte_carlo/D-11.png"
  - image_path: "/images/portfolio/monte_carlo/D-12.png"
    url: "/images/portfolio/monte_carlo/D-12.png"
  - image_path: "/images/portfolio/monte_carlo/D-13.png"
    url: "/images/portfolio/monte_carlo/D-13.png"

gallery_d2:
  - image_path: "/images/portfolio/monte_carlo/D-21.png"
    url: "/images/portfolio/monte_carlo/D-21.png"
  - image_path: "/images/portfolio/monte_carlo/D-22.png"
    url: "/images/portfolio/monte_carlo/D-22.png"
  - image_path: "/images/portfolio/monte_carlo/D-23.png"
    url: "/images/portfolio/monte_carlo/D-23.png"

gallery_d3:
  - image_path: "/images/portfolio/monte_carlo/D-31.png"
    url: "/images/portfolio/monte_carlo/D-31.png"
  - image_path: "/images/portfolio/monte_carlo/D-32.png"
    url: "/images/portfolio/monte_carlo/D-32.png"
  - image_path: "/images/portfolio/monte_carlo/D-33.png"
    url: "/images/portfolio/monte_carlo/D-33.png"

gallery_d:
  - image_path: "/images/portfolio/monte_carlo/D-L1.png"
    url: "/images/portfolio/monte_carlo/D-L1.png"
  - image_path: "/images/portfolio/monte_carlo/D-L2.png"
    url: "/images/portfolio/monte_carlo/D-L2.png"
  - image_path: "/images/portfolio/monte_carlo/D-L3.png"
    url: "/images/portfolio/monte_carlo/D-L3.png"
  - image_path: "/images/portfolio/monte_carlo/D-R1.png"
    url: "/images/portfolio/monte_carlo/D-R1.png"
  - image_path: "/images/portfolio/monte_carlo/D-R2.png"
    url: "/images/portfolio/monte_carlo/D-R2.png"
  - image_path: "/images/portfolio/monte_carlo/D-R3.png"
    url: "/images/portfolio/monte_carlo/D-R3.png"


---

{% include figure image_path="/images/portfolio/monte_carlo/D-R3.png" %}

## Background
I investigated protein folding with Monte Carlo simulations as part of a
problem set at Stanford University.

All structures and graphs shown on this page were generated by code I had
written in MATLAB.


## The Model
Simple 2D lattice models with hydrophobic or phobic patterning were used
to model protein folding. These models are commonly referred to as 
hydrophobic-polar (HP) models as Lau and Dill studied in 1989.

The potential of the protein structure is defined as:

$$E = -2 \sum_{i<j}^{N} {h_{i,j}} + \sum_{j}^{N} s_{j}$$

1. $E$ is energy in arbitrary units.
2. Interactions between hydrophobic residues are favored:<br>
   $ h_{i,j}=1 $ if residues $i$ and $j$ are in nearest neighbor contact, both hydrophobic, and not immediately connected along the chain.
   Otherwise, $ h_{i,j} = 0 $.
3. Exposure of hydrophobic residues is disfavored:<br>
   $ s_{j}=1 $ is residue $j$ is hydrophobic and in contact with solvent.
   Otherwise, $ s_{j}=0 $.


## Initial Structures
{% include gallery id="gallery_initial_structures" layout="third" %}


## Exploring Sequence Space (Order of Residues)
Metropolis Monte Carlo simulations were ran to explore the sequence space
of each of the three structures. 

In other words, the shape of the structure was kept constant, while the polarity of the residues was perturbed.

The plots below are examples of a simulation run for each structure.
**Black dots represent hydrophobic residues and red dots represent polar residues**.
<br><br>

**Structure 1**
{: .text-center}
{% include figure image_path="/images/portfolio/monte_carlo/A-E1.png" %}
{% include gallery id="gallery_a1" layout="half" %}
<br>

**Structure 2**
{: .text-center}
{% include figure image_path="/images/portfolio/monte_carlo/A-E2.png" %}
{% include gallery id="gallery_a2" layout="half" %}
<br>

**Structure 3**
{: .text-center}
{% include figure image_path="/images/portfolio/monte_carlo/A-E3.png" %}
{% include gallery id="gallery_a3" layout="half" %}


## Searching for the Optimal Sequence
MATLAB code from the previous section was adapted to execute $\alpha$ Monte
Carlo simulations, each with $\beta$ iterations of random residue.

The code was executed with $\alpha=300$ simulations and $\beta=500$ residue
perturbations and the final energy for each simulation result is collected.

The optimal sequence for each structure, i.e. the sequence with the lowest
energy, is shown below.

{% include gallery id="gallery_b" layout="third" %}


## Does the Optimal Sequence Fold Uniquely?
Given the optimal sequences (order of residues) found in the previous section,
**is it possible for there to be a more optimal structure**?


Moveset 1 from "Transition states and folding dynamics of proteins and heteropolymers"
from Chan and Dill, 1994, was implemented. The optimal sequences found in the
previous section were saved and used in the simulations.

The sequences are given a randomized structure and then folding simulations
were ran to see if the structure would fold into a more optimal one.

Examples of some folding simluations are shown below.
<br><br>

**Sequence 1**
{: .text-center}
{% include gallery id="gallery_d1" layout="third" %}

**Sequence 2**
{: .text-center}
{% include gallery id="gallery_d2" layout="third" %}

**Sequence 3**
{: .text-center}
{% include gallery id="gallery_d3" layout="third" %}

The final results are plotted below. New structures found in the folding 
simulations are shown in the top row. The original structure of each sequence
(as found in **Searching for the Optimal Sequence**) is shown in the bottom row.
<br>

{% include gallery id="gallery_d" layout="third" %}

<b>There appears to be a more optimal structure for sequences 1 and 3.
Sequence 2 seems to already folded into the most optimal structure.</b>

