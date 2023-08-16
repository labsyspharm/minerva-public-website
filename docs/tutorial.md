---
layout: default
title: Tutorial
nav_order: 4

---
# Tutorial

This page will walk you through the steps of creating a basic Minerva Story, with curated channel groups and narrated waypoints. 

## STEP 0 (Before you start): Requirements

To create a Minerva Story, you will need

- A OME-TIFF or SVS image.
  - You will need to have this on your local computer or....
  - All OME-TIFF channels must be 16-bit integers, as output by the [mcmicro](https://mcmicro.org/) pipeline, or unsigned 8-bit integers. (how would someone check this?)

- [Recommended] A CSV file with marker names in one column, if marker names are not in the OME-XML metadata.
  - The header of thee column should be `marker_name`
  - *Alternatively*, you will need to know the marker names and order to add them manually.

This [example dataset](./dataset.md) contains a OME-TIFF and CSV marker file that you can use to follow this tutorial.

---

## STEP 1: Download Minerva Author


[instructions and links to download Minerva Author](./usage/download.md){: .btn .btn-outline .btn-arrow }

---

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

---

## STEP 3: Import data

**Select the OME-TIFF file you wish to create a Minerva Story for**

Alternatively, if you have already started authoring a story want to return to it, select the `.story.json` file saved from the previous session.

**Select the CSV file with a list of marker names in the image**

This file must be a .csv with the [same format as the example](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/marker_names.csv).

**Enter an output name (e.g. LUNG-3-PR) for this story.**

This string will be used in the output filenames. Avoid spaces and special characters. Underscores and dashes are ok.

{: .fs-3 }
{: .fw-300 }
> \*If you do not choose an optional output name, your story file will be named `out`.

**Click "Import" and wait for the image to be loaded in your browser**

{: .fs-3 }
{: .fw-300 }
> \*During this time, your image is being converted to smaller image tiles for faster viewing within the story. This step will take longer if your image is larger in file size.

<img src="https://user-images.githubusercontent.com/9781588/110489394-5c42fb80-80bd-11eb-8929-e0c1f4a62bbf.png" align="middle" width="800px" /> 

---

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

- When your Minerva Story is made public:
    - A colored underline will automatically appear when the marker name in the narrative description matches a marker in the currently active “channel groups” legend.
    - A link to the GeneCard will automatically appear when the marker name in the narrative description matches a marker in the “database” (two CSV files with links and aliases for cell types and markers).
 
<img src="https://user-images.githubusercontent.com/9781588/110496681-bcd53700-80c3-11eb-95b3-3923aeff347f.png" align="middle" style="border: 1px solid black" width="800px" /> 

**Add as many waypoints as you would like. You can change the zoom, pan, and add annotations such as boxes and arrows to the image.**

- Click the small white "arrow" icon on the right of the control pane to create an arrow.
    - Then click anywhere on the image to place an arrow.
    - Click the name of the arrow at the bottom of the control pane to rename or rotate the arrow.
- Click the small white "crosshairs" icon on the right of the control pane to make a rectangular outline for any region of interest.
    - Then click and drag anywhere on the image to place the outline.

<img src="https://user-images.githubusercontent.com/9781588/110498441-53562800-80c5-11eb-9225-4e5a46808688.png" align="middle" width="800px" /> 

### 4.4 Create optional data visualizations

Adding other ways to visualize data can help you tell a more complete story.

> *If you are not adding other data visualizations, simply skip to the next step.*


[Instructions to add data visualizations](./usage/data-visualizations.md){: .btn .btn-outline .btn-arrow } 

---

## STEP 5: Save and publish

### Save

Periodically while writing your story, you'll want to click the "Save" button to write your story's progress to a file that can later be reopened in Minerva Author to continue writing your story.

Each time you save, Minerva Author will write to a `.story.json` file to store your waypoints and channel groups.

### Publish

Once you have completed authoring your story, click the "Publish" button to export a Minerva Story that's ready to publish. You will see the progress bar reach 100% once it is done saving. 

Each time you publish, Minerva Author will write an `index.html` page that loads an `exhibit.json` to display as a Minerva Story, as well as a fully rendered image pyramid for each channel group and cell state segmentation. 

Add steps about publishing or link to publishing guide.