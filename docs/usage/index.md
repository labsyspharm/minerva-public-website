---
layout: page
title: How to Use Minerva
nav_order: 6
has_children: true
---

# How to use Minerva

If this is your first time using Minerva, head to the [tutorial]({{ site.baseurl }}/usage/tutorial.html) for an example step-by-step guide to create your <span style="color: #1DC690;">**Minerva Story**</span> using <span style="color: #278AB0;">**Minerva Author**</span>.

[//]: # ## Description
[//]: # This should be a brief, 1-2 sentence description
[//]: # **MY SOFTWARE** performs this task. 

## Required Input

To create a <span style="color: #1DC690;">**Minerva Story**</span>, you will need

**An OME-TIFF image**
  - This image can either be on your local computer or a mounted drive

**[Recommended] A CSV file with marker names in one column, if marker names are not in the OME-XML metadata.**
  - The header of the column should be `marker_name`
  - *Alternatively*, you will need to know the marker names and order to add them manually.

## Output

Once you finish authoring and exporting your story, Minerva Author will output the following:

| **File Name**  | **Description** |
| **exhibit.json** | Contains all the configurations for your story. It follows [this schema](https://labsyspharm.github.io/minerva-story/json-schema/exhibit/build/). |
| **index.html** | Describes the web page that loads *exhibit.json* to display as your story. |
| **A folder named *out*** (or the optional output name you entered) | Contains all the fully rendered image pyramids for each channel group and cell stage segmentation. | 


## Minerva Glossary

You may encounter the following terms while using <span style="color: #278AB0;">**Minerva Author**</span>, viewing a <span style="color: #1DC690;">**Minerva Story**</span> or planning your story. Here are their meanings.

| **Waypoint** | A specific location in the tissue image. For example, blood vessel, lymph node margin. The most basic waypoint consists of a user-selected area on the slide and the related text description. |
| **Channel** | Staining for a marker, for example CD3 labeling T cell membranes. |
| **Channel Group** | Several channels bundled together to convey information. For example, CD3, CD4, CD8 and FOXp3 to distinguish T cell subtypes, or CD45, keratin, CD31 and SOX10 to distinguish melanoma surrounding epithelia blood vessels and immune cells. Individual channels within the group cannot be toggled. Viewers can choose what channel group to display. |
| **Mask** | Segmentation masks. Masks can be added to a waypoint, and are only visible on that waypoint. Viewer can toggle each mask individually. |
| **Visualization** | Plots and/or videos that help illustrate the point alongside the image data. Minerva Author can generate scatter plot, matrix plot and bar chart (max one of each type) with input data in the form of .csv files. They will appear underneath the text description on a waypoint. Additionally, user can embed images (.png, .jpeg etc.) and/or videos in the description using Markdown and HTML. |
| **Annotation** | Arrow, ROI rectangles and text labels can be displayed on your image as annotation. |
