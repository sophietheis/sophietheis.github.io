---
title: Publications
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Publications

{% include section.html %}

## Highlighted

{% include citation.html lookup="CellMet: Extracting 3D shape and topology metrics from confluent cells within tissues" style="rich" %}

{% include section.html %}

## Preprint
{% include list.html data="citations" component="citation"
filter="publisher.downcase.include?('biorxiv')" style="rich"%}

{% include section.html %}


## All

{% include list.html data="citations" component="citation" 
filter="!publisher.downcase.include?('biorxiv')" style="rich" %}
