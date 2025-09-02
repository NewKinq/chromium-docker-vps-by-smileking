# Chromium Docker VPS by Smileking

Run Chromium browser inside a Docker container on your VPS with noVNC access through your browser.

## 🚀 Quick Start
1. Install Docker and Docker Compose on your VPS.
2. Clone this repository:
   git clone https://github.com/NewKinq/chromium-docker-vps-by-smileking.git
   cd chromium-docker-vps-by-smileking
3. Start the container:
   docker compose up -d
4. Access Chromium in your browser at:
   http://<your-server-ip>:5800

   - Username: kasm_user
   - Password: 12345678 (you can change it in docker-compose.yml)

## 🛠 Configuration
- The browser config is stored in ./chrome-config on your VPS.
- To update settings or install extensions, just use Chromium inside the noVNC window.
- Edit docker-compose.yml to change the password or port if needed.

## 🔄 Managing the Container
Stop the container:
   docker compose down

Restart the container:
   docker compose up -d

View logs:
   docker logs -f chromium-vps

## ✅ Requirements
- A VPS with at least 2GB RAM for smooth Chromium performance.
- Docker + Docker Compose installed.

## 🙌 Credits
Created by Smileking to help anyone easily run Chromium in a VPS.  
Image based on kasmweb/chrome.
