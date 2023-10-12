---
layout: default
nav_exclude: false
title: Data Visualizations
parent: How to Use Minerva
nav_order: 16
---
# Data Visualizations

Sometimes, you may want to include other forms of data visualization alongside your image data to tell a more complete story. 

**Minerva Author supports**

* [Scatter plots](./data-visualizations.md#scatter-plots)
* [Matrix plots (heatmaps)](./data-visualizations.md#matrix-plots-heatmaps)
* [Bar charts](./data-visualizations.md#bar-charts)
* [Cell segmentation masks](./data-visualizations.md#cell-segmentation-masks)

---

## Scatter plots

**You will need...**


> * a CSV file 
>
>   **Example**: [scatterplot.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/scatterplot.csv)

Your CSV file should have the following headings:

| clust_ID | X_position | Y_position | **  | *** |
|----------|------------|------------|-----|-----|
| ...      | ...        | ...        | ... | ... |
| ...      | ...        | ...        | ... | ... |
| ...      | ...        | ...        | ... | ... |

Each row should represent a specific cell, with the `clust_ID` column set to a positive whole number identifying the cluster assigned to each cell. The `X_position` and `Y_position` should give the position of each cell in image pixels. The remaining two columns should contain positive numerical values in each row, as they will form the X and Y position of your scatterplot.

The column headings `**` and `***` should be replaced with the labels for the X axis and Y axis of your scatterplot. For the below example, `**` is `KERATIN` and `***` is `CD45`. Using the Minerva Author UI, it is possible to assign names and colors to each of the four clusters. The below example shows the matrix plot UI in Minerva Author and the output in Minerva Story when paired with the [`scatterplot.csv`](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/scatterplot.csv) from the [Example Dataset](https://github.com/labsyspharm/minerva-story/wiki/Example-Dataset) page.

| Minerva Author | Minerva Story  |
|-----------|-----|
| ![Scatterplot](https://user-images.githubusercontent.com/9781588/111822148-d0e61900-88b9-11eb-9cd1-8c3a19f50c61.png) | ![Scatterplot output](https://user-images.githubusercontent.com/9781588/111824750-faed0a80-88bc-11eb-9ae7-f248db3500f9.png) |

## Matrix plots (heatmaps)


**You will need...**
> * a CSV file 
> 
>   **Example**: [matrix.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/matrix.csv)

Your the first heading of your CSV file should be `ClustName`:

| ClustName | **  | *** | **** | ***** | ****** |
|-----------|-----|-----|------|-------|--------|
| ...       | ... | ... | ...  | ...   | ...    |
| ...       | ... | ... | ...  | ...   | ...    |
| ...       | ... | ... | ...  | ...   | ...    |

The number of additional headings marked `**`, `***`, ... `******` determines the number of columns in your matrix plot. Typically, the headings should match marker names in your dataset. The number of rows in the CSV file determines the number of rows in your matrix plot. Typically, the names in the `ClustName` column should match clusters of cells in your dataset. The remaining values should be normalized numerical averages of marker intensity for each given cluster. The below example shows the matrix plot UI in Minerva Author and the output in Minerva Story when paired with the [`matrix.csv`](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/matrix.csv) from the [Example Dataset](https://github.com/labsyspharm/minerva-story/wiki/Example-Dataset) page.

| Minerva Author | Minerva Story  |
|-----------|-----|
| ![Matrix](https://user-images.githubusercontent.com/9781588/111826503-21ac4080-88bf-11eb-99f7-f70a21bcadd0.png) | ![Matrix output](https://user-images.githubusercontent.com/9781588/111827106-e3635100-88bf-11eb-88c4-c8f9ef8dd0d0.png) |


## Bar charts 


**You will need...**
> * a CSV file 
> 
>   **Example**: [barchart.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/barchart.csv)

Your CSV file should have the headings `type` and `frequency`:

| type | frequency |
|------|-----------|
| ...  | ...       |
| ...  | ...       |
| ...  | ...       |

Typically, the names in the `type` column should match clusters of cells in your dataset. The values in the `frequency` column should be numerical cell counts for each given cluster. The below example shows the bar chart UI in Minerva Author and the output in Minerva Story when paired with the [`barchart.csv`](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/barchart.csv) from the [Example Dataset](https://github.com/labsyspharm/minerva-story/wiki/Example-Dataset) page.

| Minerva Author | Minerva Story  |
|-----------|-----|
| ![Barchart](https://user-images.githubusercontent.com/9781588/111828823-3e964300-88c2-11eb-8bcf-7cf42831cfd2.png) | ![Barchart output](https://user-images.githubusercontent.com/9781588/111828824-3fc77000-88c2-11eb-93aa-1a6f41b634cd.png) |


## Cell segmentation masks


> **You will need...**
> * A 32-bit TIFF or OME-TIFF segmentation image.
> * A CSV file matching the format specified for cell segmentation masks

From the "Edit Groups" tab, you will see the empty mask interface if you have not yet added cell segmentation masks to your story using Minerva Author:

![empty](https://user-images.githubusercontent.com/9781588/112503952-b8ff1100-8d61-11eb-94a2-09fd0ee7097c.png)

Use the first field to select a path to a cell segmentation image in either OME-TIFF or TIFF format. If you select a TIFF file, you will need to wait for Minerva Author to convert that file to an OME-TIFF. Minerva Author will save the OME-TIFF in the same directory as the selected TIFF. After the mask image has loaded, your mask interface should look like this:


![step1](https://user-images.githubusercontent.com/9781588/112503951-b8ff1100-8d61-11eb-97da-52ee16e363ba.png)

At any time, you may use the second field to select a "cell states" CSV file with two columns with `CellID` and `State` as the column headers. Each row should have a positive whole number for the `CellID` column and a text label in the `State` column. Minerva Author uses this file to create a separate cell mask for each unique state.

| CellID | State |
|------|-----------|
| ...  | ...       |
| ...  | ...       |
| ...  | ...       |

After the "cell states" CSV file loads, you can change the color and label for each cell state. Your mask interface should look something like this:

![step2](https://user-images.githubusercontent.com/9781588/112507501-147ece00-8d65-11eb-8654-98cbb674f497.png)

Now, if you open the "Edit Story" tab, each waypoint will have a dropdown menu that allows you to select an arbitrary number of cell states for the waypoint to display. The waypoint dropdown should look something like this:

![step3](https://user-images.githubusercontent.com/9781588/112503949-b8667a80-8d61-11eb-9f73-164d9073e147.png)

Now, any cell segmentation masks that you select for a given waypoint will render on top of the channels in the channel group associated with that waypoint.


---
