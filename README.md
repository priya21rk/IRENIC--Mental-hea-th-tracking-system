# Irenic - Mental Health Tracker

**Irenic** is a mental health tracking platform that helps users monitor and manage their well-being. This project consists of two main components:

1. **IrenicUI** - A TypeScript and Chakra UI-based frontend, providing an interactive dashboard for users to track and visualize mental health metrics.
2. **Stress Tracker API** - A Flask-based backend, which handles data processing, user authentication, and integrates with OpenAI for AI-driven insights.

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Features

### IrenicUI
- **Responsive Dashboard**: Built with Horizon UI and Chakra UI for a seamless user experience.
- **Data Visualization**: Tracks metrics like stress levels, mood, and other relevant health indicators.
- **User-friendly Design**: Provides a clean, modern interface for tracking mental health.

### Stress Tracker API
- **User Authentication**: Secure login and session management with JWT tokens.
- **AI-Enhanced Insights**: Utilizes OpenAI to provide users with mental health support and insights.
- **Data Persistence**: Stores user data, survey responses, and more in a PostgreSQL database.

---

## Project Structure
```plaintext
Irenic/
├── irenicUI/               # Frontend project directory
│   ├── src/                # Source files for the React/TypeScript app
│   ├── public/             # Public assets for the app
│   ├── package.json        # Node.js dependencies
│   └── tsconfig.json       # TypeScript configuration
└── stress_tracker/         # Backend project directory
    ├── app.py              # Main API server
    ├── Models.py           # Database models
    ├── Schemas.py          # Marshmallow schemas for data validation
    ├── requirements.txt    # Python dependencies
    ├── templates/          # HTML templates for the Flask app
    └── static/             # Static assets for Flask
```
---

## Setup and Installation

### Prerequisites
- **Node.js** and **npm** (for `irenicUI`)
- **Python 3.8+** (for `stress_tracker`)
- **PostgreSQL** (for backend database)

### Installation

#### 1. Clone the Repository
```bash
git clone https://github.com/your-username/irenic.git
cd irenic
```

#### 2. Frontend (IrenicUI) Setup
```bash
cd irenicUI
npm install
npm run build    # Build the project for production
```

#### 3. Backend (Stress Tracker API) Setup
Navigate to `stress_tracker` and create a virtual environment:

```bash
cd ../stress_tracker
python3 -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Set up PostgreSQL and environment variables (use `.env` and `.flaskenv` for configuration).

Run database initialization:
```bash
python db_init.py
```

Start the backend server:
```bash
flask run
```

---

## Usage

### Running the Frontend
In the `irenicUI` directory:
```bash
npm start
```
Access the frontend at `http://localhost:3000`.

### Running the Backend
In the `stress_tracker` directory:
```bash
flask run
```
The backend will be available at `http://localhost:5000`.

---

### API Endpoints

The API includes endpoints for:

- **User Registration and Authentication**: `POST /register`, `POST /login`
- **Mental Health Tracking**: `POST /track`, `GET /track/{user_id}`
- **AI Insights**: `GET /insights/{user_id}` (powered by OpenAI)

---

## Contributing
Feel free to contribute by opening an issue or submitting a pull request.
```
