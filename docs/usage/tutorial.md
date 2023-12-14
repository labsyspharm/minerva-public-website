---
layout: default
title: Tutorial
parent: How to Use Minerva
nav_order: 1
---
# Tutorial

This page will walk you through the steps of creating a basic <span style="color: #1DC690;">**Minerva Story**</span>, with curated channel groups and narrated waypoints. 

Before you start, it might be helpful to go over the [**Minerva Glossary**](../overview/glossary.md) to know some of the terms in this tutorial.

## STEP 0 : Requirements

Check to make sure you have the following before you start authoring your story:

1. You will need the path pointing to your **OME-TIFF image**
  - e.g. "C/Documents/Data/image_01.ome.tif"
  - This image can either be on your local computer or a mounted drive

2. [Recommended] The path to a **CSV file with marker names in one column**
  - The header of the column should be `marker_name`. See an example [*marker_name.csv file*](https://gist.githubusercontent.com/thejohnhoffer/f08eac0a9e15ad50eeb21f84276c93e4/raw/marker_names.csv).
  - *Alternatively*, you will need to know the marker names and order to add them manually.

{: .fs-5 }
{: .fw-300 }

No image data yet? No worries!

>This [example dataset](../dataset.md) contains a OME-TIFF and CSV marker file that you can use to follow this tutorial.

---

## STEP 1: Download Minerva Author


[instructions and links to download Minerva Author](../download.md){: .btn .btn-outline .btn-arrow }

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

If you start with `.story.json`, you do not need to provide a CSV file.

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

Minerva uses **Markdown** to format text. This means that you can bold text by adding **\*\*around to your text\*\*** and italicize by adding *\*around your text\**. 

You can also add formating elements like headings, lists and tables with **Markdown**. For more **Markdown** basics, follow the link below.

[Markdown Basics](https://labsyspharm.github.io/jekyll-tutorial/markdown-basics.html){: .btn .btn-outline .btn-arrow }{:target="_blank"}

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

- When your <span style="color: #1DC690;">**Minerva Story**</span> is made public:
    - A colored underline will automatically appear when the marker name in the narrative description matches a marker in the currently active “channel groups” legend.
    - **Optionally**, you can add outgoing links on the marker names in the narrative description that lead to the GeneCard for the corresponding markers.

    > *See how to set up the links on the [Frequently Asked Questions](../FAQ.md#i-see-links-on-cell-type-and-marker-names-in-some-minerva-stories-how-can-i-add-it-to-my-story) page.*
 
<img src="https://user-images.githubusercontent.com/9781588/110496681-bcd53700-80c3-11eb-95b3-3923aeff347f.png" align="middle" style="border: 1px solid black" width="800px" /> 

**Add as many waypoints as you would like. You can change the zoom, pan, and add annotations such as boxes and arrows to the image.**

- Click the arrow icon ![arrow](../images/arrow.svg) on the right of the control pane to create an arrow.
    - Then click anywhere on the image to place an arrow.
    - Click the name of the arrow at the bottom of the control pane to rename or rotate the arrow.
- Click the crosshair icon ![region](../images/region.svg) on the right of the control pane to make a rectangular outline for any region of interest.
    - Then click and drag anywhere on the image to place the outline.

<img src="https://user-images.githubusercontent.com/9781588/110498441-53562800-80c5-11eb-9225-4e5a46808688.png" align="middle" width="800px" /> 

### 4.4 Create optional data visualizations

Adding other ways to visualize data can help you tell a more complete story.

> *If you are not adding other data visualizations, simply skip to the next step.*


[Instructions to add data visualizations](./data-visualizations.md){: .btn .btn-outline .btn-arrow } 

---

## STEP 5: Save and publish

### Save

Periodically while writing your story, you'll want to click the "Save" button to write your story's progress to a file that can later be reopened in Minerva Author to continue writing your story.

Each time you save, Minerva Author will write to a `.story.json` file to store your waypoints and channel groups.

### Publish and make your story public

Once you have completed authoring your story, click the "Publish" button to export a Minerva Story that's ready to publish. You will see the progress bar reach 100% once it is done saving. 

> *A list of expected outputs can be found [here](index.md#output)*

To make your story visible to the public, you will need to host your image pyramids, *index.html* and *story.json* files. 

There are many ways to do this. Here, we recommend using GitHub and GitHub Pages with the following steps.

### 5.1 Fork the example repository

[View the example repository for Minerva Stories here](https://github.com/thejohnhoffer/minerva-story-template/){: .btn .btn-outline .btn-arrow }

This create a copy of this repository under your account. GitHub has excellent documentation on how to fork a repository. You can follow their [instructions here](https://docs.github.com/en/get-started/quickstart/fork-a-repo).

### 5.2 Upload your data and story files

The structure of the example repository mirrors the output you will recieve from <span style="color: #278AB0;">**Minerva Author**</span>.

Using Add a File, upload your folder of image pyramids, *index.html* and *story.json* files to your repository, **replacing** the example files. 

![Add a file](../images/add-file-github.PNG)

### 5.3 Making your story public

*You are nearly there!*

Under **Settings** > **Code and Automations** > **Pages**, you can set the sources of your GitHub Page to *main* and display your site by clicking **Save**.

<img src="../images/github-pages-setup.png" width="600">

Your Minerva Story is ready to be viewed and shared! ✨