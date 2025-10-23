# U-GO: AI-Based Assessment Tool for Presentation Skills
This is the B.Sc. Thesis project for "U-GO," a multimodal AI tool for assessing and coaching soft skills. The system analyzes a user's presentation from a video recording, providing detailed feedback on their visual and vocal delivery.


This project was developed at the SWARM Robotics Lab  and incubated at the National Incubation Center, Taxila.

[View the Full B.Sc. Thesis (PDF) for detailed research and architecture.](U-GO_Thesis_AI4GA10.pdf)
## Core Features
The AI pipeline is built on two parallel streams:

### 1. Visual Stream 

Analyzes the video frames to understand the presenter's body language and facial expressions.


* **Face Detection:** Uses **MTCNN** to locate the user's face.


* **Emotion Recognition:** Classifies facial expressions into Positive, Negative, and Calm ratios.



* **Pose Estimation:** Uses **BlazePose** to extract 33 body keypoints.



* **Activity Recognition:** A custom-trained **LSTM** model analyzes the sequence of body keypoints to detect positive (e.g., hand gestures) and negative (e.g., arms crossed) body posture.


### 2. Audio Stream 

Analyzes the extracted audio to assess vocal delivery.


* **Speech-to-Text:** Uses the **SpeechRecognition** Library to generate a transcript.


* **Vocal Analytics:** The audio is analyzed to measure:

  * Rate of Speech

  * Filler Words Spoken (e.g., "um," "ah")

  * Pitch Variation

  * Repeated Words

## Final Dashboard
All analytics are compiled into a final score and displayed on a user-friendly dashboard, allowing the user to track their progress over time.


## Tech Stack

* Core AI: Python, LSTM, Scikit-learn


* Computer Vision: OpenCV, BlazePose (via Mediapipe) , MTCNN 


* Speech: SpeechRecognition Library 

## Project Status
This repository contains the full academic B.Sc. thesis detailing the research, architecture, and implementation of the U-GO platform. The production code developed during incubation is proprietary.
