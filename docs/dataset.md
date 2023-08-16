---
layout: default
title: Example data
nav_order: 20
nav_exclude: false
---
This example dataset is a valuable resource for the development of multiplexed image viewing tools like Minerva. Download the files to your local computer and use them as inputs to practice using **Minerva Author**. 

For practice, try to reproduce the two stories created to describe [histologic features](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3.html) and quantitative [single-cell data analysis](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3_DATA.html) in a single lung cancer specimen.

# About the Dataset
As described in [Rashid et al., Scientific Data, 2019](https://www.nature.com/articles/s41597-019-0332-y), the dataset comprises of multiplexed immunofluorescence images and derived single-cell measurements of immune lineage and other markers in formaldehyde-fixed and paraffin-embedded (FFPE) human lung cancer tissue. We used tissue cyclic immunofluorescence (t-CyCIF) to generate fluorescence images which we artifact corrected using the BaSiC tool, stitched and registered using the ASHLAR algorithm, and segmented using ilastik software and MATLAB. We extracted single-cell features from these images using HistoCAT software. This data is also described in [Du, Lin, and Rashid et al., Nature Protocols, 2019](https://www.nature.com/articles/s41596-019-0206-y).


# Image File (20 GB)

- [lung-3-pr_40x.ome.tif](https://www.synapse.org/#!Synapse:syn17778717)

# Channel Names

<!-- https://www.synapse.org/#!Synapse:syn21815856/files/ -->
- [marker_name.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/marker_names.csv)

# Visualization Charts

- [scatterplot.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/scatterplot.csv)
- [matrix.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/matrix.csv)
- [barchart.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/barchart.csv)

# Segmentation Mask

Missing files?