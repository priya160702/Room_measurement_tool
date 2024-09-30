# Room Measurement Tool

This Python script captures an image of a room using your webcam, processes the image to detect corners and edges, and estimates the dimensions of the room based on user-selected reference points. The script uses **OpenCV** and **NumPy** for image processing and feature detection.

## Features

- Captures a live image of a room via your webcam.
- Detects edges and corners in the captured image.
- Allows the user to define two reference points that are 3 feet apart for scaling measurements.
- Estimates distances between detected corners and calculates room dimensions (length, width, height, or diagonal).
- Visualizes the detected features and displays the results.

## Requirements

- Python 3.x
- OpenCV
- NumPy

### Install Dependencies

```bash
pip install opencv-python numpy

