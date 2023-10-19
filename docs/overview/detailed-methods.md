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

<span style="color: #1DC690;">**Minerva Story**</span> is a lightweight static web application that enables interactive exploration of large multiplexed images in a web browser. <span style="color: #278AB0;">**Minerva Author**</span> is a multi-platform Python application for users to create and author <span style="color: #1DC690;">**Minerva Story**</span>.

## Minerva Author
<span style="color: #278AB0;">**Minerva Author**</span> transforms a terabyte-scale multiplex OME-TIFF image into a directory of JPEG images. It is a JavaScript React web application with a Python Flask backend, packaged with PyInstaller as a native application.This transformation preserves the image’s full resolution at a reduced bit-depth suitable for human viewing and feasible web hosting. <span style="color: #278AB0;">**Minerva Author**</span> selects a subset of intensity values for each channel when the story is created. Each image channel is split into many square image tiles of 1024 pixels each. The tiles vary in their resolution, from the full image resolution to a single thumbnail. Each tile is loaded by the tiled image viewer only when needed for display in Minerva Story. Minerva Author optionally allows for the creation of “channel groups,” which show specific image channels overlayed in the application. The JPEG image tiles for each channel are stitched and overlaid together in <span style="color: #1DC690;">**Minerva Story**</span>. Each channel is individually selectable and colorable.

Metadata or text descriptions created in Minerva Author’s graphical interface (or command line interface) can be added to Minerva Story. A sequence of such descriptions define the “waypoints” of a Minerva Story instance. When a waypoint is selected, Minerva Story sets the viewer’s coordinates to a specific image location/resolution and specific channel group . At any point the user is free to continue panning/zooming the image and toggling/modifying the visible image channels. The visible image intensity values of each channel may be chosen by domain experts or created by the Auto-Minerva command-line script. Other features of Minerva include text and polygonal overlays, overlay of separate image channel in an interactive lens, and image segmentations optionally linked with data visualizations. The Minerva Author application depends on a Flask api server (Python) and a React client (JavaScript). The image rendering features of the application are also implemented as a script executable from the command line.