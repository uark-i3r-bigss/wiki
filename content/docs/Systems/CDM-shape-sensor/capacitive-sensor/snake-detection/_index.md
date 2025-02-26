---
title: Detection/Evaluation
---

# Snake Detection/Evaluation

## Introduction

<!-- Embed Powerpoint -->
<iframe src="https://livejohnshopkins.sharepoint.com/sites/PPMD/_layouts/15/Doc.aspx?sourcedoc={88d9359f-f48d-4df5-a944-9ba786252005}&amp;action=embedview&amp;wdAr=1.7777777777777777" width="100%" height="450px" frameborder="0">This is an embedded <a target="_blank" href="https://office.com">Microsoft Office</a> presentation, powered by <a target="_blank" href="https://office.com/webapps">Office</a>.</iframe>

## Method

The pipeline is as follows:

{{< mermaid >}}
flowchart LR
    raw_image[Raw Image\n 640 x 480\n RealSense RGB camera]
    raw_image-->Initialization
    raw_image-->Detec_01
    
    subgraph Initialization
    direction TB
    Init_01[Plane Calibration]
    -->
    Init_02[Define\n Planar Coord System]
    -->
    Init_03[Define\n 'pixel to mm' scale]
    end

    Initialization-->output_01[Projection Matrix\n & SE2]
    output_01-->Detec_04
    
    subgraph Detection
        direction TB
        Detec_01[RGB -> HSV]
        -->
        Detec_02[Color Filter, Blue]
        -->
        Detec_03[-> Grayscale -> Binary]
        -->
        Detec_04[Skeleton Detection]
    end
    
    Detec_04-->Plotting
    
    subgraph Plotting
        direction TB
        Plot_01[Skeleton Points]
        -->
        Plot_02[Shape Points\n reconstructed from\n capacitive sensor]
    end

    Plotting-->evaluation[Compute Error]
{{< /mermaid >}}

Click [Here](https://github.com/jhu-bigss/CDM_Capacitive_Shape_Sensing_ROS2/tree/main/snake_detection) to see the source code.