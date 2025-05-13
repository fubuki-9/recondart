# 🔍 ReconDart: OSINT Cybersecurity Platform

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![React 18+](https://img.shields.io/badge/React-18%2B-61DAFB)](https://react.dev/)

**Automated threat intelligence** with AI-powered analysis and interactive visualization.  
Scan IPs/domains/emails/files and map risks using **10+ security APIs** + **MITRE ATT&CK**.


## 🚀 Features

- 🔍 Unified scans for IP/Domain/Email/Phone/File
- 📊 Interactive attack graphs (ReactFlow)
- 🤖 AI recommendations (Google Gemini)
- 📁 Static file analysis (Mandiant Capa)
- 📄 PDF reports (planned)


## ⚙️ Tech Stack

**Frontend:**  
![React](https://img.shields.io/badge/-React-20232A?logo=react) ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript)  
**Backend:**  
![Python](https://img.shields.io/badge/-Python-3776AB?logo=python) ![Flask](https://img.shields.io/badge/-Flask-000000?logo=flask)

## 🛠️ Setup

```bash
 Clone & Install
git clone https://github.com/yourusername/ReconDart.git
cd ReconDart
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt

 Configure .env
echo "NUMVERIFY_API_KEY=your_key
VITE_GEMINI_API_KEY=your_gemini_key
VITE_BACKEND_URL=http://localhost:5000" > .env && cp .env FE/.env

 Install Frontend
cd FE && npm install

▶️ Usage
'''bash
 Start backend
python src/main.py

 Start frontend (from /FE)
npm run dev
