# GraniteRegulate: AI-Powered GDPR and HIPAA Compliance Tool

## 1. Project Overview

GraniteRegulate is an advanced, AI-powered solution designed to automatically detect violations of the General Data Protection Regulation (GDPR) and the Health Insurance Portability and Accountability Act (HIPAA) in corporate data. By analyzing meeting recordings and structured data files, our tool identifies and flags the presence of Personally Identifiable Information (PII) and Protected Health Information (PHI), ensuring your organization remains compliant with critical data protection regulations.

GDPR Compliance: Detects names, email addresses, phone numbers, and other sensitive personal data to ensure regulatory alignment.  
HIPAA Compliance: Flags health-related information such as diagnoses, patient records, and treatment data for unauthorized exposure.

## 2. Core Technology

GraniteRegulate leverages IBM’s Granite Large Language Models, offering high-precision speech-to-text and NLP capabilities. This enables accurate, real-time analysis of audio and textual datasets.

## 3. Key Features

- Real-Time Violation Detection: Detects GDPR and HIPAA violations in audio recordings and CSV files.
- Automated Task Management: Integrates with Asana, auto-generating tasks for each violation to ensure quick remediation.
- Comprehensive PDF Reporting: Generates clear, downloadable compliance reports with rule-specific insights.
- Interactive Dashboard: Built using React, visualizes violation data through dynamic charts and detailed tables.
- Rule Cross-Referencing: Compares data against GDPR and HIPAA rule sets for precision compliance validation.

## 4. System Architecture

### Backend (FastAPI)

- API Endpoints (main.py):
  - POST /api/analyze: Accepts .csv, .pdf, or .mp3/.wav files and initiates analysis.
  - POST /api/generate-report: Generates downloadable compliance reports.

- Violation Detection (watsonchat.py):
  - Uses ibm-watsonx-ai with ibm/granite-13b-instruct-v2 to analyze content for GDPR/HIPAA violations.

- Speech-to-Text (speech.py):
  - Transcribes meeting audio using IBM Watson STT V1 service.

- Asana Integration (asana_client.py):
  - Creates task items in Asana for every violation identified.

### Frontend (React)

- User interface for file uploads and dashboard
- Real-time charts and tables for violation insights
- Live updates as data is processed

## 5. Getting Started

### 5.1 Clone the repository

```bash
git clone https://github.com/your-repo/GraniteRegulate.git
cd GraniteRegulate

### 5.2 Clone the repository
bash
Copy
Edit
cd backend
cp .env.example .env  # Add your API keys and configurations
pip install -r requirements.txt
uvicorn main:app --reload

5.3 Frontend Setup
bash
Copy
Edit
cd frontend
npm install
npm run dev

6. Hackathon Showcase
GraniteRegulate was developed as part of the IBM Hackathon, showcasing the real-world application of IBM's Granite LLMs in solving compliance and data privacy challenges. The solution is robust, scalable, and effective in identifying regulatory violations in real-time.

7. Developer Info
Shoury Pandya
Email: pshoury@gmail.com
LinkedIn: https://linkedin.com/in/shourypandya
GitHub: https://github.com/ShouryPandya

8. License
This project is licensed under the MIT License. See LICENSE for more information.
