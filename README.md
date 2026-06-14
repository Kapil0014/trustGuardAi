#  TrustGuard AI

## FastAPI Backend for UI Dark Pattern Detection

TrustGuard AI is a backend service for auditing websites and applications for dark patterns. It supports image uploads, live URL scanning, sample datasets, and PDF report generation.

---

## 📁 Project Structure

```text
trustguard-backend/
├── main.py
├── analyzer.py
├── screenshot.py
├── report.py
├── models.py
├── sample_data.py
├── .env
├── .gitignore
└── requirements.txt
```

---

## 🚀 Setup

### 1. Create Virtual Environment

```bash
python -m venv venv
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Install Playwright Chromium

```bash
playwright install chromium
```

### 4. Configure Environment Variables

Create a `.env` file:

```env
GEMINI_API_KEY=your_key_here
```

---

## ▶️ Run the Application

```bash
uvicorn main:app --reload
```

Server URL:

```text
http://127.0.0.1:8000
```

---

## 📡 API Endpoints

### POST `/scan/image`

Upload and analyze a screenshot.

**Request**

* Content-Type: `multipart/form-data`
* Field: `file`

**Supported Formats**

* JPEG
* PNG
* WEBP

**Maximum Size**

* 10 MB

---

### POST `/scan/url`

Analyze a live webpage.

**Request**

```json
{
  "url": "https://example.com"
}
```

---

### GET `/samples`

Returns pre-built sample scan results.

---

### GET `/health`

```json
{
  "status": "ok",
  "version": "1.0.0"
}
```

---

### POST `/report/pdf`

Generate a branded PDF report.

Response:

```text
application/pdf
```

---

## ✨ Features

* Dark Pattern Detection
* Screenshot Analysis
* URL-Based Website Audits
* PDF Report Generation
* FastAPI REST APIs
* Gemini AI Integration
* Fallback Analysis Support

---

## 🛠️ Tech Stack

* Python
* FastAPI
* Playwright
* Gemini AI
* Pydantic
* ReportLab

