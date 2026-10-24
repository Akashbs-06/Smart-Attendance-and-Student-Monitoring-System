# Contributing to Smart Attendance and Student Monitoring System

Thank you for your interest in contributing to the **Smart Attendance and Student Monitoring System**! Contributions, bug reports, feature suggestions, and documentation improvements are welcome.

Our goal is to improve an AI-powered classroom monitoring system that uses computer vision to support automated attendance and student activity monitoring.

## 📋 Table of Contents

* [Getting Started](#getting-started)
* [Development Setup](#development-setup)
* [How to Contribute](#how-to-contribute)
* [Reporting Bugs](#reporting-bugs)
* [Suggesting Features](#suggesting-features)
* [Code Guidelines](#code-guidelines)
* [Commit Message Guidelines](#commit-message-guidelines)
* [Pull Request Process](#pull-request-process)
* [Privacy and Security](#privacy-and-security)
* [Code of Conduct](#code-of-conduct)

## Getting Started

Before contributing, please:

1. Read the project's `README.md`.
2. Review the existing source code and project structure.
3. Check existing issues to avoid duplicating work.
4. Identify a bug, improvement, documentation task, or new feature to work on.

## Development Setup

### 1. Fork the Repository

Fork this repository on GitHub:

https://github.com/Akashbs-06/Smart-Attendance-and-Student-Monitoring-System

### 2. Clone Your Fork

Replace `<your-username>` with your GitHub username.

```bash
git clone https://github.com/<your-username>/Smart-Attendance-and-Student-Monitoring-System.git
```

Navigate into the cloned project:

```bash
cd Smart-Attendance-and-Student-Monitoring-System
```

### 3. Create a Branch

Create a separate branch for your contribution:

```bash
git checkout -b feature/your-feature-name
```

For bug fixes, you can use:

```bash
git checkout -b fix/your-bug-name
```

### 4. Set Up the Environment

Navigate to the application directory:

```bash
cd final_year_project-main-main-main
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Some features require additional computer vision model files and a compatible camera. Follow the project's README and existing configuration for the required setup.

## How to Contribute

You can contribute in several ways:

* Fix bugs in existing functionality.
* Improve face detection and recognition.
* Improve mobile phone detection.
* Improve drowsiness detection.
* Enhance attendance management and reporting.
* Improve the dashboard and user interface.
* Improve database operations and error handling.
* Add automated tests.
* Improve installation instructions and documentation.

Please keep changes focused and explain the problem your contribution solves.

## Reporting Bugs

When reporting a bug, include:

* A clear and descriptive title.
* Steps to reproduce the issue.
* Expected behavior.
* Actual behavior.
* Relevant error messages or logs.
* Operating system and Python version.
* Relevant dependency versions, if known.

Do not include passwords, API keys, private student information, or identifiable student photographs in bug reports.

## Suggesting Features

Feature suggestions should explain:

1. The problem or limitation.
2. The proposed solution.
3. The expected benefits.
4. Any relevant technical considerations.

Check existing issues before submitting a new suggestion.

## Code Guidelines

Please follow these guidelines when making changes:

* Use clear, descriptive variable and function names.
* Follow standard Python conventions, including PEP 8 where practical.
* Keep functions focused and maintainable.
* Add comments when they clarify complex logic.
* Handle errors appropriately.
* Avoid introducing unnecessary dependencies.
* Preserve compatibility with the existing project structure.
* Update documentation when functionality or setup requirements change.
* Test changes before submitting a pull request.

For computer vision features, explain any important changes to model configuration, detection thresholds, or processing logic.

## Commit Message Guidelines

Write short, meaningful commit messages.

Examples:

```text
feat: improve face recognition
fix: handle camera initialization errors
docs: update installation instructions
test: add attendance module tests
refactor: simplify database operations
```

Use a descriptive message that explains the purpose of your change.

## Pull Request Process

Before submitting a pull request:

1. Make sure your changes are limited to the intended functionality.
2. Test the affected features.
3. Update relevant documentation.
4. Check that no credentials or private data are included.
5. Commit your changes with a descriptive message.
6. Push your branch to your fork.
7. Open a pull request against the original repository's `main` branch.

Include the following information in your pull request:

* Summary of changes.
* Reason for the changes.
* Related issue, if applicable.
* Testing performed.
* Screenshots for relevant user-interface changes.

Please be prepared to address review feedback and make additional changes if needed.

## Privacy and Security

This project processes facial images and classroom activity information. Contributors must take privacy and security seriously.

* Never commit student photographs or facial datasets.
* Never upload attendance records or private database files.
* Never commit passwords, email credentials, API keys, or other secrets.
* Use environment variables for sensitive configuration.
* Do not include identifiable personal information in example data or screenshots.
* Obtain appropriate authorization before collecting or processing personal data.
* Report potential security vulnerabilities privately to the repository maintainer rather than publishing sensitive details.

## Code of Conduct

All contributors are expected to communicate respectfully and constructively.

Harassment, discrimination, personal attacks, and abusive behavior are not acceptable. Feedback should focus on improving the project and helping contributors collaborate effectively.

## Questions

For questions or assistance, open a GitHub issue with a clear description of your question.

Repository:
https://github.com/Akashbs-06/Smart-Attendance-and-Student-Monitoring-System

Thank you for helping improve the Smart Attendance and Student Monitoring System!
