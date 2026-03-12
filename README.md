<div align="center">

<img src="https://raw.githubusercontent.com/RDrahul123/RDrahul123/main/20251206_111856-IMG_STYLE~2.jpg" width="120" alt="Rahul Dodke" style="border-radius:50%"/>

# ✦ Rahul Dodke — Portfolio

**Data Science Analyst & Software Engineer**

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-RDrahul123.github.io-3b82f6?style=for-the-badge)](https://RDrahul123.github.io/Portfolio)
[![Admin Panel](https://img.shields.io/badge/⚙_Admin_Panel-Back_Office-8b5cf6?style=for-the-badge)](https://RDrahul123.github.io/Portfolio/admin.html)
[![GitHub Pages](https://img.shields.io/badge/Deployed_on-GitHub_Pages-24292e?style=for-the-badge&logo=github)](https://pages.github.com)

</div>

---

## ✨ Overview

A modern, fully dynamic portfolio website with a private **back office admin panel** — no server, no framework, no build step. Everything runs on pure HTML, CSS, and Vanilla JS deployed via GitHub Pages.

Edit your portfolio content from any device through the admin panel — changes go live on the website within **~60 seconds**.

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────┐
│                  GitHub Repository                   │
│                                                      │
│   index.html ──fetches──► data.json                  │
│   admin.html ──writes──►  data.json  (GitHub API)    │
│   .github/workflows/deploy.yml  (auto-deploy)        │
└─────────────────────────────────────────────────────┘
          │                          ▲
          │  Push to main            │ GitHub API (PUT)
          ▼                          │
   GitHub Actions             Admin Panel
   (auto-deploy)              (admin.html)
          │                          ▲
          ▼                          │ Login 🔐
   GitHub Pages               prakrit0566
   (live site)
```

**The flow:**
1. Edit content in the **Admin Panel**
2. Click **🚀 Publish Changes**
3. Admin writes `data.json` to GitHub via API
4. GitHub Actions auto-deploys
5. Portfolio fetches updated `data.json` on next load ✅

---

## 📁 File Structure

```
Portfolio/
├── index.html              # Main portfolio (renders from data.json at runtime)
├── admin.html              # Private back office admin panel
├── data.json               # 📦 Content database — all portfolio data lives here
├── .github/
│   └── workflows/
│       └── deploy.yml      # Auto-deploy on push to main
└── README.md
```

---

## 🚀 Features

### Portfolio (`index.html`)
- ⚡ **Zero build step** — pure HTML/CSS/JS, no npm, no webpack
- 🌗 **Dark / Light theme** with localStorage persistence
- 🎨 **Animated hero** with interactive particle canvas (mouse repulsion effect)
- 📱 **Fully responsive** — mobile hamburger menu included
- 🔄 **100% dynamic rendering** — all content loaded from `data.json`
- 🎯 **Project filter buttons** — filter by technology category
- 📊 **SVG Radar chart** with hover tooltips for skills proficiency
- ✨ **Scroll-triggered animations** via IntersectionObserver API
- 📄 **Inline resume** with PDF download link

### Admin Panel (`admin.html`)
- 🔐 **Private login** — username + password protected (session-scoped)
- 🔑 **GitHub API integration** — publishes directly to your repo
- ✏️ **Edit everything** — Hero, About, Experience, Projects, Skills, Education
- ➕ **Add / remove / reorder** any item in any section
- 💾 **One-click publish** — commits `data.json` and triggers live deploy
- 📊 **Dashboard** — content overview with item counts
- 🟢 **GitHub connection banner** — clear status indicator always visible

---

## 📦 Sections Managed via Admin

| Section | What You Can Edit |
|---------|-------------------|
| 👤 **Hero** | Name, role/title, bio paragraph, profile photo URL |
| 🙋 **About** | Two paragraphs, years of experience stat, records stat |
| 💼 **Experience** | Add/remove/reorder jobs · role, company, period, bullet points |
| 🗂 **Projects** | Title, description, tech tags, GitHub link, cover image URL |
| 🛠 **Skills** | Skill categories and comma-separated tech items per category |
| 🎓 **Education** | Institution, degree, period, grade/score |

---

## ⚙️ Setup & Deployment

### 1. Clone the repo

```bash
git clone https://github.com/RDrahul123/Portfolio.git
cd Portfolio
```

### 2. Enable GitHub Pages

> Repo → **Settings → Pages → Source → GitHub Actions** → Save

### 3. Push to `main`

```bash
git add .
git commit -m "🚀 Initial deploy"
git push origin main
```

Your site goes live at `https://RDrahul123.github.io/Portfolio` in ~60 seconds.

### 4. Connect the Admin Panel

1. Open `https://RDrahul123.github.io/Portfolio/admin.html`
2. Log in with your credentials
3. Click the **"Connect GitHub →"** banner on the dashboard
4. Generate a **Classic Personal Access Token**:
   - Go to [github.com/settings/tokens/new](https://github.com/settings/tokens/new)
   - Scope: ✅ **`repo`** (top-level checkbox)
   - Expiration: `No expiration`
5. Paste token + GitHub username + repo name → **Connect & Continue**

Every **🚀 Publish Changes** now updates your live site automatically.

---

## 🔑 GitHub Token Setup

| Setting | Value |
|---------|-------|
| Token type | **Classic** (not Fine-grained) |
| Scope | ✅ `repo` — top-level only |
| Expiration | No expiration |
| Repo → Actions → Workflow permissions | **Read and write** ✅ |

> ⚠️ Your token is stored only in your **browser's localStorage**. Never commit it to the repo.

---

## 🛠️ Tech Stack

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-24292e?style=flat-square&logo=github&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)

</div>

| Tool | Purpose |
|------|---------|
| Vanilla JS | All interactivity, dynamic rendering from `data.json` |
| CSS Custom Properties | Dark/light theming system |
| GitHub REST API v3 | Writing `data.json` directly from admin panel |
| GitHub Actions | CI/CD — auto deploy on every push |
| GitHub Pages | Free static hosting |
| Lucide Icons | Icon set loaded via CDN |
| Google Fonts | Space Mono · Syne · Inter |

---

## 👤 About Me

```python
rahul = {
    "name"     : "Rahul Dodke",
    "role"     : "Data Science Analyst & Software Engineer",
    "location" : "Indore, M.P, India",
    "skills"   : ["Python", "SQL", "Machine Learning", "Power BI", "AWS"],
    "impact"   : "15% improvement in data-driven decision making",
    "accuracy" : "99.9% in data preprocessing pipelines",
    "scale"    : "100K+ records processed & audited weekly",
}
```

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rahul-dodke)
[![GitHub](https://img.shields.io/badge/GitHub-24292e?style=flat-square&logo=github&logoColor=white)](https://github.com/RDrahul123)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat-square&logo=kaggle&logoColor=white)](https://www.kaggle.com/prakrit0566)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/rahul0566)
[![HackerRank](https://img.shields.io/badge/HackerRank-2EC866?style=flat-square&logo=hackerrank&logoColor=white)](https://www.hackerrank.com/profile/heyrahul_0566)
[![Google Dev](https://img.shields.io/badge/Google_Dev-4285F4?style=flat-square&logo=google&logoColor=white)](https://g.dev/rahulprakrit)

</div>

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">

**Built with ❤️ using HTML · CSS · Vanilla JS**

*No frameworks. No build tools. Just clean, fast, beautiful code.*

⭐ **Star this repo if you found it useful!**

</div>
