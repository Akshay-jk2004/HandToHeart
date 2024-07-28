## INTRODUCTION







our Video Conferencing Application designed to enable non-verbal individuals to participate in meetings. This application translates real-time sign language into text, making communication seamless and inclusive


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
