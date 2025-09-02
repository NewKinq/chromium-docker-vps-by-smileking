# Chromium VPS with Docker Compose

This project helps you run a remote Chromium browser on your VPS using Docker Compose.  
You can access it directly from your browser (no app needed) or through a VNC client.

---

## 🚀 Setup

1. Clone this repo to your VPS:
   ```bash
   git clone https://github.com/Smileking/chromium-docker-vps-by-smileking.git
   cd chromium-docker-vps-by-smileking
   ```

2. Start the container:
   ```bash
   docker compose up -d
   ```

3. Stop the container:
   ```bash
   docker compose down
   ```

---

## 🌐 Accessing the Browser

- Open in your browser:
  ```
  http://<your-server-ip>:5800
  ```
  Login with the password you set in `docker-compose.yml`.

- Or connect with a VNC client:
  ```
  <your-server-ip>:5900
  ```
  Password: `12345678` (or your chosen password)

---

## 🛠 Configuration

- Change the default VNC password by editing:
  ```yaml
  environment:
    - VNC_PW=yournewpassword
  ```

- Chromium settings and extensions will persist in:
  ```
  ./chrome-config
  ```

---

## 📦 Notes

- The container uses [`kasmweb/chrome`](https://hub.docker.com/r/kasmweb/chrome) image.
- If you face blank screen or EOF errors, refresh the page or try VNC instead.
- Update your VPS packages regularly for better performance.

---

## ✨ Credits
- Built using [Kasmweb Chrome](https://hub.docker.com/r/kasmweb/chrome) Docker image.
