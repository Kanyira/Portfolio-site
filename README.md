# 🚀 Abraham Kanyira | Personal Portfolio

**[Live Demo: https://kanyira.github.io/Portfolio-site/](https://kanyira.github.io/Portfolio-site/)**

Welcome to the repository for my personal portfolio website! This project is a fully responsive, modern web application designed to showcase my skills, experience, and services as a Web Developer, Data Analyst, and DevOps enthusiast.

The site is built with core web technologies and fully containerized using **Docker** and **Nginx (Alpine)** to ensure a consistent, lightweight, and highly portable environment, whether deployed locally or on a cloud VM.

---

## 🛠️ Tech Stack
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Deployment & Hosting**: Docker, Nginx (Alpine)
- **Design Features**: Responsive CSS Media Queries, CSS Flexbox, Micro-animations

---

## ✨ Features
- **Modern & Responsive Design**: Seamlessly adapts to all screen sizes (mobile, tablet, desktop).
- **Interactive Typewriter Effect**: Dynamic subtitle on the hero section highlighting different roles.
- **Downloadable CV Integration**: Direct link to download the latest professional CV.
- **Tabbed About Section**: Clean organization of Skills, Experience, and Education.
- **Optimized Deployment**: Uses `nginx:alpine` to keep the Docker image size under 50MB for lightning-fast deployments.

---

## 📂 Project Structure

```text
Portfolio-site/
│
├── index.html           # The main landing page
├── homestyles.css       # Custom styling and media queries
├── Abraham_CV.docx      # Downloadable CV document
├── images/              # Visual assets (profile photos, logos, etc.)
│   └── me.jpg
│
├── Dockerfile           # Instructions for building the custom Nginx image
└── docker-compose.yml   # Handles port mapping and service orchestration
```

---

## 🚀 Quick Start (Local Setup)

If you have Docker installed, you can get this site running locally in seconds.

**1. Clone the repository:**
```bash
git clone git@github.com:Kanyira/Portfolio-site.git
cd Portfolio-site
```

**2. Launch the container:**
Run the following command to build the image and start the container in detached mode (`-d`).
```bash
docker compose up -d --build
```

**3. View the site:**
Open your web browser and navigate to:
```text
http://localhost:80
```
*(Or navigate to your VM's public IP if deploying remotely).*

---

## 📝 How to Update Content

If you need to update the information on the site in the future, follow this guide:

### Update the CV
1. Replace `Abraham_CV.docx` in the root directory with your latest CV file.
2. If the new file has a different name (e.g., `resume.pdf`), update the `href` attribute inside `index.html` (around Line 36):
   ```html
   <a href="resume.pdf" download="Abraham_Kanyira_CV.pdf" class="btn">
   ```

### Update the Profile Photo
1. Place your new photo inside the `images/` folder.
2. In `index.html`, locate the `<div class="hero-image">` block (around Line 39).
3. Change the `src` attribute of the `<img>` tag to point to your new file:
   ```html
   <img src="images/new-photo.jpg" alt="Profile Picture">
   ```

### Update the Dynamic Text Roles
To change the text that automatically types itself in the hero section:
1. Scroll to the bottom of `index.html` (around Line 195).
2. Locate the JavaScript array:
   ```javascript
   const roles = ["Computer science student", "Web Developer", "Front-End Developer", "Free-Lancer"];
   ```
3. Edit the array items to reflect your current titles.

---

## 💡 Key Technical Details
- **Port Mapping**: The container listens on port `80`, mapped directly to the host's port `80` for easy access without typing port numbers in the URL.
- **Detached Mode**: Running the Docker service with the `-d` flag allows the web server to stay active even after the terminal session is closed.

---

## 📬 Contact
- **Email**: abrahamkanyira2002@gmail.com
- **LinkedIn**: [linkedin.com/in/abraham-kanyira](https://linkedin.com/in/abraham-kanyira-a48813318)
- **GitHub**: [github.com/Kanyira](https://github.com/Kanyira)

> **Copyright © 2026 Abraham Kanyira. All rights reserved.**
