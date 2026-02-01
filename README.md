## Chemical Equipment Visualizer
A full-stack web application for analyzing and visualizing operational data from chemical plant equipment. The system processes CSV datasets and provides automated insights such as system health, risk alerts, and performance trends.

## Features
Upload CSV files containing equipment data
Automatic data analysis and summary generation
Equipment health scoring
Trend detection based on upload history
Real-time alerts for unsafe conditions
Historical data tracking
Interactive React dashboard
Desktop application (PyQt) version

## Tech Stack
## Backend
Python
Django
Django REST Framework
SQLite
Pandas

## Frontend
React
Fetch API
CSS
Desktop App
Python
PyQt5

## Setup Instructions
1. Clone the repository
git clone https://github.com/your-username/chemical-equipment-visualizer.git
cd chemical-equipment-visualizer

## Backend Setup
Create virtual environment
python -m venv venv
venv\Scripts\activate

## Install dependencies
pip install -r requirements.txt

## Run migrations
cd backend
python manage.py migrate

## Create admin user
python manage.py createsuperuser

## Start backend server
python manage.py runserver

## Backend runs at:

http://127.0.0.1:8000

## Frontend Setup
cd backend/web-frontend
npm install
npm start

## Frontend runs at:
http://localhost:3000

## Desktop Application
cd backend/desktop-app
python app.py

## Future Improvements
Predictive failure analysis
Machine learning risk scoring
Role-based authentication
Cloud deployment
Real-time monitoring

## Author
Ridhima
Chemical Equipment Visualizer
Full-stack engineering project
