## INTRODUCTION
### Problem Statement
In traditional video conferencing applications, mute individuals face significant communication barriers. They are unable to participate fully in meetings because their primary mode of communication—sign language—is not understood by most participants. This lack of accessibility leads to exclusion and hampers effective collaboration and communication.

### Project Description
Our Video Conferencing Application aims to solve this problem by translating real-time sign language into text. This allows mute individuals to actively participate in meetings and ensures their contributions are understood by all attendees.

### How It Works
Real-Time Video Input: During a video call, the application captures the sign language gestures of the mute participant.
Translation: our models process the video input to recognize and translate sign language into corresponding text.
Text Display: The translated text is displayed in a dedicated chatbox within the video conferencing interface, allowing other participants to read and respond in real-time.


 ## Features:






  - User Authentication: Users can register, log in, and log out.








- Dashboard: Users are welcomed and can create or join meetings.








- Join Room: Users can enter a room ID to join an existing meeting.








- Video Call: Full-featured video conferencing with options to toggle camera and microphone, share screens, and chat.









- Responsive Design: Ensures usability across different devices.








## InstallationPrerequisites:

- Python 3.x



- Django


- Other dependencies listed in requirements.txt



## Usage
### Admin Panel

- Access the admin panel at `http://127.0.0.1:8000/admin/`
### Main Application

- **Dashboard**: 
  - Access the dashboard at `http://127.0.0.1:8000/`


  ### Steps

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Akshay-jk2004/HandToHeart.git
    cd HandToHeart
    ```

2. **Create a virtual environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Apply migrations**:
    ```bash
    python manage.py migrate
    ```

5. **Run the server**:
    ```bash
    python manage.py runserver
    ```


## Model Details
 Hand Gesture Recognition Model
The hand gesture recognition model is a key component of this project. It uses a Convolutional Neural Network (CNN) to classify hand gestures into corresponding letters.

## Model Architecture:

Input Layer: Accepts 28x28 grayscale images of hand gestures.
Convolutional Layers: Multiple layers to extract features from the images.
Pooling Layers: Reduces the spatial dimensions of the extracted features.
Fully Connected Layers: For classification of the gestures into corresponding letters.
Output Layer: Uses a softmax activation function to output probabilities for each letter.
# Training Data:

The model was trained on the Sign Language MNIST dataset, which contains images of hand gestures representing different letters of the alphabet.
### Model File:

The trained model is saved as smnist.h5.
Gesture Detection Process
### Hand Detection:

The system uses MediaPipe to detect hands in real-time from the video feed.
Hand landmarks are identified to track the position and movements of the hands.
### Image Preprocessing:

The detected hand region is converted to grayscale and resized to 28x28 pixels to match the input size expected by the model.
### Prediction:

The preprocessed image is fed into the CNN model.
The model outputs probabilities for each letter, and the top predictions are displayed with their confidence levels.
Code Overview
The script final.py contains the code for real-time hand gesture detection and recognition.

### Dependencies:

TensorFlow: For loading and using the trained model.
OpenCV: For capturing video feed and preprocessing images.
MediaPipe: For hand detection and landmark identification.
Pandas and NumPy: For data manipulation and numerical operations.
### Key Functions:

load_model('smnist.h5'): Loads the trained hand gesture recognition model.
cv2.VideoCapture(0): Captures video feed from the default camera.
hands.process(framergb): Processes the video frames to detect hands.
model.predict(pixeldata): Predicts the letter based on the preprocessed image of the hand gesture.

## Models Training Screenshots

In models training folder


## Labels
The labels for the model's classes are stored in the `labels.txt` file
```
0 Class 1
1 Class 2
```

## Training
The model was trained using a dataset of sign language gestures, labeled according to the `labels.txt` file.
The training process involved augmenting the dataset and using various techniques to improve accuracy and generalization.


### Demo Link
Uploaded in the repository
https://github.com/Akshay-jk2004/HandToHeart/issues/2#issue-2433969752
