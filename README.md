# Attendance System Using Face Recognition

A Python-based **Face Recognition Attendance System** that automatically detects and recognizes faces through a webcam and records attendance with the person's name, time, and date.

The system uses **OpenCV** for real-time camera processing and the **face_recognition** library for face detection and recognition.

## Features

- Real-time face detection using webcam
- Face recognition using pre-stored images
- Automatically marks attendance for recognized persons
- Records Name, Time, and Date
- Prevents duplicate attendance entries
- Displays the recognized person's name on the camera screen
- Shows a warning message when a face is not recognized
- Stores attendance records in a CSV file
- Simple and easy-to-use attendance system

## Technologies Used

- Python
- OpenCV
- NumPy
- face_recognition
- Tkinter
- CSV
- DateTime

## Project Structure

```text
Attendance-System/
│
├── images/
│   ├── person1.jpg
│   ├── person2.jpg
│   └── ...
│
├── Attendence.py
├── Attendnce.csv
├── main.py
└── README.md
```

## How It Works

1. Images of known persons are stored inside the `images` folder.
2. The system reads the images and generates face encodings.
3. The webcam starts and captures video in real time.
4. Faces detected through the webcam are compared with the stored face encodings.
5. If a matching face is found, the person's name is displayed on the camera screen.
6. The person's attendance is automatically recorded in `Attendnce.csv`.
7. The attendance record contains:
   - Name
   - Time
   - Date
8. If the person's attendance has already been recorded, another entry is not added.
9. If the detected face is not recognized, the system displays a `Not Found` warning.

## Attendance Format

Attendance is stored in `Attendnce.csv` in the following format:

```text
Name,Time,Date
YOGESH,10:30:15,20:03:24
```

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Yog5777/Attendance-System.git
```

### 2. Open the Project Directory

```bash
cd Attendance-System
```

### 3. Install Required Libraries

```bash
pip install opencv-python
pip install numpy
pip install face-recognition
```

> Note: The `face-recognition` library depends on `dlib`. Depending on your Python version and operating system, additional setup may be required to install `dlib`.

## Add Known Faces

Create an `images` folder in the project directory if it is not already available.

Add clear images of the people whose attendance you want to recognize.

The image filename is used as the person's name.

Example:

```text
images/
├── Yogesh.jpg
├── Rahul.jpg
└── Amit.jpg
```

For example, if the image filename is `Yogesh.jpg`, the system will recognize the person as `YOGESH`.

## Run the Project

Run:

```bash
python Attendence.py
```

The webcam will open and start detecting faces.

When a registered face is recognized, the system displays the person's name and records the attendance automatically.

## Attendance File

Attendance records are saved in:

```text
Attendnce.csv
```

Example:

```csv
Name,Time,Date
YOGESH,22:44:23,20:03:24
```

## Applications

This project can be used as a basic attendance solution for:

- Schools
- Colleges
- Classrooms
- Offices
- Training institutes
- Small organizations

## Future Improvements

The project can be further improved by adding:

- Student registration interface
- Admin login
- Database integration
- Attendance dashboard
- Daily attendance reports
- Export to Excel/PDF
- Improved unknown-face handling
- Multiple face registration
- Email notifications
- Web-based attendance management

## Author

**Yogesh Chandak**

GitHub: `Yog5777`

## Disclaimer

This project was developed for educational and academic purposes as a Face Recognition Attendance System.
