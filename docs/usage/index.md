---
layout: page
title: How to Use Minerva
nav_order: 6
has_children: true
---

# How to use Minerva

If this is your first time using Minerva, head to the [tutorial]({{ site.baseurl }}/usage/tutorial.html) for an example step-by-step guide to create your <span style="color: #1DC690;">**Minerva Story**</span> using <span style="color: #278AB0;">**Minerva Author**</span>.

[Follow the Tutorial here](./tutorial.md){: .btn .btn-outline .btn-arrow } 

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

