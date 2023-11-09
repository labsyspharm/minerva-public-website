---
layout: default
nav_exclude: false
title: FAQ
nav_order: 7
---
# Frequently Asked Questions:
[//]: # This page can be hidden (nav_exclude: true) if you are not ready to display FAQ on your site.
[//]: # *Detailed answers will help you ward off some emails!*

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
  - TOC
{:toc}
</details>

## What is an OME-TIFF? 
OME-TIFF is a TIFF images file format that contains a OME-XML metadata block. 

For more documentation on the format, check out the [OME webpage](https://www-legacy.openmicroscopy.org/site/products/ome-tiff).

## Is there additional requirements for my OME-TIFF?
  - OME-TIFF image channels must be unsigned 16-bit integers or unsigned 8-bit integers
    >*Images outputed by the [mcmicro](https://mcmicro.org) pipeline are unsigned 16-bit integers.*
  - [Cell segmentation](./usage/data-visualizations.md#cell-segmentation-masks) masks must be unsigned 32-bit integers, loaded from a separate OME-TIFF

## I see links on cell type and marker names in some Minerva Stories, how can I add it to my story?

Minerva has a built-in list of external links associated with commonly-encountered cell types and markers that can automatically be added to your story. The list is defined in [main.js](https://github.com/labsyspharm/minerva-browser/blob/master/main.js#L88).

To enable the links, head to the `index.html` file generated by Minerva Author (an example of it can be found [here](https://github.com/thejohnhoffer/minerva-story-template/blob/main/index.html#L17)), and remove the `cellTypeData: []` and `markerData: []` lines to enable automatically generated links to common cell types and cell markers.

Alternatively, provide your own list in the same file by using this format:

```
markerData: [
{"String":"name 1","Link":"url/1"},
{"String":"name 2","Link":"url/2"}
....
],
cellTypeData: [
{"String":"name 3","Link":"url/3"},
{"String":"name 4","Link":"url/4"}
....
]
```

The linked cell types and marker names will look like the ones in [this story](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3#s=1#w=3#g=0#m=0_3_2_1#a=-100_-100#v=0.5_0.6508_0.5#o=-100_-100_1_1#p=Q).

## Suggest your frequently encountered questions about Minerva!

Is your question not on this list yet? You can suggest your own FAQs by opening an issue on [GitHub Issues](https://github.com/labsyspharm/minerva-public-website/issues) for this website! 