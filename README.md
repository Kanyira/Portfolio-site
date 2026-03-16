Portfolio Site (Containerized)
This is my personal portfolio site, built with HTML and CSS, and fully containerized using Docker and Nginx. I built this to ensure the environment is consistent whether it's running on my local machine or a cloud VM.
🚀 The Setup
Instead of installing a web server directly on my VM, I’m using a lightweight Nginx (Alpine) image. This keeps the deployment clean and easy to tear down or update.
Project Structure
index.html: The main landing page.
homestyles.css: Custom styling.
images/: All visual assets for the site.
Dockerfile: Instructions for building the custom Nginx image.
docker-compose.yml: Handles port mapping and service orchestration.
🛠️ How to Run Locally
If you have Docker installed, you can get this site up in seconds:
Clone the repo:
bash
git clone git@github.com:Kanyira/Portfolio-site.git
cd Portfolio-site
Use code with caution.

Launch the container:
bash
docker compose up -d --build
Use code with caution.

View the site:
Open your browser and head to http://localhost:80 (or your VM's public IP).
💡 Key Technical Details
Port Mapping: The container listens on port 80, mapped directly to the host's port 80 for easy access without typing port numbers in the URL.
Base Image: I chose nginx:alpine to keep the image size under 50MB, making it fast to pull and deploy.
Detached Mode: I run the service with the -d flag so the web server stays active even after I close my terminal session.
