---
title: Projects
nav:
  order: 2
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-flask-vial" %}Projects

{% include section.html %}

## Vertex modelling of morphogenesis
{% capture content %} {% include figure.html image="images/projects/Tyssue_module.png" caption="Sum-up of the different aspect of Tyssue modularity."  %} {% endcapture %}
{% include float.html content=content flip=false %}

Tyssue : a python simulation library for vertex modelling
Tissue remodelling is a complex process, integrating multiple inputs such as gene expression patterns, cell adherent properties and cell mechanics. It can be difficult to manipulate specific aspects genetically or capture morphogenetic events when the process is rapid. Critically, morphogenesis is inherently a mechanical process. Theoretical modelling of tissue formation can help us to understand how tissues acquire their shape and go beyond the limitation of experimental systems.

Motivated by this, we developed Tyssue, a vertex epithelium simulation library developed in Python. It is multiscale, and can include protein properties that lead to tissue shape change. Thanks to its modularity, we can simulate a wide range of processes. Further, the same mesh can be used to model different processes with different physical properties.

I contribute to the development of this library that has been developed by Guillaume Gay from the UAR BioCampus in Montpellier.


{% include section.html %}

## Modelling fold formation in Drosophila melanogaster
{% capture content %} {% include figure.html 
image="images/projects/droso_mesoderm.png" 
caption="Sum-up of modelling mesoderm invagination." width="400px" %} {% 
endcapture %}
{% include float.html content=content flip=false %}

In drosophila imaginal tissues, we found that at the onset of Epithelial-Mesenchymal Transition (EMT), cells generate myosin II-dependent apico-basal forces while constricting their apex and pull down transiently the apical surface of the epithelium, before delaminating. During mesoderm invagination, we found similar apico-basal structure formed in cells which are under tension.

To test the role and the contribution of such forces, we developed a bio-physical vertex model of the embryo apical junction network. This 3D model of the apical surface of cells of mesoderm invagination mimicks the cellular dynamics observed in the embryo. 

Simulation results showed that apical tension alone without apico-basal force only leads to a curved-shaped mesoderm, independently of the strength of apical contractility. Only in the presence of apico-basal tension does the mesoderm invaginate, forming the V-shape observed in vivo.

{% include section.html %}

{% capture content %} {% include figure.html 
image="images/projects/ModelLegFold.png" caption="Sum-up of modelling leg fold formation with mechanical perturbators around." width="400px" %} {% endcapture %}

{% include float.html content=content flip=true %}

Drosophila leg imaginal disc is an other example of fold formation where a subgroup of cells (here, apoptotic cells) help to form the fold. To test the role of apoptotic forces in folding, we elaborated a physical model based on the 2D vertex model. In the absence of the apoptotic dependent forces, the model indicates that the simple disappearance of 30 cells from a continuous ring-like domain is not sufficient to induce cell shape reorganisation and to create an invagination at the tissue level.
 We observed that developing leg folding occurs in a mechanically noisy environment. To test the impact of mechanical perturbations on fold formation, we implemented our previous model of developing leg folding and integrated random mechanical perturbations in close vicinity to the predicted fold domain, mimicking the mechanical noise observed in vivo. Interestingly, we found that mechanical noise appears sufficient to induce fold deviations in the simulations, mimicking the absence of Myosin planar polarity in the tissue. 
We then wondered whether restoring myosin II polarity in a non-polarized tissue could rescue the defects of fold deviation. Although not feasible in vivo, we could address this question using in silico modeling, asking whether fold deviation caused by local mechanical perturbations could be rescued by the introduction of planar polarized junctional myosin II. In order to integrate myosin II planar polarity in the model, we mimicked myosin II planar polarity and the associated tension anisotropy by the attribution of different values of junctional tension depending on junction orientation in our model. Fold robustness was unaffected by the integration of tension polarity in the model in the absence of external perturbations, while interestingly, gradual increase of tissue polarity favors fold straightness and insensitivity to surrounding perturbations. We further quantified fold morphogenetic robustness in our theoretical model for different degrees of polarity. Interestingly, increasing polarity decreases the degree of deviation of the fold and thus decreases the variability in fold directionality, supporting the fact that the planar polarization of tissue tension favors mechanical isolation of fold formation, which ultimately ensures morphogenetic robustness.