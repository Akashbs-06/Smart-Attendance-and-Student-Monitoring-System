
# Smart Attendance and Student Monitoring System

An AI-powered classroom monitoring system that automates student attendance using face recognition and monitors classroom activities using computer vision.

## 📌 Project Overview

The **Smart Attendance and Student Monitoring System** is designed to simplify classroom attendance management and improve student monitoring. It uses computer vision and deep learning techniques to identify students, detect mobile phone usage, monitor drowsiness, and generate engagement scores.

The system provides a web-based dashboard for teachers and administrators to monitor classroom activity, review attendance records, view alerts, and generate reports.

## ✨ Key Features

* **Automated Attendance:** Detects and recognizes enrolled students using face recognition.
* **Face Detection:** Uses OpenCV YuNet for face detection.
* **Face Recognition:** Uses OpenCV SFace for identifying registered students.
* **Mobile Phone Detection:** Uses YOLOv8 to detect mobile phone usage in the classroom.
* **Drowsiness Detection:** Uses MediaPipe Face Mesh and Eye Aspect Ratio (EAR) to identify potential drowsiness.
* **Real-Time Alerts:** Generates alerts for detected mobile phone usage and drowsiness.
* **Engagement Score:** Calculates student engagement using attendance and classroom monitoring events.
* **Web Dashboard:** Provides an interface for classroom monitoring and reviewing events.
* **Attendance Reports:** Supports attendance analysis and PDF report generation.
* **Database Management:** Uses SQLite for local data storage.
* **Camera Integration:** Supports camera input, including a compatible Android phone webcam application.

## 🛠️ Technologies Used

| Technology               | Purpose                                                                      |
| ------------------------ | ---------------------------------------------------------------------------- |
| Python                   | Main programming language                                                    |
| OpenCV                   | Image processing and computer vision                                         |
| YuNet                    | Face detection                                                               |
| SFace                    | Face recognition                                                             |
| YOLOv8                   | Mobile phone detection                                                       |
| MediaPipe Face Mesh      | Facial landmark detection                                                    |
| NumPy                    | Numerical operations                                                         |
| Flask                    | Backend web server and APIs                                                  |
| Flask-CORS               | Cross-origin communication                                                   |
| SQLite                   | Database management                                                          |
| HTML, CSS and JavaScript | Web interface                                                                |
| Chart.js                 | Charts and analytics                                                         |
| FPDF2                    | PDF report generation                                                        |
| React.js                 | Frontend technology planned or used, depending on the current implementation |

## 🏗️ System Modules

### 1. Face Detection and Recognition

Detects faces from camera frames and compares them with enrolled student data to automate attendance recording.

### 2. Mobile Phone Detection

Uses the YOLOv8 model to identify mobile phones in classroom camera frames and records relevant detection events.

### 3. Drowsiness Detection

Uses MediaPipe Face Mesh to identify facial landmarks and calculate the Eye Aspect Ratio (EAR). The system can flag potential drowsiness based on the implemented detection conditions.

### 4. Engagement Score

Combines attendance information and monitoring events to estimate student engagement.

### 5. Backend and Database

The Flask backend manages application requests and monitoring events. SQLite stores application data locally.

### 6. Dashboard and Reports

Provides a web interface for reviewing attendance, monitoring events, analytics, alerts, and generated reports.

## 📂 Project Structure

```text
Smart-Attendance-and-Student-Monitoring-System/
│
├── final_year_project-main-main-main/
│   ├── backend/
│   │   └── app.py
│   │
│   ├── frontend/
│   │   ├── index.html
│   │   ├── login.html
│   │   └── chart.umd.min.js
│   │
│   ├── main.py
│   ├── camera.py
│   ├── config.py
│   ├── database.py
│   ├── detector.py
│   ├── enroll_student.py
│   ├── check_enrollment.py
│   ├── report_generator.py
│   ├── session_report_mailer.py
│   ├── timetable_helper.py
│   ├── tracker.py
│   ├── voice_alerts.py
│   ├── requirements.txt
│   ├── deploy.prototxt
│   └── haarcascade_frontalface_default.xml
│
└── README.md
```

*Note: This structure highlights the main files currently included in the repository. Additional files may exist in the local project.*

## ⚙️ Prerequisites

Install the following software before running the project:

* Python 3.11 (or the version supported by your installed dependencies)
* Git
* Visual Studio Code or another Python editor
* A webcam or compatible camera source
* Required Python packages listed in `requirements.txt`

Some computer vision features also require compatible model files. These model files are not included in the GitHub repository and must be obtained separately from their official sources or your original project setup.

## 🚀 Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/Akashbs-06/Smart-Attendance-and-Student-Monitoring-System.git
```

### Step 2: Open the Project Folder

```bash
cd Smart-Attendance-and-Student-Monitoring-System/final_year_project-main-main-main
```

### Step 3: Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### Step 4: Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If installation fails, check the Python version and package versions specified by the project dependencies.

### Step 5: Configure Required Model Files

Download or restore the required computer vision model files and place them in the paths expected by the application.

Examples of model files used by this project include:

* YOLOv8 model weights
* YuNet face detection model
* SFace face recognition model
* SSD face detection model, if required by the implementation

Model filenames and paths must match those referenced in the source code.

### Step 6: Configure the Camera

Connect a compatible webcam or configure your Android phone webcam application.

Ensure that the camera source and permissions are correctly configured before running the application.

### Step 7: Start the Application

Run the main application:

```bash
python main.py
```

The exact startup procedure may vary depending on the application's current configuration. If the Flask backend must be started separately, follow the instructions implemented in `backend/app.py`.

## 🖥️ How It Works

1. The camera captures classroom frames.
2. The face detection module identifies faces in the frames.
3. The face recognition module attempts to identify enrolled students.
4. Attendance information is recorded according to the application's configured rules.
5. The YOLOv8 module detects mobile phones.
6. The drowsiness module analyzes facial landmarks and eye movements.
7. Monitoring events are recorded and used to calculate engagement scores.
8. Teachers and administrators can review the available dashboard information and reports.

## 🔒 Privacy and Security

* Student photographs and attendance records should be stored securely.
* Do not commit student photographs, database files, attendance records, or generated reports to a public repository.
* Never upload passwords, SMTP credentials, API keys, or other secrets.
* Configure credentials through environment variables or a local `.env` file that is excluded from Git.
* Obtain appropriate permission before collecting or processing student facial data.
* Follow applicable privacy, institutional, and data protection requirements.

## ⚠️ Limitations

* Face recognition accuracy depends on lighting, camera quality, face orientation, and the enrolled reference images.
* Mobile phone detection depends on the model, image quality, and detection thresholds.
* Drowsiness detection is an estimate and should not be treated as a medical assessment.
* Engagement scores are indicators based on implemented rules and should not be considered definitive measurements of student attention.
* A compatible camera and the required model files must be available for the corresponding features to work.

## 🔮 Future Enhancements

* Develop a more comprehensive React-based monitoring dashboard.
* Add role-based access control for teachers and administrators.
* Improve face recognition under different lighting conditions.
* Add cloud deployment and secure database backup.
* Improve analytics and attendance visualization.
* Add configurable alerts and notification settings.
* Provide automated testing and deployment workflows.

## 👨‍💻 Author

**Akash B S**

Engineering Student | Software Development and Artificial Intelligence

GitHub: [Akashbs-06](https://github.com/Akashbs-06)

## 📄 License

A license has not yet been specified. Add an appropriate open-source license if you intend to permit others to reuse, modify, or distribute this project.
