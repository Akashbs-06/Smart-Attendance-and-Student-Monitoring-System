# Security Policy

## Overview

The Smart Attendance and Student Monitoring System is an AI-powered application designed to support automated student attendance and classroom monitoring using computer vision.

Security is important because the application may process facial images, student attendance records, classroom monitoring events, and other potentially sensitive information.

This document explains how to report security vulnerabilities and outlines recommended security practices for contributors and users.

## Supported Versions

Security fixes should target the latest maintained version of the project.

| Version                             | Security Support |
| ----------------------------------- | ---------------- |
| Latest version on the `main` branch | Best effort      |
| Older versions                      | Not guaranteed   |

This project is under active development, and formal release-based security support may not yet be established.

## Reporting a Vulnerability

**Please do not disclose security vulnerabilities publicly before the issue has been investigated.**

If you discover a potential security vulnerability:

1. Do not publish passwords, API keys, private student data, or exploit details in a public issue.
2. Report the issue privately to the repository maintainer through an available private contact method.
3. Include a clear description of the vulnerability.
4. Explain the potential impact and affected components.
5. Include reproduction steps where possible, without exposing real student data.

Repository:
https://github.com/Akashbs-06/Smart-Attendance-and-Student-Monitoring-System

If a private reporting channel has not been configured, contact the repository owner through an appropriate private channel before sharing sensitive technical details.

Please do not assume that a report has been received or that a fix is in progress until you receive confirmation.

## Security Best Practices

### 1. Protect Credentials

* Never commit passwords, API keys, access tokens, or SMTP credentials.
* Store sensitive configuration in environment variables.
* Keep local `.env` files out of version control.
* If a credential is accidentally exposed, revoke or rotate it immediately.

### 2. Protect Student Information

* Do not upload identifiable student photographs or facial datasets to a public repository.
* Do not commit attendance records, private databases, or generated reports containing personal information.
* Use synthetic or anonymized data for demonstrations and testing.
* Restrict access to student information to authorized users.

### 3. Secure Face Recognition and Monitoring Data

* Obtain appropriate authorization before collecting or processing facial images.
* Store facial data securely and limit access to authorized personnel.
* Establish suitable retention and deletion procedures.
* Avoid exposing student identities or monitoring events through public dashboards or logs.

### 4. Secure the Flask Backend

* Never use Flask's development server as a production deployment server.
* Keep debug mode disabled in production.
* Validate and sanitize incoming requests.
* Apply authentication and authorization to protected endpoints.
* Configure CORS to allow only trusted origins.
* Use secure session settings and protect authentication credentials.
* Avoid exposing stack traces, internal paths, or sensitive information in error responses.

### 5. Secure the Database

* Restrict access to SQLite database files.
* Use parameterized SQL queries rather than constructing queries from untrusted input.
* Protect database backups.
* Avoid committing production databases to Git.
* Ensure that database access follows appropriate authorization rules.

### 6. Manage Dependencies Safely

* Install dependencies from trusted sources.
* Review dependency updates and security advisories.
* Keep required libraries reasonably up to date.
* Test updates before deploying them.
* Avoid unnecessary dependencies.

### 7. Protect Model Files and Application Assets

* Obtain machine-learning models from trusted sources.
* Verify model provenance before using downloaded files.
* Do not load untrusted serialized model files.
* Keep private datasets and model-training artifacts out of public repositories unless their publication is authorized.

## Security Limitations

This project is under development. The security recommendations in this document do not guarantee that every component is secure.

Before deploying the application in a real classroom or production environment, review authentication, authorization, network exposure, data storage, logging, dependency management, and privacy controls.

## Responsible Disclosure

Contributors and users are encouraged to report vulnerabilities responsibly and avoid accessing, modifying, or disclosing data without authorization.

The project maintainer should assess reported vulnerabilities, determine their severity, and communicate appropriate remediation steps when possible.

Thank you for helping keep the Smart Attendance and Student Monitoring System secure.
