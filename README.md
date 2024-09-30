# Room Measurement Tool

## Overview
This Python script captures an image of a room using your webcam, processes the image to detect corners and edges, and estimates the dimensions of the room based on user-selected reference points. The script uses OpenCV and NumPy to process images and perform calculations on detected features.

## Features
- Captures live image of the room via webcam.
- Processes the image to detect edges and corners.
- Allows user to define two reference points in the image that are 3 feet apart to calculate measurements.
- Estimates distances between detected corners and provides dimensions of the room (length, width, height, or diagonals).
- Visualizes the detected features and measurement results.

## Requirements
* Python 3.x
* OpenCV
* NumPy
  
### Install dependencies:
```bash
pip install opencv-python numpy

## How It Works
1. **Image Capture:** The script opens your webcam and waits for you to press the 'c' key to capture an image.
2. **Image Processing:**
- The captured image is converted to grayscale and edge detection is applied using the Canny algorithm.
- The script detects corners in the processed image, which will be used for measurements.

