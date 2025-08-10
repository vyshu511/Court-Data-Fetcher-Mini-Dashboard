Court Data Fetcher & Mini Dashboard
📌 Overview
The Court Data Fetcher & Mini Dashboard is a Python + Flask-based web application that allows users to search for legal case details from Indian court portals, extract key metadata, and display them in an easy-to-read dashboard.
It is designed for automation, efficiency, and simplicity, helping legal professionals, researchers, and interns quickly gather case-related data.

🚀 Features
Case Search Form: Input case type, case number, and filing year.

Web Scraping Integration: Fetches case details from Indian eCourts/District Court portals.

Metadata Extraction:

Party names

Filing dates

Order PDF links

Query Logging:

All searches stored in an SQL database (MySQL/SQLite).

User-Friendly Dashboard:

Displays results in tabular format.

Clickable links for order PDFs.

CAPTCHA Handling Strategy documented for manual & automated workflows.

Responsive UI using HTML, CSS, and Bootstrap.

🛠️ Tech Stack
Backend: Python, Flask

Frontend: HTML, CSS, Bootstrap

Database: MySQL / SQLite

Web Scraping: Requests, BeautifulSoup

Other Tools: JSON, Logging

📂 Project Structure
php
Copy
Edit
court-data-fetcher/
│
├── static/                # CSS, JS, and assets
├── templates/             # HTML templates
├── app.py                  # Main Flask application
├── scraper.py              # Web scraping logic
├── database.py             # DB connection and query logging
├── config.py               # Configuration settings
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
⚙️ Installation & Setup
1️⃣ Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/court-data-fetcher.git
cd court-data-fetcher
2️⃣ Create a Virtual Environment
bash
Copy
Edit
python -m venv venv
source venv/bin/activate   # For Linux/Mac
venv\Scripts\activate      # For Windows
3️⃣ Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4️⃣ Configure Database
For MySQL, update config.py with:

python
Copy
Edit
DB_CONFIG = {
    'host': 'localhost',
    'user': 'root',
    'password': 'your_password',
    'database': 'court_data'
}
For SQLite, set:

python
Copy
Edit
DB_PATH = "court_data.db"
5️⃣ Run the Application
bash
Copy
Edit
python scraper.py
Access the app at http://127.0.0.1:5000

📖 Usage
Open the web application in a browser.

Enter case type, case number, and filing year.

Click Search.

View:

Case parties

Filing dates

Order document links

All queries are stored in the database for later reference.

🧠 CAPTCHA Handling
Some court portals require CAPTCHA verification.

Manual Approach: User solves CAPTCHA in the browser.

Automated Approach: (Optional) Integrate with services like 2Captcha or OCR for automated solving.

📜 License
This project is licensed under the MIT License – feel free to modify and use it.

👨‍💻 Author
Developed by Vyshnavi Manam
B.Tech Artificial Intelligence & Data Science
GitHub: https://github.com/vyshu511

