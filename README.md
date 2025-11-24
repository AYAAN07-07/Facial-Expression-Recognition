# Real-Time Emotion Detection using Python

This project is a real-time facial emotion recognition application. It uses the computer's webcam to detect faces, analyze facial expressions, and display the dominant emotion (e.g., happy, sad, angry) along with a confidence score directly on the video feed.

## 📝 Description

The script utilizes the **FER (Facial Expression Recognition)** library, which leverages a pre-trained Convolutional Neural Network (CNN) to classify emotions. It relies on **OpenCV** for video capture and image processing.

**Supported Emotions:**
* Angry
* Disgust
* Fear
* Happy
* Sad
* Surprise
* Neutral

## 🚀 Features

* **Real-time Detection:** Processes video frames on the fly.
* **MTCNN Integration:** Uses Multi-task Cascaded Convolutional Networks (MTCNN) for highly accurate face detection.
* **Visual Feedback:** Draws bounding boxes around faces and labels them with the predicted emotion and probability score.
* **Robust Handling:** Handles multiple faces in a single frame.

## 🛠️ Prerequisites

Before running the script, ensure you have Python installed (version 3.6 or higher is recommended).

### Dependencies

You need to install the following Python libraries:
* `opencv-python`
* `fer`
* `tensorflow` (The FER library is built on top of Keras/TensorFlow)

## 📦 Installation

1.  **Clone the repository** (or download the script):
    ```bash
    git clone [https://github.com/your-username/emotion-detection.git](https://github.com/your-username/emotion-detection.git)
    cd emotion-detection
    ```

2.  **Install the required packages:**
    You can install them via pip:
    ```bash
    pip install opencv-python fer tensorflow
    ```

## 💻 Usage

1.  Run the Python script:
    ```bash
    python main.py
    ```
    *(Note: Replace `main.py` with whatever you named your file).*

2.  **Grant Camera Access:** If prompted, allow the terminal/IDE access to your webcam.

3.  **Interact:**
    * Look at the camera.
    * The window "Emotion Detection" will appear.
    * To **exit** the application, press the **`q`** key on your keyboard.

## ⚙️ Configuration

Inside the code, you can toggle the `mtcnn` parameter when initializing the detector:

```python
# High accuracy, slower speed (Recommended for better detection)
detector = FER(mtcnn=True)

# Lower accuracy, faster speed (Use if experiencing lag)
detector = FER(mtcnn=False)# Facial-Expression-Recognition
