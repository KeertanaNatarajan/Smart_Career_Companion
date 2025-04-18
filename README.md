
#  Smart Career Companion

An AI-powered career guidance platform that helps users:

✅ Build ATS-friendly resumes  
✅ Assess skills & identify gaps  
✅ Get real-time job & course recommendations via APIs  
✅ Simulate mock interviews  
✅ Calculate a personalized Candidate Profile Score  

##  Getting Started

 **Prerequisites**  
Make sure you have these installed on your computer:

- Python 3.11+ | To run the backend application | [Download](https://www.python.org/downloads/)
- Git | To clone this project from GitHub | [Download](https://git-scm.com/downloads)
- pip (comes with Python) | To install Python packages | Installed with Python
- Virtual Environment (venv) | For clean dependency management | `python -m venv venv`

These instructions will help you run the Smart Career Companion app on your local machine.

### 1. Clone the repo
```bash
git clone https://github.com/YOUR-USERNAME/smart-career-companion.git
cd smart-career-companion
```

### 2. Create a virtual environment
```bash
python3 -m venv venv
# macOS/Linux
source venv/bin/activate
# Windows (PowerShell)
venv\Scripts\Activate.ps1
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure API Keys & Environment Variables
You can simply edit the code by pasting your apikey for udemy api, gemini api, and rapidapi key for jsearch api and replace them approriately in the place of "your_api_key", instead of following the below step.

if you are the following below step make change necessary changes in your code.
Create a `.env` file in your project’s root directory:
```bash
touch .env  # (type in cmd or terminal)
```
Inside `.env`, add your private keys and configuration:
```ini
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=your_flask_secret_key
GEMINI_API_KEY=your_google_gemini_key
RAPIDAPI_KEY=your_rapidapi_key
```
 **Alternative:**  
If you prefer, you can create a sample config file:  
`instance/config.py.example`  
And write:

```python
FLASK_APP = "app.py"
SECRET_KEY = "your_secret_key"
GEMINI_API_KEY = "your_google_gemini_key"
RAPIDAPI_KEY = "your_rapidapi_key"
```

### 5. Initialize the database
```bash
flask db init      # (only the very first time)
flask db migrate
flask db upgrade
```

This will create your SQLite DB and apply all Alembic migrations.

### 6. Run the application
```bash
flask run
```
Point your browser to: [http://127.0.0.1:5000](http://127.0.0.1:5000) to see the home page.

---

###  How to Explore the Features

**Sign up / Log in**  
Create a new user account and authenticate.

**Resume Builder & PDF Generator**  
– Go to `Dashboard → Create Resume`  
– Fill in your details and click Generate  
– Download the PDF via `Dashboard → Download Resume`

**Resume Scoring**  
– Navigate to `Resume Score`  
– Upload any PDF to get an AI‑generated score & feedback.

**Certificates & QR Codes**  
– Go to `Badges & Certificates` to upload PDF badges.  
– View or download certificates, extract and verify any embedded QR code.

**Job Market Insights**  
– Visit `Job Market` (add optional `?country=` or `?domain=` filters)  
– Browse trending jobs, in‑demand skills, and salary benchmarks.

**Course Recommendations**  
– Go to `Skill Gap Analysis`, enter your current skills and target domain, and get Udemy course suggestions.

**Job Search**  
– Use `Job Recommendation`, fill in your preferences and skills, and see real‑time job listings.

**Career Catalyst Chatbot**  
– Head to `Career Catalyst`, select a topic (e.g. “Mock Interview”), and interact with the AI advisor.

**Mock Interviews**  
– Under `Mock Interview`, answer questions and receive feedback plus the next question in a chat flow.

---

###  Troubleshooting

- **Errors generating PDF:** Ensure `weasyprint` and `PyMuPDF` are installed.
- **Database issues:** Delete `instance/users.db` (if present) and rerun migrations.
- **API errors:** Double‑check your `.env` API keys.

---

###  License

This project is licensed under the MIT License - see the LICENSE file for details.  
![License Badge](https://img.shields.io/badge/License-MIT-green)

---

###  Contributors

Thanks to the amazing contributors who helped build this project!

- [Keertana Natarajan](https://github.com/KeertanaNatarajan) 
- [Rajalakshmi S](https://github.com/Rajalakshmi2702)   
- [Neelaveni R](https://github.com/Neelaveni1009)  

---

###  Tech Stack

- **Backend:** Flask, SQLAlchemy  
- **Frontend:** HTML, CSS, Bootstrap  
- **Database:** SQLite  
- **API Integrations:** RapidAPI, Google Gemini  
- **Tools:** WeasyPrint, PyMuPDF for PDF generation
