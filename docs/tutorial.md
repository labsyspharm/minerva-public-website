---
layout: default
title: Tutorial
nav_order: 4

---
# Tutorial

## STEP 0 (Before you start): Requirements

To create a Minerva Story, you will need the following

- The file path to your OME-TIFF or SVS image.
  - All OME-TIFF channels must be 16-bit integers, as output by the [mcmicro](https://mcmicro.org/) pipeline, or unsigned 8-bit integers.
  - Here's an [example OME-TIFF](https://www.synapse.org/#!Synapse:syn17778717).
- The file path to a CSV file with marker names, if marker names are not in the OME-XML metadata.
  - Here’s an [example CSV file](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/marker_names.csv) with the correct “marker_names” header.
- **Optionally**, to create data visualization charts:
  - CSV files matching the formats specified for [data visualizations][44].
  - Here are three example CSV files: [scatterplot.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/scatterplot.csv), [matrix.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/matrix.csv), and [barchart.csv](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/barchart.csv).
- **Optionally**, to import cell state segmentation masks:
  - A 32-bit TIFF or OME-TIFF segmentation image.
  - A CSV file matching the format specified for [cell segmentation masks][45].

## STEP 1: Download Minerva Author

When downloading Minerva Author, please be aware of its current technical limitations:

- Minerva Author only saves to the folder where the application is launched.
- You ​should **close the previous Minerva Author tab** before opening a new one.
- Minerva Author has been tested in Chrome and Firefox. It **does not support** Safari or Internet Explorer.
- All `.story.json` files require linked files (`.tif`, `.ome.tif`, `.svs`, and `.csv`) not to be moved or deleted.

### Download links

#### Mac
* Download this zip file for [MacOS 10, 11, or 12](https://github.com/labsyspharm/minerva-author/releases/download/v1.12.0/minerva_author_macos.zip).

#### Windows
* Download this zip file [for Windows](https://github.com/labsyspharm/minerva-author/releases/download/v1.12.0/minerva_author_windows.zip).

### Source code

Alternatively, click [here](https://github.com/labsyspharm/minerva-story/wiki/How-to-run-Minerva-Author%3F-(from-source-code)) for instructions on how to run from source code.

## STEP 2: Run Minerva Author

* Unzip the downloaded file
* Run the executable:
  - On Windows, double-click on the executable file **minerva_author.exe**.
  - On MacOS, right-click and "Open" the executable file **minerva_author**.

This will open a terminal on your computer and begin running the program
<img src="https://user-images.githubusercontent.com/31513137/78614058-83ed6c00-783b-11ea-83da-8c80c519b483.png" align="middle" width="800px" /> 

It will also launch the program in your default browser. If your default browser not Firefox or Chrome, copy the URL from the address bar to Chrome or Firefox.

<img src="https://user-images.githubusercontent.com/9781588/110488689-b0011500-80bc-11eb-8c3d-7b25f97f3b08.png" align="middle" width="800px" />

If the program does not automatically launch, then open a browser and enter `localhost:2020` into the address bar


## STEP 3: Import data

* Select the OME-TIFF file you wish to create a Minerva Story for. 

This is the image you wish to create a Minerva Story for. It must be in OME-TIFF file format. Future releases of Minerva may accommodate other image file standards.

Alternatively, if you have already started authoring a story want to return to it, select the top-level `.story.json` file saved from the previous session.

* Enter the file path to a list of channel names

This file must be a .csv with the [same format as the example](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/marker_names.csv).

* Enter an output name (e.g. LUNG-3-PR) for this story. This string will be used in the output filenames. Avoid spaces and special characters. Underscores and dashes are ok.

* Click "Import" and wait for image pyramid to be generated.

Note: The duration of this step scales with size of OME-TIFF file.

<img src="https://user-images.githubusercontent.com/9781588/110489394-5c42fb80-80bd-11eb-8929-e0c1f4a62bbf.png" align="middle" width="800px" /> 

## STEP 4: Start authoring

### 4.1 Enter sample info

**Begin by giving your sample a title and a description.**

<img src="https://user-images.githubusercontent.com/9781588/110490758-9fea3500-80be-11eb-98dd-332d1c894d8b.png" align="middle" width="800px" /> 

**This information will be displayed in the front page in the Minerva Story, along with a table of contents.**

<img src="https://user-images.githubusercontent.com/31513137/80245108-16617e00-8638-11ea-8145-c34a31358080.png" align="middle" width="800px" /> 
	
### 4.2 Create channel groups

A channel group is a predefined group of image channels and rendering settings (color, contrast, etc.) that will be displayed at each waypoint of the Minerva story and that the users can toggle between.

**Click the "Add Group" button and enter a name for the channel group.**

<img src="https://user-images.githubusercontent.com/9781588/110492383-205d6580-80c0-11eb-8159-2b39cb12f02e.png" align="middle" width="800px" /> 

**Then, select the channels you want to assign to the channel group.**

<img src="https://user-images.githubusercontent.com/9781588/110492550-4be05000-80c0-11eb-981b-15f1e127ab84.png" align="middle" width="800px" /> 

**Next, change the color for each channel.**

<img src="https://user-images.githubusercontent.com/9781588/110493613-c90bc500-80c0-11eb-87b9-2b97f83e59e5.png" align="middle" width="800px" /> 

**Finish by adjusting the channel contrast using the slide bar.**

<img src="https://user-images.githubusercontent.com/9781588/110493617-ca3cf200-80c0-11eb-9229-768c4da8783e.png" align="middle" width="800px" /> 

Create as many channel groups as you would like. You can always come back to this tab to add more.

### 4.3 Create waypoints

Now it's time to add narrative text and annotate the image. Select the "Edit Story" tab.

**Start by selecting the channel group you want displayed at this waypoint.**
<img src="https://user-images.githubusercontent.com/9781588/110497942-e478cf00-80c4-11eb-8dbe-9b3cd8682be6.png" align="middle" width="800px" /> 

**Then enter the title and narrative description for the waypoint.**

- When hosting your Minerva Story:
    - A colored underline will automatically appear when the marker name in the narrative description matches a marker in the currently active “channel groups” legend.
    - A link to the GeneCard will automatically appear when the marker name in the narrative description matches a marker in the “database” (two CSV files with links and aliases for cell types and markers).
 
<img src="https://user-images.githubusercontent.com/9781588/110496681-bcd53700-80c3-11eb-95b3-3923aeff347f.png" align="middle" style="border: 1px solid black" width="800px" /> 

**Add as many waypoints as you would like. You can change the zoom, pan, and add annotations such as boxes and arrows to the image.**

- Click the small white "arrow" icon on the right of the control pane to create an arrow.
    - Then click anywhere on the image to place an arrow.
    - Click the name of the arrow at the bottom of the control pane to rename or rotate the arrow.
- Click the small white "crosshairs" icon on the right of the control pane to make a rectangular overlay.
    - Then click and drag anywhere on the image to place an overlay.

<img src="https://user-images.githubusercontent.com/9781588/110498441-53562800-80c5-11eb-9225-4e5a46808688.png" align="middle" width="800px" /> 

---

### 4.4 Import data visualizations

**Note**: If you have no data visualization charts to add, you may skip to the next step.

<details>
<div markdown="1">
<summary>Expand to see how to add data visualizations</summary>

### Add scatter plots

You should have a CSV file available with the following headings:

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

### Add matrix plots (heatmaps)

You should have a CSV file available where the first heading is `ClustName`:
| ClustName | **  | *** | **** | ***** | ****** |
|-----------|-----|-----|------|-------|--------|
| ...       | ... | ... | ...  | ...   | ...    |
| ...       | ... | ... | ...  | ...   | ...    |
| ...       | ... | ... | ...  | ...   | ...    |

The number of additional headings marked `**`, `***`, ... `******` determines the number of columns in your matrix plot. Typically, the headings should match marker names in your dataset. The number of rows in the CSV file determines the number of rows in your matrix plot. Typically, the names in the `ClustName` column should match clusters of cells in your dataset. The remaining values should be normalized numerical averages of marker intensity for each given cluster. The below example shows the matrix plot UI in Minerva Author and the output in Minerva Story when paired with the [`matrix.csv`](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/matrix.csv) from the [Example Dataset](https://github.com/labsyspharm/minerva-story/wiki/Example-Dataset) page.

| Minerva Author | Minerva Story  |
|-----------|-----|
| ![Matrix](https://user-images.githubusercontent.com/9781588/111826503-21ac4080-88bf-11eb-99f7-f70a21bcadd0.png) | ![Matrix output](https://user-images.githubusercontent.com/9781588/111827106-e3635100-88bf-11eb-88c4-c8f9ef8dd0d0.png) |


### Add bar charts 

You should have a CSV file available with the headings `type` and `frequency`:

| type | frequency |
|------|-----------|
| ...  | ...       |
| ...  | ...       |
| ...  | ...       |

Typically, the names in the `type` column should match clusters of cells in your dataset. The values in the `frequency` column should be numerical cell counts for each given cluster. The below example shows the bar chart UI in Minerva Author and the output in Minerva Story when paired with the [`barchart.csv`](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/barchart.csv) from the [Example Dataset](https://github.com/labsyspharm/minerva-story/wiki/Example-Dataset) page.

| Minerva Author | Minerva Story  |
|-----------|-----|
| ![Barchart](https://user-images.githubusercontent.com/9781588/111828823-3e964300-88c2-11eb-8bcf-7cf42831cfd2.png) | ![Barchart output](https://user-images.githubusercontent.com/9781588/111828824-3fc77000-88c2-11eb-93aa-1a6f41b634cd.png) |


## 4.5 Import cell segmentation masks

**Note**: If you have no cell segmentation masks, you may skip to the next step.

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
</div>
</details>


## STEP 5: Save and publish

### Save

Periodically while writing your story, you'll want to click the "Save" button to write your story's progress to a file that can later be reopened in Minerva Author to continue writing your story.

Each time you save, Minerva Author will write to a `.story.json` file to store your waypoints and channel groups.

### Publish

Once you have created all desired channel groups and completed authoring the waypoints, click the "Publish" button to export a Minerva Story that's ready to serve publicly. You will see the progress bar reach 100% once it is done saving. 

Each time you publish, Minerva Author will write an `index.html` page that loads an `exhibit.json` to display as a Minerva Story, as well as a fully rendered image pyramid for each channel group and cell state segmentation. After you publish, you can manually edit the `exhibit.json` file, which follows [this schema](https://labsyspharm.github.io/minerva-story/json-schema/exhibit/build/).

## STEP 6: Additional Customization

Manual edits to the `exhibit.json` file allow further customization than possible with the UI.

### 6.1 Lensing Configuration

You may wish to display a custom channel in a movable "lens" atop an existing waypoint.

You may add a "Lensing" configuration with the following properties:

- "Group" must match the `Name` of an item in the `Groups` array:
- "Rad" optionally specifies the radius of the lens in screen pixels:

The "Lensing" may be defined for all waypoints with:

```json
{
  "Lensing": {"Group": "Lensing Channel Group", "Rad": 100},
  "Stories": [],
  "Groups": [],
  "Masks": []
}
```

The lensing may also be defined within a waypoint:

```json
  "Stories": [
    {
      "Name": "Example Story",
      "Waypoints": [
        {
          "Lensing": {
            "Group": "Lensing Channel Group",
            "Rad": 100
          },
          "Zoom": 0.5,
          "Pan": [ 0.5, 0.5 ],
          "Name": "Example Waypoint",
          "Group": "Example Channel Group",
          "Description": "In this tissue specimen...",
        },
      ]
    }
  ]
```


{: .fs-3 }
{: .fw-300 }
> \*Remember to ....

