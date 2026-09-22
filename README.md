# AUAS Second-Stage Activity & Homework System

Responsive public dashboard for second-stage students of the Technical College of Informatics.
Only the instructor/manager can log in and add/edit/delete content.

## Features
- Public read-only student dashboard; no student account required.
- Second-stage scope is built into the application.
- Weekly organization with dates.
- Tasks grouped by subject and day.
- Homework, activities, assignments, announcements.
- Image/file attachment upload.
- Secure instructor login with hashed password.
- CSRF protection and login rate limiting.
- Responsive RTL Kurdish UI for mobile and laptop.
- SQLite for local development; PostgreSQL-ready for online hosting.

## Run locally
1. Install Python 3.11+.
2. `python -m venv .venv`
3. Activate the environment.
4. `pip install -r requirements.txt`
5. Copy `.env.example` to `.env` and change SECRET_KEY and ADMIN_PASSWORD.
6. Run: `python run.py`
7. Open http://127.0.0.1:5000/

Instructor login: http://127.0.0.1:5000/instructor/login

## Production
Use PostgreSQL and a production WSGI server such as Gunicorn. Set:
- SECRET_KEY
- DATABASE_URL
- ADMIN_USERNAME
- ADMIN_PASSWORD

Do not use the development server in production.
