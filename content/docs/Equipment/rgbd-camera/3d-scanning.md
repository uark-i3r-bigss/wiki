---
titile: 3D Scanning
weight: 2
---
Knowledge Base
--------------

*   [3DScanExpert](https://3dscanexpert.com/)
*   [3D Scanning 101](https://www.polyga.com/3d-scanning-101/), The Basics of the Structured-Light 3D Scanning
*   [OpenScan](https://en.openscan.eu/), DIY 3D Scanner
*   [SOLIDWORKS ScanTo3D add-in Tutorial](https://www.youtube.com/playlist?list=PL1TStJR6oVYdLuWf4few4pII-PGe-kkzn)

* * *

**3D Reconstruction** with RGBD camera

*   [Summary of Stereo Mapping Cameras](https://discuss.luxonis.com/d/48-summary-of-stereo-mapping-cameras), by Luxonis
*   Awesome 3D reconstruction list
    *   A curated list of papers & resources linked to 3D reconstruction from image: [https://github.com/openMVG/awesome\_3DReconstruction\_list](https://github.com/openMVG/awesome_3DReconstruction_list)
    *   [In-hand Object Scanning via RGB-D Video Segmentation](https://www.rgbdinhandmanipulation.com/)
*   [VoxelHashing](https://github.com/niessner/VoxelHashing) & [BundleFusion](https://github.com/niessner/BundleFusion), [mLib](https://github.com/niessner/mLib) (Research Library used in the Visual Computing Lab) by [niessner](https://github.com/niessner)

* * *

Next-Best-View for RGBD 3D Reconstruction

*   [ScanRL: Next-Best View Policy for 3D Reconstruction](https://www.youtube.com/watch?v=OXynAHTDTTA&ab_channel=RowelAtienza)
    *   Paper: [https://arxiv.org/abs/2008.12664](https://arxiv.org/abs/2008.12664)
    *   Code: [https://github.com/darylperalta/ScanRL](https://github.com/darylperalta/ScanRL)

* * *

Commercial Full Body 3D Scanner

*   [Make a 3D printed figurine: 3D portraits, 3D selfie figure | Shapify](https://www.shapify.me/)

3D Scanning with iPhone/Smartphones

*   [Openspace](https://www.openspace.ai/resources/videos/openspace-3d-scanning-demo/)
*   [Trnio 3D Scanner](https://www.trnio.com/)

Examples
--------

*   [Lightweight and loosely coupled handheld rgb-d sensor real-time indoor environment reconstruction system](https://github.com/2Pigs1World/RGBD-IndoorSceneReconstruction-ROS)
*   [3D Face Reconstruction from RGBD data, and Deformation Transfer](https://github.com/nurlanov-zh/3d-face-reconstruction)
*   [ampscan](https://ampscan.readthedocs.io/en/latest/index.html), an open-source Python package for analysis and visualisation of digitised surface scan data
    *   [https://github.com/abel-research/ampscan](https://github.com/abel-research/ampscan)
*   [A 3D Scanner using Laser Structured Light, written in Python using OpenCV and NumPy](https://github.com/giulioz/laser-scanning)

Recent Papers
-------------

about RGBD reconstruction

### **RGB-D Reconstruction & RGB-D SLAM**

*   **iDFusion: Globally Consistent Dense 3D Reconstruction from RGB-D and Inertial Measurements** \[[pdf](https://dl.acm.org/doi/abs/10.1145/3343031.3351085)\] _ACM MM 2020_
*   **Multi-Robot Collaborative Dense Scene Reconstruction** \[[pdf](https://dl.acm.org/doi/pdf/10.1145/3306346.3322942)\] _TOG 2019_
*   **BAD SLAM: Bundle Adjusted Direct RGB-D SLAM** \[[pdf](https://openaccess.thecvf.com/content_CVPR_2019/papers/Schops_BAD_SLAM_Bundle_Adjusted_Direct_RGB-D_SLAM_CVPR_2019_paper.pdf)\] \[[project page](https://github.com/2Pigs1World/RGBD-Paper-List/blob/main/www.eth3d.net)\] _CVPR 2019_
*   **Real-time Indoor Scene Reconstruction with RGBD and Inertia Input** \[[pdf](https://arxiv.org/pdf/1812.03015)\] \[[dataset](https://github.com/zhuzunjie17/FastFusion)\] _ICME 2019 Best Student Paper Award_
*   **TextureFusion: High-Quality Texture Acquisition for Real-Time RGB-D Scanning** \[[pdf](https://openaccess.thecvf.com/content_CVPR_2020/papers/Lee_TextureFusion_High-Quality_Texture_Acquisition_for_Real-Time_RGB-D_Scanning_CVPR_2020_paper.pdf)\] \[code\] _CVPR 2020_
*   **Geometry-Aware ICP for Scene Reconstruction from RGB-D Camera** \[[pdf](http://www.sci-hub.ren/10.1007/s11390-019-1928-6)\] _JOURNAL OF COMPUTER SCIENCE AND TECHNOLOGY 2019_
*   **Joint Texture and Geometry Optimization for RGB-D Reconstruction** \[[pdf](https://openaccess.thecvf.com/content_CVPR_2020/papers/Fu_Joint_Texture_and_Geometry_Optimization_for_RGB-D_Reconstruction_CVPR_2020_paper.pdf)\] _CVPR 2020_
*   **Noise-Resilient Reconstruction of Panoramas and 3D Scenes using Robot-Mounted Unsynchronized Commodity RGB-D Cameras** \[[pdf](http://orca.cf.ac.uk/130657/1/DepthPano-TOG2020.pdf)\] _TOG2020_
*   **Real-Time Global Registration for Globally Consistent RGB-D SLAM** \[[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8606275)\] _TOR 2019_
*   **Robust RGB-D SLAM Using Point and Line Features for Low Textured Scene** \[[pdf](https://www.mdpi.com/1424-8220/20/17/4984/pdf)\] \[[code](https://michaelgrupp.github.io/evo/)\] _Sensors 2020_
*   A Vertex-to-Edge Weighted Closed-Form Method for Dense RGB-D Indoor SLAM \[[pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8649628)\] _IEEE ACCESS 2019_

### **3D Semantic Instance Segmentation**

*   **3D-SIS: 3D Semantic Instance Segmentation of RGB-D Scans** \[[pdf](https://openaccess.thecvf.com/content_CVPR_2019/papers/Hou_3D-SIS_3D_Semantic_Instance_Segmentation_of_RGB-D_Scans_CVPR_2019_paper.pdf)\] _CVPR 2019_

### **Learning-based RGB-D Reconstruction**

*   **DeepDeform: Learning Non-rigid RGB-D Reconstruction with Semi-supervised Data** \[[pdf](https://arxiv.org/pdf/1912.04302.pdf)\] \[[data](https://github.com/AljazBozic/DeepDeform)\] _CVPR 2020_
*   **Visual Camera Re-Localization from RGB and RGB-D Images Using DSAC** \[[pdf](https://arxiv.org/pdf/2002.12324.pdf)\] _arXiv 2020_
*   **SPSG: Self-Supervised Photometric Scene Generation from RGB-D Scans** \[[pdf](https://arxiv.org/pdf/2006.14660.pdf)\] _arXiv 2020_
*   **X-Section: Cross-Section Prediction for Enhanced RGB-D Fusion** \[[pdf](https://openaccess.thecvf.com/content_ICCV_2019/papers/Nicastro_X-Section_Cross-Section_Prediction_for_Enhanced_RGB-D_Fusion_ICCV_2019_paper.pdf)\] _ICCV 2019_