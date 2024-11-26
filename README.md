📖 Project Overview
This project focuses on building an environment perception pipeline for autonomous vehicles, leveraging semantic segmentation, object detection, and depth data. The main goal is to enable self-driving cars to navigate safely by estimating drivable space, detecting lane boundaries, and identifying obstacles.

🎯 Objectives
1- Estimate 3D Drivable Space
- Use semantic segmentation outputs to determine drivable areas.
- Compute 3D coordinates (x,y,z) of pixels using depth data and camera calibration matrices.
  
2- Detect and Refine Lane Boundaries
- Identify lane markings using semantic segmentation outputs.
- Filter and merge detected lines to accurately define lane boundaries.
  
3- Calculate Minimum Impact Distance

- Use object detection and semantic segmentation to identify and filter obstacles.
- Calculate the minimum distance of obstacles from the vehicle using depth information.
