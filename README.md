# Vehicle Counting System

## Overview
- A Python-based vehicle counting system that uses OpenCV to detect and count vehicles in video footage. The project leverages computer vision techniques to identify vehicles crossing a designated line in the video and keeps track of the total count.

## Features
- Detects vehicles in each frame of a video file.
Counts vehicles as they cross a specified line in the frame.
- Displays a bounding box and a vehicle counter on each detected vehicle.
- Tracks vehicle centers and removes duplicates for accurate counting.
## Requirements
- Python 3.x
- OpenCV (with contrib modules)
- NumPy

**Install dependencies using:**
```bash
pip install opencv-contrib-python numpy
```
## How It Works
- Background Subtraction: The project uses a background subtractor to detect moving objects (vehicles) from the static background in the video.
Image Processing: The frames are converted to grayscale and blurred to remove noise. Morphological operations are applied to enhance detection.
Vehicle Detection and Counting: Each detected vehicle is tracked as it moves across a designated counting line. A unique center point is identified for each vehicle to ensure accurate counting.
- Counter Display: The total count of vehicles is displayed on the frame and updated in real-time.
Usage
- Place your video file (e.g., video.mp4) in the project directory.

## Run the script with:

```bash
python vehicle.py
```
- The video window will display the vehicle detections, bounding boxes, and the total count.

- Press Enter to exit the program.

## Code Explanation
- center_handle(): Calculates the center point of each detected vehicle.
- Vehicle Counting Logic: A vehicle is counted when it crosses the defined counting line, with an allowable offset to avoid duplicate counting.
- OpenCV Functions: Various OpenCV functions (cv2.dilate, cv2.morphologyEx, etc.) are used for image processing and contour detection.

## Example Output
- The program displays the video with a counter overlay, updating the vehicle count as each vehicle crosses the line.