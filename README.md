# Chemical Equipment Parameter Visualizer  
**Hybrid Web + Desktop Application**

A full-stack data visualization system for analyzing and monitoring chemical equipment parameters from CSV datasets. The platform processes operational data and generates automated insights such as health scores, risk alerts, and historical trends.

This project was developed as part of a **technical screening task** to demonstrate real-world software engineering practices including backend API development, frontend integration, data analytics, and desktop UI design.

---

## Key Capabilities

### Data Handling
- CSV upload and parsing using Pandas  
- Automatic validation of required columns  
- Summary statistics computation  

### Analytics
- Equipment health scoring  
- Safe-range violation detection  
- Alert generation for abnormal parameters  
- Trend analysis across multiple uploads  

### Visualization
- Interactive React dashboard  
- Desktop PyQt application  
- Charts using Chart.js and Matplotlib  

### System Features
- REST API built with Django REST Framework  
- Authentication using environment variables  
- PDF report generation  
- Upload history tracking  

---

## Architecture Overview

```text
Frontend (Web) ───────┐
                      ├── Django REST API ─── SQLite DB
Desktop (PyQt) ───────┘
```

Both the web and desktop clients consume the **same backend API**, ensuring consistency across platforms.

---

## Tech Stack

### Backend
- Python  
- Django  
- Django REST Framework  
- Pandas  
- SQLite  

### Web Frontend
- React  
- JavaScript  
- Fetch API  
- CSS  

### Desktop Client
- Python  
- PyQt5  
- Matplotlib  

---

## Project Structure

```text
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
```

---

## Setup Guide

### 1. Clone Repository
```bash
git clone <repository-url>
cd chemical-equipment-visualizer
```

---

## Backend Setup

### Create virtual environment
```bash
python -m venv venv
venv\Scripts\activate
```

### Install dependencies
```bash
pip install -r requirements.txt
```

### Run migrations
```bash
cd backend
python manage.py migrate
```

### Create admin user
```bash
python manage.py createsuperuser
```

### Start server
```bash
python manage.py runserver
```

API available at:
```
http://127.0.0.1:8000/api
```

---

## Web Frontend Setup

```bash
cd backend/web-frontend
npm install
npm start
```

Frontend runs at:
```
http://localhost:3000
```

---

## Desktop Application

```bash
cd backend/desktop-app
python app.py
```

---

## CSV Format

Uploaded CSV files must follow this structure:

```text
Equipment Name,Type,Flowrate,Pressure,Temperature
Pump-1,Pump,120,30,80
Pump-2,Pump,150,32,85
Reactor-1,Reactor,200,50,120
...
```

---

## Environment Variables

Create a `.env` file inside:

```
backend/web-frontend/.env
```

```env
REACT_APP_API_BASE=http://127.0.0.1:8000/api
REACT_APP_API_USER=your_username
REACT_APP_API_PASS=your_password
```

These credentials are excluded from version control using `.gitignore`.

---

## Why This Project Stands Out

This project demonstrates:

- Full-stack system design  
- Real-world data processing  
- Secure configuration practices  
- Clean separation of concerns  
- Hybrid application architecture  

It simulates an **industrial monitoring system** and can be extended for predictive maintenance, anomaly detection, and operational intelligence.

---

## Author

**Ridhima**  
Chemical Equipment Parameter Visualizer  
Technical Screening Project  

