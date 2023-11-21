---
layout: default
title: Computational Method
nav_order: 20
parent: What is Minerva
---
# Computational Method
{:.no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
  1. TOC
{:toc}
</details>

Minerva is comprised of two applications: <span style="color: #1DC690;">**Minerva Story**</span> and <span style="color: #278AB0;">**Minerva Author**</span>. 

<span style="color: #1DC690;">**Minerva Story**</span> is a lightweight static web application that enables interactive exploration of large multiplexed images in a web browser. <span style="color: #278AB0;">**Minerva Author**</span> is a multi-platform Python application for users to create <span style="color: #1DC690;">**Minerva Stories**</span>.

## Minerva Author
<span style="color: #278AB0;">**Minerva Author**</span> a JavaScript React web application with a Python Flask backend, packaged with PyInstaller as a native application. It transforms a terabyte-scale multiplex OME-TIFF image into a directory of JPEG image tiles. This transformation preserves the image’s full resolution at a reduced bit-depth suitable for human viewing and feasible web hosting. Both RGB images(brightfield, H&E, immunohistochemistry, etc.) and multi-channel fluorescence images (immunofluorescence,  CODEX, CyCIF, etc.) are supported.

<span style="color: #278AB0;">**Minerva Author**</span> selects a subset of intensity values to display for each channel when the story is created. Each image channel is split into many square image tiles of 1024 pixels each. The tiles vary in their resolution, from the full image resolution to a single thumbnail. Each JPEG image tile is loaded by the tiled image viewer only when needed for display in <span style="color: #1DC690;">**Minerva Story**</span>. <span style="color: #278AB0;">**Minerva Author**</span> optionally allows for the creation of “channel groups,” which show specific image channels overlayed in the application. The JPEG image tiles for each channel are stitched and overlaid together in the <span style="color: #1DC690;">**Minerva Story**</span>. Each channel is individually selectable and colorable.

## Minerva Story
<span style="color: #1DC690;">**Minerva Story**</span> is a single-page web application for presenting an image and its narrative to end users. In <span style="color: #1DC690;">**Minerva Story**</span>, each preselected field of view is called a waypoint. Authors of stories can add text discription and metadata in <span style="color: #278AB0;">**Minerva Author**</span> for each waypoint and choose the default channel group to display. When viewer selects a waypoint, <span style="color: #1DC690;">**Minerva Story**</span> sets the viewer’s coordinates to a specific image location/resolution and specific channel group. At any point the user is free to continue panning/zooming the image and toggling/modifying the visible image channels. The visible image intensity values of each channel may be chosen by domain experts or created by the Minerva's built-in Python script. 

Other features of <span style="color: #1DC690;">**Minerva Story**</span> include text and polygonal overlays, overlay of separate image channel in an interactive lens, and image segmentations optionally linked with data visualizations. The image rendering features of the application are also implemented as a script executable from the command line.

<span style="color: #1DC690;">**Minerva Stories**</span> can be hosted through GitHub Pages or any other web host supporting static content such as Amazon S3.

<br>

{: .fw-300 }
Learn more about the software aspects of Minerva in our publication in *Journal of Open Source Software*:

Hoffer J, Rashid R, Muhlich JL, Chen, YA, Russell D, Ruokonen J, Krueger R, Pfister H, Santagata S, Sorger PK. (2020). Minerva: a light-weight, narrative image browser for multiplexed tissue images. Journal of Open Source Software, 5(54), 2579, [https://doi.org/10.21105/joss.02579](https://doi.org/10.21105/joss.02579).