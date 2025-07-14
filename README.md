# 🔍 Real-Time Face Recognition with Email Alert System

This is a real-time face recognition system that detects and recognizes faces from a live video stream using OpenCV and the `face_recognition` library. When an unknown face is detected, it automatically captures the image and sends an email alert with the face attached.

## 🚀 Features

- Real-time face detection using Haar Cascade
- Face recognition using deep face embeddings
- Email alert with captured face image for unknown individuals
- Works with IP camera (DroidCam) or local webcam
- Secure Gmail-based SMTP support for notifications

## 📁 Project Structure

face-recognition-alert-system/
│
├── haarcascades/              # Haar cascade file for face detection
│   └── haarcascade_frontalface_default.xml
│
├── known_faces_images/        # Folder with known face images
│   └── [person1.jpg, person2.png, ...]
│
├── alert_module.py            # Handles email alert functionality
├── dordrim.py                 # Likely main script to run everything
├── encode_faces.py            # Encodes known faces into embeddings
├── face_detection.py          # Face detection and recognition logic
├── README.md                  # Project documentation (this file)
└── .gitignore                 # Ignore unnecessary files (you will create this)

## ⚙️ Installation

1. **Clone the repository:**
   git clone https://github.com/yourusername/face-recognition-alert-system.git
   
Add known faces:

Place clear, front-facing images of known individuals in the known_faces_images/ folder.

The filename (without extension) will be used as the person's name.

Update credentials:

Open face_detection.py and replace the placeholder values for:

sender_email = "your_email@gmail.com"
sender_password = "your_app_password"
receiver_email = "recipient_email@gmail.com"
droidcam_url = "http://your.droidcam.ip:port/video"
📷 Usage
To start the system, run:
python face_detection.py
Press q to quit the video window.

📬 Email Alerts
Uses Gmail SMTP (smtp.gmail.com, port 587)

Sends alerts with a snapshot of the unknown face

Make sure less secure apps or App Password is enabled for your Gmail account

🔒 Security Tips
Do not hardcode passwords in public repos.

Use environment variables or a .env file and load with python-dotenv.

🛠️ Dependencies
opencv-python

face_recognition

numpy

smtplib (built-in)

email (built-in)
