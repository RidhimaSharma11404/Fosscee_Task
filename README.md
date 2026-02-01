## Chemical Equipment Parameter Visualizer : Hybrid Web + Desktop Application
1.A full-stack data visualization system for analyzing and monitoring chemical equipment parameters from CSV datasets. The platform processes operational data and generates automated insights including health scores, risk alerts, and historical trends.
2.This project was built as part of a technical screening task to demonstrate real-world software engineering practices, including API design, frontend integration, data analytics, and desktop UI development.

## Key Capabilities
## Data Handling
-CSV upload and parsing using Pandas
-Automatic validation of required columns
-Summary statistics computation
## Analytics
-Equipment health scoring
-Safe-range violation detection
-Alert generation
-Trend analysis across uploads
## Visualization
-Interactive React dashboard
-Desktop PyQt application
-Charts using Chart.js and Matplotlib
## System Features
-REST API (Django REST Framework)
-Authentication using environment variables
-PDF report generation
-Upload history tracking
## Architecture Overview

Frontend (Web) ───────┐
                      ├── Django REST API ─── SQLite DB
Desktop (PyQt) ───────┘
Both the web and desktop clients consume the same backend API, ensuring consistency across platforms.

## Tech Stack
## Backend
Python
Django
Django REST Framework
Pandas
SQLite

## Web Frontend
React
JavaScript
Fetch API
CSS
Desktop Client
Python
PyQt5
Matplotlib

## Project Structure
chemical-equipment-visualizer/
│
├── backend/
│   ├── api/                # Core API logic
│   ├── desktop-app/        # PyQt desktop client
│   ├── backend/            # Django settings
│   └── manage.py
│
└── web-frontend/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   └── services/
    └── package.json

## Setup Guide
1. Clone Repository
   git clone <repository-url>
   cd chemical-equipment-visualizer

## Backend Setup
1.Create virtual environment
  python -m venv venv
  venv\Scripts\activate
2.Install dependencies
  pip install -r requirements.txt
3.Run migrations
 cd backend
 python manage.py migrate
4.Create admin user
 python manage.py createsuperuser
5.Start server
 python manage.py runserver

API available at:
http://127.0.0.1:8000/api

## Web Frontend
cd backend/web-frontend
npm install
npm start

Frontend runs at:
http://localhost:3000

## Desktop Application
cd backend/desktop-app
python app.py
