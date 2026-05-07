# 🎓 Campus Connect

A full-stack web platform that bridges the gap between **students** and **universities** — enabling students to build their academic profiles, showcase projects, and discover campus events, while campuses can manage their presence and engage with their community.

---

## 🚀 Features

### For Students
- 📝 **Profile Management** — Set up a detailed academic profile with bio, university, field of study, skills, and social links (LinkedIn, GitHub)
- 📄 **Resume Builder** — Build and download a professional resume directly from your dashboard
- 💼 **Project Uploads** — Upload and showcase academic projects (PDF, DOCX, images, ZIP)
- 🔍 **Discover Campuses & Events** — Browse universities and explore upcoming campus events
- 🖼️ **Profile Picture Upload** — Personalize your student profile

### For Campuses
- 🏫 **Campus Profile** — Create and manage a rich university profile with photos, description, and location
- 📅 **Event Management** — Create, edit, and delete events (Workshops, Conferences, and more) with registration links
- 👥 **Student Discovery** — View and connect with students on the platform

### General
- 🔐 **Role-based Authentication** — Separate login flows for students and campuses
- 🔎 **Search** — Find students and campuses across the platform
- 📱 **Responsive UI** — Clean, mobile-friendly interface

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Flask |
| Database | SQLite + SQLAlchemy ORM |
| Frontend | HTML5, CSS3, JavaScript, Jinja2 |
| Auth | Werkzeug (password hashing) |
| Deployment | Vercel |

---

## 📁 Project Structure

```
Campus/
├── app.py                  # Main Flask application & all routes
├── models.py               # SQLAlchemy database models
├── extensions.py           # Flask extensions (db)
├── wsgi.py                 # WSGI entry point
├── vercel.json             # Vercel deployment config
├── static/
│   ├── css/                # Stylesheets
│   ├── js/                 # JavaScript files
│   ├── img/                # Static images & logos
│   └── uploads/            # User-uploaded files
│       ├── profiles/       # Student profile pictures
│       ├── campus/         # Campus images
│       ├── events/         # Event images
│       └── projects/       # Student project files
├── templates/
│   ├── index.html          # Landing page
│   ├── login.html          # Login page
│   ├── signup.html         # Signup page
│   ├── student_dashboard.html
│   ├── campus_dashboard.html
│   ├── resume_builder.html
│   ├── search.html / search_results.html
│   └── components/         # Reusable template components
└── instance/
    └── campus_connect.db   # SQLite database
```

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/campus-connect.git
   cd campus-connect
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install flask flask-sqlalchemy werkzeug
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Open your browser** and navigate to `http://localhost:5000`

---

## 🗄️ Database Models

| Model | Description |
|---|---|
| `User` | Core auth model with email, hashed password, and role (`student` / `campus`) |
| `Student` | Extended student profile — bio, skills, education, experience, certifications |
| `Campus` | University profile — name, location, website, founded year, photos |
| `Event` | Campus-hosted events with type, date, status, and optional registration URL |
| `StudentProject` | Projects uploaded by students with title, description, and file |
| `CampusPhoto` | Gallery photos associated with a campus profile |

---

## 🌐 Deployment

This project is configured for deployment on **Vercel** via `vercel.json` and `wsgi.py`.

To deploy:
```bash
npm install -g vercel
vercel
```

> **Note:** For production, replace the SQLite database with a hosted database (e.g., PostgreSQL) and set a fixed `SECRET_KEY` via environment variables.

---

## 📸 Screenshots

> *(Add screenshots of your landing page, student dashboard, campus dashboard, and resume builder here)*

---

## 🤝 Contributing
---

