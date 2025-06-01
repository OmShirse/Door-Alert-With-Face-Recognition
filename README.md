Smart Door Alert with Face Recognition
Overview
This project is a smart door alert system with face recognition, designed to enhance home security. A camera embedded in the door scans faces, checks them against a database of known individuals, and decides whether to unlock the door for familiar faces or trigger an alert for unknowns. Built with Python and compatible with microcontrollers like Arduino or ESP, it’s a user-friendly solution for secure access control.
Features

Face Detection: Uses a webcam to detect faces in real-time.
Face Recognition: Compares detected faces against a pre-loaded database of known face encodings.
Visual Feedback: Displays a live video feed with labeled rectangles around detected faces, marking them as "Known" or "Unknown."
Hardware Compatibility: Designed to integrate with microcontrollers like Arduino or ESP for lock control.

Requirements

Python 3.x
Libraries:
opencv-python (cv2) for video capture and display
face_recognition for face detection and recognition
pickle for loading pre-saved face encodings


A webcam (USB or built-in)
Pre-trained face encodings saved in encodings.pickle (format: {"encodings": [], "names": []})

Installation

Install dependencies:pip install opencv-python face_recognition


Ensure a webcam is connected and accessible.
Prepare a encodings.pickle file with known face encodings and names.

Usage

Run the script:python face_recognition_door.py


The webcam will start, displaying a live feed with detected faces.
Faces are labeled as "Known" (with a name) or "Unknown" based on the database.
Press q to exit the program.

How It Works

The script loads pre-saved face encodings and names from encodings.pickle.
It captures video from the webcam and resizes frames for faster processing.
Faces are detected and compared against known encodings using the face_recognition library.
Recognized faces are labeled with names; unknowns are flagged for potential alerts.
The system draws rectangles around faces and displays names in the video feed.

Notes

Ensure the encodings.pickle file is in the same directory as the script.
The webcam index (0) may need adjustment based on your system.
For integration with a door lock, additional hardware (e.g., Arduino, ESP) and code modifications are required to send lock/unlock signals based on recognition results.

Future Improvements

Add real-time alerts (e.g., email or SMS) for unknown faces.
Integrate with a physical lock system using GPIO pins on a microcontroller.
Enhance the database to support dynamic updates of known faces.

License
This project is licensed under the MIT License.
