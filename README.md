# Finger Count Detection using Mediapipe and OpenCV

This project detects and counts the number of fingers visible in a video feed using the Mediapipe library for hand landmark detection and OpenCV for video processing.

## Features
- Detects hand landmarks using Mediapipe.
- Counts the number of fingers visible on both hands.
- Displays the video feed with the hand landmarks drawn.
- Saves the processed video to an output file.

## Requirements

To run this project, you need to have the following libraries installed:

- Python 3.12.7
- OpenCV
- Mediapipe
- Numpy
- Math

### Install Requirements

You can install the required libraries using the following command:

### bash
pip install opencv-python mediapipe

### Usage
To run the project and start the video feed, simply execute the Python script:
python fingerCount.py

### Code Overview
The main script uses OpenCV to capture video from the webcam and Mediapipe to detect hand landmarks. Here's a breakdown of the main components:

- Holistic Model: We use Mediapipe's holistic model to detect hand landmarks.
- Finger Counting: The function count_valid_fingers calculates how many fingers are raised based on the distance between landmarks.

### Finger Counting Logic
The code checks if a finger is raised by calculating the distance between the wrist and the fingertip landmarks. If the distance exceeds a certain threshold, the finger is considered raised. The thumb is treated separately due to its unique position.

### Future Improvements
Some ideas for future improvements:
- Add more gesture recognition (e.g., fist, peace sign).
- Support for multi-hand interaction.
- Real-time feedback for gesture-based control systems.

### License
This project is open source and available under the MIT License.
