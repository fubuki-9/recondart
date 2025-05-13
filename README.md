# ReconDart: Cybersecurity Reconnaissance and Analysis Platform

ReconDart is a web application designed to empower security analysts and organizations with comprehensive threat intelligence and reconnaissance capabilities. It automates the process of gathering, analyzing, and visualizing data from various open-source intelligence (OSINT) sources and threat feeds, allowing users to understand and visualize their digital security exposure across IP addresses, domains, emails, phone numbers, and usernames. The platform also includes static file analysis to identify potential malicious capabilities and leverages AI to provide actionable security recommendations.
Set up the Backend:

Navigate to the backend root directory (where src and requirements.txt are located).

Set up a Python virtual environment (recommended):
Bash

python -m venv venv
Activate the virtual environment:
On macOS and Linux:
Bash

source venv/bin/activate
On Windows:
Bash

venv\Scripts\activate
Install backend dependencies:
Bash

pip install -r requirements.txt
Create a .env file: In the backend root directory, create a file named .env.
Add your API keys and configurations to .env: Obtain necessary API keys (see "API Keys" section below) and add them to the file.
Code snippet

# Backend .env file
ipAPI_KEY=YOUR_IPAPI_KEY # Check if key is required for your use case based on ip-api.com tier
onypheAPI_KEY=YOUR_ONYPHE_KEY # Obtain from Onyphe
NUMVERIFY_API_KEY=YOUR_NUMVERIFY_KEY # Obtain from apilayer/NumVerify
GROCLAKE_API_KEY=YOUR_GROCLAKE_KEY # Based on groclake usage in /chat endpoint
GROCLAKE_ACCOUNT_ID=YOUR_GROCLAKE_ACCOUNT_ID # Based on groclake usage in /chat endpoint

# Frontend will also use this in its .env for direct calls
VITE_BACKEND_URL=http://localhost:5000
VITE_GEMINI_API_KEY=YOUR_GEMINI_API_KEY # Obtain from Google AI Studio/Cloud
3. Set up the Frontend:

Navigate to the frontend directory (likely FE within the repository).

Install frontend dependencies:
Using npm:
Bash

npm install
Using yarn:
Bash

yarn install
Create a .env file: In the frontend directory (FE), create a file named .env.
Add necessary environment variables to the frontend .env file:
Code snippet

# Frontend FE/.env file
VITE_BACKEND_URL=http://localhost:5000 # Ensure this matches the backend server address
VITE_GEMINI_API_KEY=YOUR_GEMINI_API_KEY # Your Google Gemini API key for frontend recommendations
▶️ Running the Application
Start the Flask Backend Server:
Navigate to the backend root directory (where src/main.py is located) and run:

Bash

python src/main.py
The backend should start and listen on http://localhost:5000.

Start the Frontend Development Server:
Navigate to the frontend directory (likely FE) and run:

Using npm:
Bash

npm run dev
