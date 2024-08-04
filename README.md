# ROS-AI-week-5-task-1
smart methods internship - Real-Time Face Detection by OpenCV

# Real-Time Face Detection with Flask and OpenCV

This project demonstrates a real-time face detection application using Flask and OpenCV. The application captures video from a webcam, detects faces in real-time, and streams the processed video to a web interface.

## Features

- Real-time face detection using OpenCV's Haar Cascade Classifier.
- Video streaming to a web interface using Flask.
- Simple and clean user interface.

## How It Works

1. **Webcam Capture**: The application uses OpenCV to access the webcam and capture video frames.
2. **Face Detection**: Each frame is processed using OpenCV's Haar Cascade Classifier to detect faces.
3. **Video Streaming**: The processed frames are streamed to a web interface using Flask.
4. **Web Interface**: A simple HTML page displays the video stream, showing detected faces in real-time.

### Detailed Workflow

1. **Initialization**: When the Flask application starts, it initializes the Haar Cascade Classifier for face detection.
2. **Frame Capture**: The application captures frames from the webcam in a loop.
3. **Face Detection**: Each frame is converted to grayscale, and the classifier detects faces in the frame.
4. **Drawing Rectangles**: Rectangles are drawn around the detected faces.
5. **Encoding Frames**: The frames are encoded in JPEG format.
6. **Streaming**: The encoded frames are streamed to the client as multipart data.
7. **Web Interface**: The client-side JavaScript sets the source of an image element to the video feed URL, displaying the stream.

## Prerequisites

Ensure you have met the following requirements:

- Python 3.6+
- `pip` package manager
- Webcam (for capturing video)

## Installation

1. **app.py code**

  - Imports: Imports necessary modules such as cv2 for OpenCV and Flask for creating the web application.
  - Initialize Flask: Creates a Flask application instance.
  - Load Classifier: Loads the Haar cascade classifier for face detection.
  - Generate Frames Function:
    - Opens the webcam.
    - Captures frames in a loop.
    - Converts frames to grayscale.
    - Detects faces in each frame.
    - Draws rectangles around detected faces.
    - Encodes frames as JPEG.
    - Yields frames as a byte stream.
  - Routes:
    - /: Renders the home page.
    - /video_feed: Streams the video feed.
  - Run the Application: Starts the Flask application.

2. **index html code**

  - HTML Structure: Basic HTML5 document structure with <!DOCTYPE html> declaration.
  - Head Section: Contains metadata and a title for the page.
  - Style: Inline CSS for basic styling to center the video on the screen.
  - Body:
    - Contains an img element with the ID video to display the video stream.
    - Includes a script tag to load the JavaScript file.

3. **script.js code**

  - Event Listener: Waits for the DOM content to be fully loaded.
  - Get Image Element: Retrieves the img element by its ID video.
  - Set Source: Sets the src attribute of the img element to /video_feed, which streams the video feed.

## Usage

1. **Run the Flask Application**

    ```sh
    python app.py
    ```

2. **Open your Web Browser**

    Navigate to `http://127.0.0.1:5000` to view the real-time face detection.
   
## Results 
<img width="959" alt="f" src="https://github.com/user-attachments/assets/5ccb0cbd-9f51-49a9-a8bf-ba20b1529823">

