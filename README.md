# Room_measurement_tool

# Overview
This Python script captures an image of a room using your webcam, processes the image to detect corners and edges, and estimates the dimensions of the room based on user-selected reference points. The script leverages OpenCV and NumPy to process images and perform calculations on detected features.

# Features
Captures live image of the room via webcam.
Processes the image to detect edges and corners.
Allows user to define two reference points in the image that are 3 feet apart to calculate measurements.
Estimates distances between detected corners and provides dimensions of the room (length, width, height, or diagonals).
Visualizes the detected features and measurement results.
# Requirements
Python 3.x
OpenCV
NumPy
# Install dependencies:
bash
Copy code
pip install opencv-python numpy
# How It Works
Image Capture: The script opens your webcam and waits for you to press the 'c' key to capture an image.

Image Processing:

The captured image is converted to grayscale and edge detection is applied using the Canny algorithm.
The script detects corners in the processed image, which will be used for measurements.
Reference Point Selection:

You will be asked to select two points on the image that are 3 feet apart.
This information is used to convert pixel distances into real-world feet.
Distance Calculation:

Based on the detected corners and reference points, the script calculates distances between each pair of corners and converts these distances into feet.
Room Measurement Analysis:

The script analyzes the dimensions by considering the longest, second-longest, and third-longest distances detected.
It checks if the angles between the longest dimensions are roughly perpendicular to infer the possible shape of the room.
Results Visualization:

The detected corners are highlighted on the image, and the estimated measurements are printed out.
# How to Use
Run the script:

bash
Copy code
python room_measurement.py
The webcam will open, and you'll be prompted to capture an image by pressing 'c'. Ensure that the image clearly shows multiple corners and features of the room.

Once the image is captured, the script will detect corners and edges.

You'll be asked to click on two points in the image that are 3 feet apart (these could be on walls or known features).

The script will calculate and display the estimated room dimensions. You can view the detected corners in a window.

# Notes
Ensure the image has distinct features (walls, corners) for better corner detection.
The accuracy of measurements depends on the reference points and image quality.
The "Estimated Height" may not be accurate if the ceiling is not visible in the image.
# Troubleshooting
Webcam not opening: Ensure your webcam is properly connected and not used by another application.
Image not processed: If the image fails to load or process, check the image file permissions and format.
Not enough corners detected: Try capturing an image with clearer and more distinct corners.
# Example Output
Room Dimensions:
Estimated Length: 15.00 feet
Estimated Width: 12.50 feet
Estimated Height: 8.50 feet
Largest Diagonal: 17.00 feet
