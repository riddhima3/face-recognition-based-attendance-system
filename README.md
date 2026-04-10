# Face Recognition Based Attendance System
A real-time attendance tracking system that uses facial recognition to 
automatically mark and record attendance. Eliminates manual attendance
and prevents proxy attendance.

## How It Works

1. Faces are captured and stored using a webcam
2. KNN classifier is trained on stored face data
3. Real-time webcam feed detects and recognises faces
4. Attendance is automatically marked with name and timestamp
5. Records are saved to a CSV file for each day

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| OpenCV | Face detection and webcam feed |
| Scikit-learn (KNN) | Face recognition classifier |
| Haar Cascade | Face detection XML model |
| Streamlit | Attendance dashboard |
| Pandas | CSV attendance records |

## Project Structure
face-recognition-attendance/
│
├── add_faces.ipynb          # Capture and store face data
├── app.ipynb                # Main recognition and attendance app
├── data/
│   ├── faces_data.pkl       # Stored face encodings
│   ├── names.pkl            # Stored names
│   ├── haarcascade_frontalface_default.xml  # Face detector
│   └── background.png       # UI background
├── Attendance/
│   └── Attendance_DD-MM-YYYY.csv   # Daily attendance records
└── README.md

## Setup & Installation

1. Clone the repository
```bash
git clone https://github.com/riddhima3/face-recognition-attendance.git
cd face-recognition-attendance
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Add faces first
- Open and run `add_faces.ipynb`
- Enter the person's name when prompted
- System captures 100 face samples via webcam

4. Run the attendance system
- Open and run `app.ipynb`
- System will start webcam and begin recognising faces
- Attendance is saved automatically to the Attendance folder

## Requirements
opencv-python
scikit-learn
pandas
numpy
streamlit
streamlit-autorefresh

## Features

- Real-time face detection using Haar Cascade
- KNN based face recognition
- Automatic CSV generation per day
- Timestamp recorded for each attendance entry
- Streamlit dashboard to view attendance records

## Author

**Riddhima Saha**
- LinkedIn: [riddhima-saha](https://www.linkedin.com/in/riddhima-saha)
- Email: riddhima.sahaa@gmail.com
