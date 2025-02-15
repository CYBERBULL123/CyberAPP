
# **CypherDeck AI** 🛡️

## **Overview** 🌐
This is a **Flask-based web application** that allows users to upload files (e.g., CSV, TXT, DOCX, PDF, etc.), extract text from them, and generate **AI-powered cybersecurity reports** using a **LangChain agent**. The application includes **user authentication**, **file uploads**, **report generation**, and **PDF download functionality**.

---

## **Features** ✨

1. **User Authentication** 🔐
   - Register, login, and logout functionality.
   - Password-protected user accounts.

2. **File Upload** 📂
   - Upload files in various formats (CSV, TXT, DOCX, PDF, JSON, LOG).
   - Extract text from uploaded files.

3. **Report Generation** 📝
   - Generate **AI-powered cybersecurity reports** using a **LangChain agent**.
   - Save reports to the database.

4. **Report Management** 📊
   - View, download (as PDF), and delete reports.

5. **Database** 🗄️
   - **SQLite** database for local development.
   - **PostgreSQL** support for production.

---

## **Technologies Used** 🛠️

### **Backend**
- **Flask** 🐍: Web framework for Python.
- **Flask-Login** 🔑: User session management.
- **Flask-SQLAlchemy** 🗂️: Database ORM.

### **Frontend**
- **HTML**, **CSS**, **JavaScript** 🌐: Frontend development.
- **Bootstrap** 🎨: Responsive design and styling.

### **Database**
- **SQLite** 🗄️: Local development database.
- **PostgreSQL** 🐘: Production database.

### **File Processing**
- **Custom File Processor** 📂: Extract text from various file formats (CSV, TXT, DOCX, PDF, etc.).

### **Report Generation**
- **LangChain Agent** 🤖: Generate AI-powered cybersecurity reports.
- **Google Generative AI** 🧠: Powering the LangChain agent.

### **PDF Generation**
- **ReportLab** 📄: Generate downloadable PDF reports.

### **Deployment**
- **Render** 🚀: Hosting and deployment platform.
- **Gunicorn** 🦄: WSGI server for production.

---

## **Data Flow** 🔄

### **1. User Registration** 📝
- User submits a registration form (username, email, password).
- The data is validated and stored in the `User` table.

### **2. User Login** 🔑
- User submits a login form (username, password).
- The credentials are verified against the `User` table.
- If valid, the user is logged in and redirected to the dashboard.

### **3. File Upload** 📂
- User uploads a file (CSV, TXT, DOCX, PDF, etc.).
- The file is processed to extract text using a custom file processor.

### **4. Report Generation** 📝
- The extracted text is passed to a **LangChain agent** to generate a cybersecurity report.
- The report is saved to the `Report` table.

### **5. Report Management** 📊
- Users can view, download (as PDF), or delete their reports.

---

## **Workflows** 🔄

### **1. User Authentication Workflow** 🔐
1. User registers with a username, email, and password.
2. User logs in with their credentials.
3. User logs out when done.

### **2. File Upload and Report Generation Workflow** 📂➡️📝
1. User uploads a file.
2. The file is processed to extract text.
3. The text is passed to the **LangChain agent** to generate a report.
4. The report is saved to the database and displayed to the user.

### **3. Report Management Workflow** 📊
1. User views their reports on the dashboard.
2. User can download a report as a PDF.
3. User can delete a report.

---

## **Deployment** 🚀

### **1. Deploy on Render**
1. Push your code to **GitHub**.
2. Go to [Render](https://render.com/) and create a new **Web Service**.
3. Connect your GitHub repository.
4. Set the following environment variables:
   - `SECRET_KEY`: A secret key for Flask.
   - `SQLALCHEMY_DATABASE_URI`: PostgreSQL connection string (e.g., `postgresql://user:password@host:port/database`).
5. Set the **Build Command**:
   ```bash
   pip install -r requirements.txt
   ```
6. Set the **Start Command**:
   ```bash
   gunicorn app:app
   ```
7. Deploy the app.

---

## **Folder Structure** 📂

```
cybersecurity-report-generator/
├── app.py                  # Main Flask application
├── requirements.txt        # Python dependencies
├── Procfile                # Deployment configuration
├── instance/               # SQLite database folder
├── uploads/                # Folder for uploaded files
├── templates/              # HTML templates
│   ├── home.html           # Home page
│   ├── login.html          # Login page
│   ├── register.html       # Registration page
│   ├── index.html          # File upload and report generation page
│   ├── dashboard.html      # User dashboard
│   ├── report.html         # Report view page
│   └── error.html          # Error page
├── static/                 # Static files (CSS, JS, images)
│   ├── css/
│   └── js/
├── langchain_agent.py      # LangChain agent for report generation
└── file_processor.py       # File processor for text extraction
```

---

## **Environment Variables** 🔧

- `SECRET_KEY`: Secret key for Flask session management.
- `DATABASE_URI`: Database connection string.
- `UPLOAD_FOLDER`: Folder for storing uploaded files.
- `GOOGLE_API_KEY`: Gemini multimodal Api.

---

## **Dependencies** 📦

```plaintext
Flask
Flask-Login
Flask-SQLAlchemy
google-generativeai
reportlab
langchain
langchain-google-genai
markdown
bs4
PyPDF2
python-docx
python-dotenv
gunicorn
requests
psycopg2-binary
```

---

## **Local Development** 💻

1. Clone the repository:
   ```bash
   git clone https://github.com/CYBERBULL123/CyberAPP.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   flask run
   ```

---

## **Production Deployment** 🚀

1. Push your code to **GitHub**.
2. Deploy on **Render** or **Heroku** using the steps mentioned above.

---

## **Contributing** 🤝

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a pull request.

---


## **Contact** 📧

For any questions or feedback, feel free to reach out:
- **Email**: opaadi98@gmail.com
- **GitHub**: [CYBERBULL123](https://github.com/CYBERBULL123)

---