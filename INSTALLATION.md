# 🚀 ClassSentinel AI — Installation & Deployment Guide

> **From source code to an AI-powered classroom monitoring system.**

Welcome to the setup guide for **ClassSentinel AI**, a Smart Attendance and Student Monitoring System built around computer vision, facial analysis, and intelligent event monitoring.

This guide helps developers prepare the environment, configure the required AI models, connect a camera, and launch the application.

---

## 🧭 Installation Roadmap

Follow this sequence to set up the project:

| Phase | Task                           | Outcome                        |
| ----- | ------------------------------ | ------------------------------ |
| 01    | Prepare the environment        | Python and Git ready           |
| 02    | Get the source code            | Project available locally      |
| 03    | Create an isolated environment | Dependencies separated         |
| 04    | Install packages               | Python dependencies installed  |
| 05    | Prepare AI models              | Required model files available |
| 06    | Configure the camera           | Camera source ready            |
| 07    | Initialize application data    | Database accessible            |
| 08    | Launch and verify              | Supported features tested      |

---

## 01 · Prepare Your Environment

### System requirements

| Component        | Requirement                                      |
| ---------------- | ------------------------------------------------ |
| Operating system | Windows 10/11 or compatible OS                   |
| Python           | Python 3.11, subject to dependency compatibility |
| Version control  | Git                                              |
| Code editor      | Visual Studio Code or equivalent                 |
| Camera           | Compatible webcam or configured phone webcam     |
| Network          | Internet access for dependency installation      |

**Before proceeding:** Ensure that Python and Git are available from your terminal.

```bash
python --version
git --version
```

If either command fails, install the corresponding software and configure your system PATH.

---

## 02 · Get the Source Code

Clone the repository:

```bash
git clone https://github.com/Akashbs-06/Smart-Attendance-and-Student-Monitoring-System.git
```

Enter the application directory:

```bash
cd Smart-Attendance-and-Student-Monitoring-System/final_year_project-main-main-main
```

You should now be inside the directory containing the main Python scripts and `requirements.txt`.

---

## 03 · Create an Isolated Python Environment

Using a virtual environment prevents project dependencies from interfering with other Python applications.

Create the environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

If you use Command Prompt instead of PowerShell:

```cmd
.venv\Scripts\activate.bat
```

After activation, verify the Python interpreter:

```bash
python --version
```

The terminal should show the virtual environment as active.

---

## 04 · Install the Dependencies

Update pip:

```bash
python -m pip install --upgrade pip
```

Install the project's declared dependencies:

```bash
python -m pip install -r requirements.txt
```

### Dependency troubleshooting

If installation fails:

1. Read the first meaningful error message.
2. Confirm that the active Python version is compatible with the affected package.
3. Check whether the package requires a particular version of NumPy or another dependency.
4. Review the versions specified in `requirements.txt`.
5. Retry only after resolving the underlying compatibility issue.

Avoid installing random package versions to bypass errors, because this can introduce new dependency conflicts.

---

## 05 · Prepare the AI Model Assets

ClassSentinel AI uses computer vision models for its supported recognition and monitoring features.

Depending on the current implementation, the required model assets may include:

| Model            | Intended purpose                                     |
| ---------------- | ---------------------------------------------------- |
| YOLOv8 weights   | Mobile phone detection                               |
| YuNet model      | Face detection                                       |
| SFace model      | Face recognition                                     |
| SSD model assets | Additional face detection, if referenced by the code |

### Model setup checklist

* Obtain the required files from trusted sources or your original project environment.
* Confirm that the files match the names expected by the source code.
* Place them at the configured paths.
* Check that the application can read the files.
* Confirm that model initialization succeeds at runtime.

**Important:** Model weights and certain binary model files are excluded from the repository. A successful Git clone therefore does not guarantee that every AI feature is immediately ready to run.

Do not download model files from unknown websites or load untrusted serialized model files.

---

## 06 · Connect the Camera

The application requires a compatible camera source for live monitoring.

Possible configurations include:

* A USB webcam
* A built-in laptop camera
* A compatible Android phone webcam application

### Camera readiness checklist

* [ ] Camera connected and powered.
* [ ] Required camera permissions enabled.
* [ ] Camera available to the operating system.
* [ ] Correct camera index or source configured.
* [ ] No other application exclusively using the camera.

