# Ip-rotation-with-TOR

# Proxy IP Rotation Dashboard

A Python Dash web app that rotates your outgoing IP address every 10 seconds using HTTP proxies.  
It fetches your current IP from `api.ipify.org` via different proxies and displays the info on a live dashboard.

---

## Features

- Validates proxy list on startup and removes dead proxies automatically  
- Rotates proxies every 10 seconds to change your public IP  
- Displays current IP and timestamped IP change log in a web dashboard  
- Built with Python, Requests, and Dash

---

## Prerequisites

- Python 3.7 or higher  
- `requests` and `dash` Python packages  

---

## Setup Instructions

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/proxy-ip-rotation-dashboard.git
   cd proxy-ip-rotation-dashboard
Create and activate a Python virtual environment (recommended):

bash
Copy code
python3 -m venv venv
source venv/bin/activate
Install required packages:

bash
Copy code
pip install -r requirements.txt
Add your proxies to proxies.txt (one proxy per line), e.g.:

cpp
Copy code
http://51.158.68.68:8811
http://91.219.236.21:8080
http://178.62.193.19:8080
Running the App
Run the app with:

bash
Copy code
python app.py
Open your browser and go to: http://127.0.0.1:8050

You will see the current IP address your requests come from and a log of IP changes.

Notes
Free proxies can be unreliable or slow — update proxies.txt regularly

If port 8050 is busy, change the port in app.py at the bottom:

python
Copy code
app.run(debug=True, port=8051)
Increase the timeout in the script if proxies are slow (default is 5 seconds)

Project Structure
bash
Copy code
proxy-ip-rotation-dashboard/
├── app.py            # Main Python app with IP rotation and Dash dashboard
├── proxies.txt       # List of HTTP proxies (one per line)
├── requirements.txt  # Python dependencies
└── README.md         # This file
Dependencies
requests

dash

Install with:

bash
Copy code
pip install requests dash
