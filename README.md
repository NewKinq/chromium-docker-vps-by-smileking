# Chromium Docker VPS by Smileking

Run a full Chromium browser on your VPS using Docker Compose and noVNC. Access it directly in your browser—no extra apps needed.

---

##  Quick Start

1. Clone the repository:
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

##  Access the Browser

Open in your browser:
```
http://<your-server-ip>:5800
```

Login with:
- **Username:** `kasm_user`
- **Password:** `12345678`  
  (Set this in `docker-compose.yml` via `VNC_PW`)

Alternatively, use a VNC client:
```
<your-server-ip>:5900
```

---

##  Configuration

- Browser data and settings are stored in `./chrome-config`
- To change VNC password, edit:
  ```yaml
  environment:
    - VNC_PW=yournewpassword
  ```

---

##  Managing the Container

**Stop**:
```bash
docker compose down
```

**Restart**:
```bash
docker compose up -d
```

**View logs**:
```bash
docker logs -f chromium-vps
```

---

##  Requirements

- VPS with **at least 2 GB RAM**
- Docker & Docker Compose installed

---

##  Credits

Created by **Smileking** to help anyone easily run Chromium in a VPS.  
Built with the Docker image: [kasmweb/chrome](https://hub.docker.com/r/kasmweb/chrome)
