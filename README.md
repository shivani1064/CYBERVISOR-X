🛡️ CYBERVISOR-X — AI Threat Intelligence Platform

CYBERVISOR-X is a cybersecurity analytics platform that combines a modern React dashboard with a multi-agent security analysis engine. It enables security teams to authenticate securely, perform automated vulnerability assessments, monitor risk scores, explore the MITRE ATT&CK framework, and manage users through a unified interface.

📦 Project Components
Folder	Description	Technology	Port
cybervisor-x/	Frontend dashboard	React + Vite	5173
cyberagent/backend/	Email OTP server	Node.js + Express + Nodemailer	5000
cyberagent/	Security analysis API	Python + FastAPI	8000

The frontend and OTP server provide the complete user experience. The FastAPI analysis engine can be run separately for automated security analysis.

✨ Features
🔐 Secure authentication system
📧 Email-based OTP verification
👤 Role-based access control (Admin & Analyst)
📊 Security dashboard with analytics and risk visualization
🧠 Multi-agent vulnerability assessment engine
🗺️ MITRE ATT&CK matrix integration
📝 Audit logs and report generation
📄 PDF report export functionality
🚀 Responsive and modern user interface
🚀 Quick Start
Prerequisites
Node.js 18+
Python 3.8+ (optional, for analysis engine)
1. Clone the Repository
git clone https://github.com/shivani1064/CYBERVISOR.git
cd CYBERVISOR
2. Start the Frontend
cd cybervisor-x
npm install
npm run dev

Application runs at:

http://localhost:5173
3. Start the OTP Server

Open a new terminal:

cd cyberagent/backend
npm install
node server.js

Server runs at:

http://localhost:5000
4. Configure Email Service

Create a .env file inside:

cyberagent/backend/

Add:

EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password
PORT=5000
Gmail Setup
Enable Google 2-Step Verification.
Generate a Google App Password.
Use the generated App Password as EMAIL_PASS.

⚠️ Never commit .env files, passwords, API keys, or secrets to GitHub.

5. Start the Analysis Engine (Optional)
cd cyberagent
pip install -r requirements.txt
python main.py

API documentation:

http://localhost:8000/docs
🧠 Multi-Agent Analysis Workflow

The analysis engine processes security data through multiple specialized agents:

Raw Data
   ↓
Data Agent
   ↓
Vulnerability Agent
   ↓
Risk Agent
   ↓
Mitigation Agent
   ↓
Report Agent
   ↓
Security Report

The generated report includes:

Identified vulnerabilities
Risk assessments
Recommended mitigations
Prioritized action items
🧪 API Test

Once the FastAPI service is running:

curl -X POST http://localhost:8000/test

The API returns a sample security analysis report.

🗂️ Project Structure
CYBERVISOR/
│
├── cybervisor-x/
│   ├── src/
│   │   ├── components/
│   │   │   ├── pages/
│   │   │   ├── layout/
│   │   │   └── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│
└── cyberagent/
    ├── backend/
    ├── agents/
    ├── main.py
    └── requirements.txt
🛠️ Technology Stack
Frontend
React
Vite
React Router
Axios
Chart.js
jsPDF
Backend
Node.js
Express.js
Nodemailer
Analysis Engine
Python
FastAPI
Uvicorn
Pydantic
🔒 Security Notice

This project is intended for educational, research, and demonstration purposes.

Before deploying to any production environment:

Replace all development credentials.
Secure environment variables.
Configure proper database storage.
Implement production-grade authentication and authorization controls.
Enable HTTPS and security hardening measures.
📄 License

This project is licensed under the MIT License.

See the LICENSE file for details.

👩‍💻 Author

Shivani Reddy Katta

GitHub: https://github.com/shivani1064
