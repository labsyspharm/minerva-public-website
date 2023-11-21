---
layout: default
title: What is Minerva
nav_order: 2
has_children: true
---
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
  - TOC
{:toc}
</details>

# What is Minerva?
Minerva is a suite of light-weight software tools that enables interactive viewing and fast sharing of large image data. It comprises <span style="color: #278AB0;">**Minerva Author**</span>, a tool that lets you easily create and annotate images, and <span style="color: #1DC690;">**Minerva Story**</span>, a narrative image viewer for web hosting.

Minerva is built to support the image data sharing for tissue atlases and digital pathology. 

{: .fs-5 }
{: .fw-300 }
Watch this episode of the [**Multiplex Tissue Imaging Technology**](https://www.tissue-atlas.org/curriculum) webinar series to learn more about Minerva!

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/685606030?badge=0&amp;autopause=0&amp;quality_selector=1&amp;progress_bar=1&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Data Visualization and Sharing with MINERVA"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>


# Anatomy of a Minerva Story

![image](../images/annotated_story_ui.png)

{: .fs-3 }
{: .fw-300 }
Click the components below to learn more about the <span style="color: #1DC690;">**Minerva Story**</span> interface.

[Narrated Waypoint](#narrated-waypoint){: .btn .btn-green }  [Curated Field of View](#curated-field-of-view){: .btn .btn-green }  [Channel Tunning](#channel-tuning){: .btn .btn-green }  [Channel Groups](#channel-groups){: .btn .btn-green }

<br>

## Narrated waypoint

<span style="color: #1DC690;">**Minerva Story**</span> displays a narrative guide that you create to help your viewer contextualize and interpret the image data. 

### Introductory content

For your viewers, a <span style="color: #1DC690;">**Minerva Story**</span> starts with the Sample Description you provide when authoring the story. This introductory text gives an overview to your data and its story. You can also use plain language to provide context with essential metadata (e.g. diagnosis, demographic etc.).

<img src="../images/intro-content-ex1.png" width="70%"> 

{: .fs-3 }
{: .fw-300 }
Example of introductory text providing essential metadata. [*Ovarian Cancer with Annotation*](https://www.cycif.org/data/gray-stic-1)

<img src="../images/intro-content-ex2.png" width="70%"> 

{: .fs-3 }
{: .fw-300 }
Example of introductory text. [*Primary Lung Cancer [M-003]*](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3_DATA.html)

### Metadata

Metadata provides crucial context for your audience to understand the image data. You can provide a list of most relevant metadata within your story. 

For tissue imaging, we recommend using the [MITI (Minimum Information about Tissue Imaging)](https://www.miti-consortium.org/) standard to guide your metadata selection.

<img src="../images/metadata.png" width="50%"> 

{: .fs-3 }
{: .fw-300 }
Example of metadata in [Multimodal spatial profiling of colorectal cancer using Orion](https://www.tissue-atlas.org/orion-crc-1) Story.

### Attribution

A <span style="color: #1DC690;">**Minerva Story**</span> is a publication in its own right. The story author list will likely be different from the manuscript or the data its based on. You can define a preferred way for others to cite your story by including anyone who contributed directory to the story as an author. This could include people who helped conceptualize, write or tune the data.

Of course, you will also want to cite the data used in the story, whether is it from a published manuscript or unpublished data.

<div class="basic-grid three-column">

<div markdown="1">
![Story from Published manuscript](../images/citation-ex1.png)

{: .fs-3 }
{: .fw-300 }
Two examples of attribution in Minerva Stories
</div>
<div markdown="1">
![Story from unpublished data](../images/citation-ex2.png)
</div>

</div><!-- end grid -->

[Back to top](#anatomy-of-a-minerva-story){: .btn .btn-green .btn-arrow } 

<br>

## Curated Field of View

Whole slide tissue images contain massive amounts of information. For some audience, a birds-eye perspective of the whole slide can be overwhelming. For each waypoint of the <span style="color: #1DC690;">**Minerva Story**</span>, you have the option of guiding your audience through the image, directing their attention to the salient details of the data. 

### Initial waypoint

The first waypoint of a <span style="color: #1DC690;">**Minerva Story**</span> makes the first impression for your audience. You may choose to display an area of the sample that's both recognizable and meaningful for the narrative of the story.

<div class="basic-grid two-column">

<div markdown="1">
<img src="../images/full-slide-view.png" width="800"> 

{: .fs-3 }
{: .fw-300 }
An example of a birds-eye view of the whole slide

</div>
<div markdown="1">
<img src="../images/curated-first-waypoint.jpg" height="300"> 

{: .fs-3 }
{: .fw-300 }
An example of a curated field of view where cellular-level detail is visible

</div>

</div><!-- end grid -->

[Back to top](#anatomy-of-a-minerva-story){: .btn .btn-green .btn-arrow } 

<br>

## Channel Tuning

When the viewer selects a waypoint, they are first shown a set of markers, called a channel group, selected by the author of the <span style="color: #1DC690;">**Minerva Story**</span> to company that field of view. 

The appropriate range of channel intensities is vital for understanding the image data. Screens can only display 1/256 of the range of intensity values in source images, so Minerva must choose subset of intensities to display. At the beginning of authoring each <span style="color: #1DC690;">**Minerva Story**</span>, <span style="color: #278AB0;">**Minerva Author**</span> will automatically suggest a range of intensities to display for each channel.

<img src="../images/auto-channel-tuning-ex.png" width="50%"> 

{: .fs-3 }
{: .fw-300 }
An example of dynamic range suggested by the built-in algorithm of Minerva

<div class="basic-grid two-column">

<div markdown="1">
<img src="../images/bright-channel-ex.png" width="800"> 

{: .fs-3 }
{: .fw-300 }
For contrast, a dynamic range that would be too bright for the same area of interest

</div>
<div markdown="1">
<img src="../images/dark-channel-ex.png" height="300"> 

{: .fs-3 }
{: .fw-300 }
And an example that shows a range too dark for this area

</div>

</div><!-- end grid -->

### Custimizing channels

The viewer also has the option of curating the markers and the colors they appear in. 

By clicking the ⚙️ icon on the top right of the channel group box, viewer can see a short description of what feature(s) each marker indicates, have the option to turn on/off each marker, customize their colors, and add additional markers available for this image.

<div class="basic-grid two-column">

<div markdown="1">
<img src="../images/channel-group-setting.png">

{: .fs-3 }
{: .fw-300 }
Clicking the ⚙️ icon brings up options to turn on/off channels and customize colors

</div>
<div markdown="1">
<img src="../images/channel-group-setting-expanded.png"> 

{: .fs-3 }
{: .fw-300 }
Clicking the ![plus icon](../images/plus.svg) icon brings up a list of other markers available to display

</div>

</div><!-- end grid -->

[Back to top](#anatomy-of-a-minerva-story){: .btn .btn-green .btn-arrow } 

<br>

## Channel Groups

When the viewer selects a waypoint, they are first shown a set of markers, called a channel group, selected by the author of the <span style="color: #1DC690;">**Minerva Story**</span> to company that field of view. The author will also give each channel group a name to indicate what tissue/cell features are highlighted. For example, "T cells", "Tissue architecture", "Tumor cells" etc. 

The viewer can switch to a different channel group at any time to compare and contrast. Going to a different waypoint resets the channel group to the author-curated ones.

[Back to top](#anatomy-of-a-minerva-story){: .btn .btn-green .btn-arrow } 

<br>

# How does Minerva work?

Minerva follows a client-server model for delivering content. Images in OME-TIFF or SVS format are imported into <span style="color: #278AB0;">**Minerva Author**</span> where a user sets image settings and annotations. <span style="color: #278AB0;">**Minerva Author**</span> then renders image pyramids and a configuration file that is read by <span style="color: #1DC690;">**Minerva Story**</span> to deliver the content to viewers.

![Minerva Author Architecture](https://user-images.githubusercontent.com/9781588/115775721-3af25200-a381-11eb-8473-bdf2371d0f16.png)

{: .fw-300 }
Minerva is available under the MIT License. It can be downloaded on the [Download page](../usage/download.md) or on GitHub at [https://github.com/labsyspharm/minerva-story](https://github.com/labsyspharm/minerva-story).

<br>

# Learn More
**View the [detailed computational methods](./detailed-methods.html) for more information on how Minerva works.**