If the application cannot open the camera, check the configured source and the camera initialization logic in the project.

For phone-based webcam setups, ensure the phone and computer are connected according to the webcam application's requirements.

---

## 07 · Prepare the Database

The project uses SQLite for local database storage.

SQLite generally requires no separate database server when accessed through Python's built-in `sqlite3` module.

Before launching the application:

1. Inspect the database configuration.
2. Confirm the configured database path.
3. Ensure the application has permission to create or access the database.
4. Use test data while validating the installation.
5. Verify that attendance and event records are written as expected.

**Privacy reminder:** Do not use or publish real student information during initial testing unless appropriate authorization and safeguards are in place.

---

## 08 · Launch the Application

From the application directory, start the main application:

```bash
python main.py
```

If the backend is designed to run separately, inspect `backend/app.py` and follow the startup procedure implemented in the code.

For a backend that supports direct execution, the command may be:

```bash
python backend/app.py
```

These commands are alternatives unless your application's architecture specifically requires multiple processes.

Follow the actual configuration and startup logic rather than assuming both commands must be run.

---

## 09 · Verify the Installation

After startup, test the features supported by your current configuration.

| Verification          | Expected result                                            |
| --------------------- | ---------------------------------------------------------- |
| Application startup   | Main process starts without an initialization error        |
| Camera initialization | Camera frames become available                             |
| Face detection        | Faces can be detected in suitable frames                   |
| Face recognition      | Enrolled test identities can be matched                    |
| Phone detection       | Required model loads and performs detection                |
| Drowsiness analysis   | Facial landmarks and configured measurements are processed |
| Attendance processing | Attendance follows the application's configured rules      |
| Database operations   | Application data can be stored and retrieved               |
| Dashboard             | Configured web interface is accessible                     |
| Reports               | Report generation works when enabled                       |

Some features may require separate configuration, model files, or startup steps.

---

## 🛠️ Troubleshooting Lab

### Python is not recognized

Check your installation and system PATH, then reopen the terminal.

### Dependencies fail to install

Verify Python compatibility and inspect the package error before changing dependency versions.

### A model file cannot be found

Check the filename, configured path, and whether the required model was obtained separately.

### Camera initialization fails

Check camera permissions, the configured camera index, and whether another application is using the device.

### Flask reports a missing module

Activate the virtual environment and install the requirements from the correct application directory.

### Database operations fail

Verify the configured database path and filesystem permissions. Check the application logs for the underlying SQLite error.

### Dashboard is unavailable

Check the backend startup status, configured address and port, and frontend connection settings.

---

## 🔐 Security Before Deployment

Before running this system with real classroom data:

* Never commit passwords, API keys, SMTP credentials, or tokens.
* Keep facial images, student information, and attendance records private.
* Exclude local databases and generated reports from public version control.
* Use environment variables for sensitive configuration.
* Restrict access to protected backend endpoints.
* Obtain appropriate authorization before collecting or processing facial data.
* Review the security implications of public network exposure before deployment.

Refer to [`SECURITY.md`](SECURITY.md) for the project's security policy.

---

## 🧪 Recommended First Run

For a controlled initial test:

1. Start with a camera you can access directly.
2. Use test identities and authorized sample images.
3. Confirm that all required model files load.
4. Test one feature at a time.
5. Check the application logs after each test.
6. Verify that generated records are stored in the expected location.
7. Test the dashboard and reporting components separately if needed.

This process helps isolate setup problems before combining all monitoring features.

---

## 📚 Technical References

* [Python Documentation](https://docs.python.org/3/)
* [OpenCV Documentation](https://docs.opencv.org/)
* [Ultralytics Documentation](https://docs.ultralytics.com/)
* [MediaPipe Documentation](https://ai.google.dev/edge/mediapipe/solutions/guide)
* [Flask Documentation](https://flask.palletsprojects.com/)
* [SQLite Documentation](https://www.sqlite.org/docs.html)

---

## 🎯 Setup Complete

Once the environment, dependencies, model assets, camera, and database are configured, you can begin testing the application's supported functionality.

**Project:** [Smart Attendance and Student Monitoring System](https://github.com/Akashbs-06/Smart-Attendance-and-Student-Monitoring-System)

*This guide describes the general setup workflow. Verify model filenames, dependency compatibility, and startup commands against the current source code before treating the installation as tested.*

---
