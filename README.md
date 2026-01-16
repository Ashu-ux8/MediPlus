# 🏥 Mediplus: AI-Powered Telemedicine Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Tech Stack: Python/Flask](https://img.shields.io/badge/Backend-Python%20%7C%20Flask-blue.svg)](https://flask.palletsprojects.com/)
[![Database: Firebase](https://img.shields.io/badge/Database-Firebase%20Firestore-orange.svg)](https://firebase.google.com/docs/firestore)
[![ML Model: Random Forest](https://img.shields.io/badge/ML-Random%20Forest-green.svg)]()

> **Mediplus is a powerful, AI-integrated web platform designed to predict diseases, recommend specialized doctors, and streamline the entire healthcare access process through smart automation and secure data management.**

---

## ✨ Key Features & Capabilities

Our platform is built around three core pillars: **Intelligent Diagnosis**, **Verified Care**, and **Seamless Access**.

| Feature Category | Description | Technology Highlight |
| :--- | :--- | :--- |
| **🧠 AI-Powered Specialist Prediction** | Predicts probable diseases based on user-inputted symptoms and automatically recommends the most suitable specialist. Includes a **Severity Scoring** system to prioritize critical cases. | **Random Forest** Classifier, Pandas/NumPy, Custom Symptom Mapping CSV |
| **✅ Doctor Credential Verification** | Ensures patient safety and platform trustworthiness by automatically verifying doctor legitimacy against official registries using web scraping. | **Selenium** Web Scraper |
| **📍 Nearest Doctor Search** | Utilizes location data to help patients quickly find the closest available doctors for both emergency and routine care. | Location-Based Search Algorithm |
| **📅 Real-Time Appointment System** | Comprehensive system for searching doctors by specialization, checking availability, and booking appointments with real-time notifications. | **Firebase Firestore** for real-time data syncing |
| **🔒 Secure User Management** | Dedicated, role-based dashboards for both patients and doctors, with secure session management and data protection. | **Flask-Session**, Firebase Authentication |

---

## 💻 Tech Stack Overview

Mediplus is a full-stack application built with robust, modern technologies.

| Layer | Technologies | Purpose |
| :--- | :--- | :--- |
| **Frontend** | HTML, CSS (Mediplus Template), JavaScript | Modern, professional, and **Mobile-Responsive UI** for a seamless user experience across all devices. |
| **Backend** | **Python**, **Flask**, Flask-Session | Lightweight and scalable web framework for handling business logic and routing. |
| **Database** | **Firebase Firestore** | NoSQL cloud database for secure, real-time storage of patient, doctor, and appointment data. |
| **Machine Learning** | Random Forest, Pandas, NumPy | Core components for disease prediction and specialist recommendation. |
| **Web Scraping** | Selenium | Used exclusively for doctor credential verification. |
| **Deployment** | Gunicorn, Render | Production-ready deployment setup. |

---

## ⚙️ Installation & Local Setup

Follow these simple steps to get a local copy of Mediplus up and running.

### Prerequisites

*   Python 3.x
*   `git`

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/MEDIPLUS.git
cd mediplus
```

### Step 2: Set up the Virtual Environment

It is highly recommended to use a virtual environment to manage dependencies.

```bash
# Create a virtual environment
python3 -m venv venv

# Activate the virtual environment
source venv/bin/activate  # On Linux/macOS
# venv\Scripts\activate   # On Windows
```

### Step 3: Install Dependencies

Install all required Python packages using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### Step 4: Configure Firebase

1.  Create a new project on [Firebase Console](https://console.firebase.google.com/).
2.  Set up **Firestore** and **Authentication**.
3.  Download your Firebase configuration file (e.g., `firebase_config.json`) and place it in the root directory of the project (or configure environment variables as needed).

### Step 5: Run the Application

```bash
# Start the Flask application
python app.py
```

The application will now be running locally, typically at `http://127.0.0.1:5000`.

---

## 🗺️ Key Functional Routes

| Route | Description | Core Technology |
| :--- | :--- | :--- |
| `/` | Main Homepage | Frontend |
| `/LoginPatient`, `/LoginDoctor` | Dedicated login pages for patients and doctors | Flask-Session, Firebase Auth |
| `/DoctorProfile`, `/patient_profile` | Role-based user dashboards | Flask, Firebase Firestore |
| `/bookappoinment` | Appointment scheduling interface | Firebase Real-Time Sync |
| `/getPredictedDoctor` | Endpoint for the ML-based specialist recommendation | Random Forest Model |
| `/validate_doctor` | Endpoint that triggers the web-scraping verification process | Selenium |
| `/NearestDoctor` | Local doctor search results | Location Algorithm |

---

## 📧 Contact & Support

Have questions, feedback, or suggestions? We'd love to hear from you!

*   **Email:** [bookmydoc28@gmail.com](mailto:bookmydoc28@gmail.com)
*   **GitHub Issues:** Feel free to open an issue on this repository for bugs or feature requests.

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE.md](LICENSE.md) file for details.
