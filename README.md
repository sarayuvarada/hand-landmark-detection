hand--landmark-detection
This project utilizes OpenCV and MediaPipe to detect and track hand landmarks in real-time using a webcam. It identifies finger positions and determines which fingers are open or closed.

Features

Real-time hand detection using MediaPipe.

Finger tracking to detect which fingers are open or closed.

FPS (Frames Per Second) display for performance monitoring.

Requirements pip install opencv-python mediapipe Note: This project is compatible with MediaPipe version 0.8.10 and above. Ensure your Python version is 3.7 or later.

File Structure

hand_detection.py: The main script for detecting hands and identifying finger positions.

README.md: This file containing instructions and details about the project.

Code Overview

handDetector Class:

findHands(img, draw=True): Detects hands in the frame and optionally draws landmarks.

findPosition(img, handNo=0): Returns a list of landmark positions for the specified hand.

getFingers(img, handNo=0): Determines which fingers are open or closed.

distance(point1, point2): Calculates the squared distance between two landmarks.

Main Function:

Captures video from the webcam.

Detects hand landmarks in real-time.

Prints the status of each finger (open/closed) to the console.

Displays the FPS on the video feed.

Example Output

Console output of finger status:

[1, 0, 1, 1, 0] # Thumb and pinky closed, other fingers open

FPS displayed on the video feed.

Troubleshooting

Webcam Not Opening:

Ensure your webcam is connected properly.

Check if another application is using the webcam.

Low FPS:

Try reducing the resolution of the video capture for better performance.

Ensure your system meets the necessary hardware requirements.

License

This project is licensed under the MIT License.
