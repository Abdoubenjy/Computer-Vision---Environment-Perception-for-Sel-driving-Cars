## Environment Perception for Self-Driving Cars

This project demonstrates advanced techniques for environment perception in self-driving cars using data from CARLA, a simulation platform for autonomous driving research. The project focuses on leveraging semantic segmentation and depth data to estimate drivable areas, detect lanes, filter object detections, and determine obstacle distances.

## Key Features

- **Drivable Space Estimation**: Calculate 3D drivable areas using semantic segmentation, depth maps, and camera calibration data.
- **Lane Detection**: Identify and visualize traffic lane markings from segmentation results.
- **Object Detection Filtering**: Use semantic segmentation to eliminate false positives from 2D object detection.
- **Obstacle Distance Calculation**: Estimate the distance to obstacles based on filtered object detection results and depth data.

## Dataset

The project uses simulated data from CARLA. Each data frame contains:

- **RGB Image**: A camera-captured RGB image of the scene.
- **Depth Map**: A per-pixel distance measurement in meters.
- **Semantic Segmentation Map**: Pixel-wise classifications into categories (e.g., roads, vehicles, pedestrians).
- **Object Detection Output**: A numpy array of bounding boxes and class predictions.
- 
Sample frame indices: 0, 1, and 2. Frame 0 is the primary example; frames 1 and 2 are for testing and validation.

## Installation

- **Clone the repository**:

git clone https://github.com/Abdoubenjy/Computer-Vision---Environment-Perception-for-Sel-driving-Cars.git
cd Computer-Vision---Environment-Perception-for-Sel-driving-Cars


## Project Workflow

- Step 1: Data Loading and Visualization
  
Load and visualize RGB, depth, and segmentation maps.
Map segmentation indices to visualization colors (e.g., blue for roads, green for vehicles).

- Step 2: Drivable Space Estimation
  
Use depth maps and camera calibration data to compute 3D coordinates of each pixel.
Filter pixels corresponding to the "road" category (index 7) from semantic segmentation.
Fit a ground plane to the filtered points using the RANSAC algorithm.

- Step 3: Lane Detection
  
Detect lane markings by extracting pixels classified as "lane markings" (index 6).

Step 4: Object Detection Filtering

Use semantic segmentation to eliminate detected objects outside drivable areas.

Step 5: Obstacle Distance Estimation

Combine filtered object detections with depth data to calculate obstacle distances.

## Technologies and Tools

**Programming Language**: Python 3
**Simulation**: CARLA
**Machine Learning**: Semantic segmentation neural networks
**Algorithms**: RANSAC for ground plane fitting
**Visualization**: Matplotlib, OpenCV

## Example Results

**Drivable Space**:

3D visualization of the drivable area based on depth and segmentation data.

**Lane Detection**:

Accurate lane marking extraction and visualization on the road.

**Object Detection Filtering**:

Removal of false-positive object detections outside drivable areas.

**Obstacle Distance Estimation**:

Precise distance calculation to detected vehicles and pedestrians.
