Got it — you want this **Court-Data Fetcher & Mini-Dashboard README** rewritten with *your* name, GitHub, LinkedIn, and other details instead of the original author’s, keeping it professional.

Here’s the updated version with your details integrated:

---

# 🏛️ Court-Data Fetcher & Mini-Dashboard



**Court-Data Fetcher & Mini-Dashboard** is a Python + Flask-based web application that allows users to fetch **Delhi High Court** case details by providing the Case Type, Case Number, and Filing Year.

The app:

* Provides a simple web UI for input
* Programmatically fetches case details from the **Delhi High Court public portal**
* Auto-handles numeric CAPTCHA
* Extracts **Parties’ Names**, **Filing & Next Hearing Dates**, and the **Most Recent Order/Judgment PDF**
* Stores every query and raw HTML response in **MySQL** for auditing
* Displays results in a clean dashboard with direct PDF download links
* Handles invalid inputs and site downtime gracefully

---

## ⚖️ Court Chosen

**Delhi High Court – Case Status (Case Type Wise)**
🔗 [https://delhihighcourt.nic.in/app/get-case-type-status](https://delhihighcourt.nic.in/app/get-case-type-status)

---

## ⚙️ Setup Steps

Follow these steps to run this project locally:

### **1️⃣ Clone the Repository**

```bash
git clone https://github.com/vyshu511/Court-Data-Fetcher-Mini-Dashboard.git
cd Court-Data-Fetcher-Mini-Dashboard/court_data_fetcher
```

### **2️⃣ Create a Virtual Environment**

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

**Linux / Mac:**

```bash
python3 -m venv venv
source venv/bin/activate
```

### **3️⃣ Install Project Dependencies**

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### **4️⃣ Setup MySQL Database**

```sql
CREATE DATABASE court_data;
USE court_data;

CREATE TABLE queries (
    id INT AUTO_INCREMENT PRIMARY KEY,
    case_type VARCHAR(50),
    case_number VARCHAR(50),
    filing_year VARCHAR(10),
    timestamp DATETIME,
    raw_response LONGTEXT
);
```

### **5️⃣ Run the Flask App**

```bash
python app.py
```

Then open: **[http://127.0.0.1:5000](http://127.0.0.1:5000)**

---

## 📦 Key Dependencies

* Flask – Web framework for UI and routing
* Selenium – Browser automation for fetching data
* WebDriver Manager – Automatically manages ChromeDriver
* BeautifulSoup4 – HTML parsing to extract case details
* MySQL Connector – Save query logs in MySQL database

---

## 🔒 CAPTCHA Strategy

The **Delhi High Court** case status page uses a **numeric text CAPTCHA**.
Our script automatically handles this without manual input or OCR.

If in the future it changes to image-based CAPTCHA, solutions like **Tesseract OCR** or manual token entry can be implemented.

---

## 📂 File Structure

```
Court-Data-Fetcher-Mini-Dashboard/
├── .github/
│   └── workflows/
│       └── python-ci.yml
├── court_data_fetcher/
│   ├── static/images/
│   │   ├── Court-Data Fetcher & Mini-Dashboard.gif
│   │   ├── ui_home.png
│   │   └── ui_result.png
│   ├── templates/
│   │   ├── index.html
│   │   └── result.html
│   ├── tests/test_app.py
│   ├── app.py
│   ├── scraper.py
│   ├── db.py
│   ├── config.py
│   ├── requirements.txt
│   └── Dockerfile
├── Demo_Video_Link_of_Task_1.txt
├── LICENSE
└── README.md
```

---

## 🎥 Demo Video

Watch the step-by-step screen capture on YouTube:
📺 https://drive.google.com/file/d/1GKRGXY_qCp3GIp-d1rKrXcGuVule3Qt_/view?usp=sharing

---

## 📫 Contact

<div align="center">

[![Email](https://img.shields.io/badge/Email-vyshunivi511%40gmail.com-red?style=flat\&logo=gmail)](mailto:vyshnavimanam23@gmail.com)

[![GitHub](https://img.shields.io/badge/GitHub-vyshu511-black?style=flat\&logo=github)](https://github.com/vyshu511)

</div>

---

## 📜 License

MIT License © 2025 [Vyshnavi Manam](https://www.linkedin.com/in/vyshnavi-manam)

