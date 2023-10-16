---
layout: default
title: Example data
nav_order: 20
nav_exclude: false
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
  - TOC
{:toc}
</details>

These two dataset can both be used to follow the tutorial and practice using <span style="color: #278AB0;">**Minerva Author**</span>. 

**Click the images below to download the files to your local computer to use them.**

<div class="basic-grid mt-6">

{% assign imageUrl = site.baseurl | append: "/images/mcmicro-exemplar-001.jpg" %}
{% include image-card.html 
    image=imageUrl
    link="https://mcmicro.s3.amazonaws.com/exemplars/exemplar-001.zip"
    label="Examplar 1 - Small lung adenocarcinoma, 240 MB (320 MB unzipped)"
%}

{% assign imageUrl = site.baseurl | append: "/images/examplar-data-002.PNG" %}
{% include image-card.html 
    image=imageUrl
    link="https://www.synapse.org/#!Synapse:syn17778717"
    label="Examplar 2 - Human lung cancer, 20 GB"
%}

</div><!-- end grid -->

## About the Datasets

### Examplar 1 - Multiplex immunofluorescnet images of small lung adenocarcinoma

Examplar 1 contains Cyclic Immunofluorescence (CyCIF) images of small lung adenocarcinoma specimens from larger tissue microarray (TMA).

#### File structure for Examplar 1

Downloading Examplar 1 will give you the following files. Below is a few words on what they are and how you can use them to practice using <span style="color: #278AB0;">**Minerva Author**</span>.

| **File/folder name** | **Content** |
| raw | This folder contains 3 *.ome* images that you can use as input for <span style="color: #278AB0;">**Minerva Author**</span>. |
| illumination | This folder contains *.tif* images that represents illumination correction for the image in raw. You **do not** need these for your <span style="color: #1DC690;">**Minerva Story**</span>. |
| markers.csv | This is *.csv* file contains the channel names. You can use it as input for input for <span style="color: #278AB0;">**Minerva Author**</span>. |

### Eaxmplar 2 - Multiplex immunofluorescent images of human lung cancer

Examplar 2 played an instrumental role in the development process of Minerva. Before using Examplar 2, keep in mind that the image file is 20GB in size.

This dataset is described in [Rashid et al., Scientific Data, 2019](https://www.nature.com/articles/s41597-019-0332-y). It comprises of multiplexed immunofluorescence images and derived single-cell measurements of immune lineage and other markers in formaldehyde-fixed and paraffin-embedded (FFPE) human lung cancer tissue. We used tissue cyclic immunofluorescence (t-CyCIF) to generate fluorescence images which we artifact corrected using the BaSiC tool, stitched and registered using the ASHLAR algorithm, and segmented using ilastik software and MATLAB. We extracted single-cell features from these images using HistoCAT software. This data is also described in [Du, Lin, and Rashid et al., Nature Protocols, 2019](https://www.nature.com/articles/s41596-019-0206-y).

For practice, you can use this dataset to try to reproduce the two stories created to describe [histologic features](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3.html) and quantitative [single-cell data analysis](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3_DATA.html) in a single lung cancer specimen.

#### Image File (20 GB)

- [lung-3-pr_40x.ome.tif](https://www.synapse.org/#!Synapse:syn17778717)

#### Channel Names

<!-- https://www.synapse.org/#!Synapse:syn21815856/files/ -->
- [marker_name.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/marker_names.csv)

#### Visualization Charts

- [scatterplot.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/scatterplot.csv)
- [matrix.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/matrix.csv)
- [barchart.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/barchart.csv)


