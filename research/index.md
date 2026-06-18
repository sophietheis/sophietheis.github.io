---
title: Research
nav:
  order: 2
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-flask-vial" %}Research

{% include section.html %}
## Mechanical forces in epithelial folding and cell extrusion

We focus on how dying or extruding cells actively shape the tissues around them, rather than being passive bystanders of morphogenesis. In *Drosophila*, we show that cells undergoing epithelial–mesenchymal transition generate an apico-basal force as they begin to delaminate, and that this force is a genuine driver of mesoderm invagination during gastrulation. Extending this idea to vertebrates, we find that apoptotic cells in the avian neural tube generate a comparable apico-basal pulling force before extrusion, and that this cumulative force contributes to the bending of the neural tube. Together, this work establishes apico-basal force generation by dying or transitioning cells as a conserved mechanical strategy in epithelial folding. We also show how the actin-regulating Arp2/3 complex contributes to the directional robustness of fold formation in the *Drosophila* leg, ensuring that mechanical "noise" from neighbouring tissues does not derail morphogenesis.

{% include section.html %}
## Geometry, curvature, and three-dimensional tissue packing

Tissues are not flat, and we are interested in how curvature itself shapes cell behaviour. With collaborators, we develop a theoretical framework explaining how epithelial cells tilt and rearrange their neighbours across the apical-to-basal axis (a transition we term an AB-T1) in response to curvature gradients and pressure differences in curved tissues — a fundamental, previously unresolved question in 3D epithelial packing.

{% include section.html %}
## Open-source computational tools for tissue mechanics
### Simulating tissue mechanics
{% capture content %} {% include figure.html image="images/projects/Tyssue_module.png" caption="Sum-up of the different aspect of Tyssue modularity."  %} {% endcapture %}
{% include float.html content=content flip=false %}
To test mechanical hypotheses quantitatively, we need models as well as data. We create Tyssue, an open-source Python library for vertex-model simulations of epithelia, allowing forces, geometry, and topology to be simulated together in 2D and 3D. Tyssue is now used to model tissue mechanics across multiple labs, and is built to be extensible so that new mechanical behaviours can be added as the underlying biology demands.


### Extracting mechanics and shape from real tissues

Simulating tissues is only half the problem — the other half is measuring them. We develop DISSECT, a tool to segment and analyse cell and tissue mechanics in highly deformed three-dimensional epithelia, and CellMet, a Python package that extracts 3D shape and topology metrics — including cell face properties and cell rearrangements — from dense tissue segmentations. Both tools are designed to be accessible to experimentalists without extensive coding backgrounds, turning raw 3D imaging data into quantitative mechanical readouts, and aim to make rigorous 3D quantification of tissue mechanics a standard part of the developmental biology toolkit.

{% include section.html %}
## Imaging tools for quantitative developmental biology

We also work on benchmarking fluorescent protein performance in the living *Drosophila* embryo, comparing brightness, maturation time, and photostability across a panel of green and red fluorophores under matched genomic and imaging conditions — providing a practical reference for choosing fluorophores in live imaging experiments.
We are interested in extending these computational and imaging tools to a broader range of three-dimensional tissues, and in using them to test how general these mechanical principles are across development.

{% include section.html %}
