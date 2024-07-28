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
    git clone https://github.com/yourusername/projectname.git
    cd projectname
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
 **Model File**
- Path: models/keras_model.h5
- Format: Keras HDF5
## Labels
The labels for the model's classes are stored in the `labels.txt` file
```
0 Class 1
1 Class 2
```

## Training
The model was trained using a dataset of sign language gestures, labeled according to the `labels.txt` file.
The training process involved augmenting the dataset and using various techniques to improve accuracy and generalization.

