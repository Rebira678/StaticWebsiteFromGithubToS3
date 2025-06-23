
---

```markdown
# 🌐 RezaDay – Cloud & DevOps Portfolio Site

Welcome to **RezaDay**, a modern portfolio designed and developed by [Rebira Adugna](https://linkedin.com/in/rebira)—a Cloud & DevOps Engineer with 50+ real-world projects across AWS, Azure, Kubernetes, and CI/CD automation.

This project showcases a scalable and professional personal website built with HTML, CSS, and JavaScript, and deployed to AWS S3 using GitHub Actions.

---

## ✨ Features

- ⚡ Fast & responsive design (custom HTML/CSS/JS)
- 💠 Glassmorphism UI with scroll-based animations
- 📦 Automated S3 deployment with GitHub Actions
- ☁️ AWS S3 static website hosting
- 🌍 Ready for CDN, HTTPS & custom domain integration

---

## 🧱 Tech Stack

| Category         | Tools Used                                       |
|------------------|--------------------------------------------------|
| Front-End        | HTML5, CSS3, JavaScript (ES6)                    |
| Infrastructure   | AWS S3, GitHub Actions, Git CLI                  |
| CI/CD            | GitHub Workflows (YAML), jakejarvis/s3-sync-action |
| DevOps Practices | Version control, automation, IAC principles      |

---

## 📁 Folder Structure

```
rezaday-portfolio/
├── index.html
├── style.css
├── scripts.js
├── assets/
│   ├── profile.jpg
│   └── cloud-bg.jpg
└── .github/
    └── workflows/
        └── deploy-to-s3.yml
```

---

## 🚀 Deployment Process (End-to-End)

1. **Clone the Repo:**

   ```bash
   git clone https://github.com/yourusername/rezaday-portfolio.git
   cd rezaday-portfolio
   ```

2. **Customize Your Content:**
   - Update `index.html` with your bio, skills, and projects
   - Replace `cloud-bg.jpg` and `profile.jpg` in `/assets/`

3. **Set Up GitHub Actions for S3 Deployment:**
   - Create `.github/workflows/deploy-to-s3.yml`
   - Paste in the GitHub Actions workflow (see below)
   - Ensure correct spacing & formatting (YAML is space-sensitive!)

4. **Configure GitHub Secrets:**
   Add the following secrets to your GitHub repo:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_BUCKET_NAME`

5. **Set Up S3 Bucket for Hosting:**
   - Enable “Static website hosting”
   - Set `index.html` as your root document
   - Make your bucket public (via bucket policy)

6. **Push Changes to Deploy:**

   ```bash
   git add .
   git commit -m "🚀 Initial launch of RezaDay portfolio"
   git push origin main
   ```

7. **Visit Your Live Site:**
   - Go to your S3 static website endpoint
   - Or connect a custom domain via Route 53 (optional)

---

## ⚙️ Sample GitHub Actions Workflow

```yaml
name: Deploy to S3

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Upload to S3
        uses: jakejarvis/s3-sync-action@master
        with:
          args: --acl public-read --delete
        env:
          AWS_S3_BUCKET: ${{ secrets.AWS_BUCKET_NAME }}
          AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
          AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          AWS_REGION: "your-region"
          SOURCE_DIR: "./"
```

---

## 📬 Connect With Me

- 🌐 [LinkedIn](https://linkedin.com/in/rebira)
- 💻 [GitHub](https://github.com/rebira678)
- ✉️ Email: rebikman9@gmail.com

---

## 🪪 License

MIT License — feel free to use this template to build your own personal DevOps masterpiece.
```

---
