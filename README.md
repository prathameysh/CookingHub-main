# 🍳 CookingHub

**CookingHub** is a visually appealing and beginner‑friendly recipe website that helps users discover, explore, and try out delicious recipes with ease. Whether you're a novice in the kitchen or a culinary enthusiast, CookingHub makes everyday cooking fun and simple.

---

## ✨ Features

- 🔍 Browse a curated collection of featured recipes
- 🧾 View detailed cooking and preparation times
- 📱 Fully responsive design — works across desktop and mobile
- 📄 Static HTML pages with clean structure and styling
- 🔗 Social media footer integration (Github, LinkedIn)
- 🔄 Smooth navigation through Home, About, Recipes, and Contact pages

---

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Deployment**: Hosted via modern static‑site platforms

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/prathameysh/CookingHub-main.git
   cd CookingHub-main
   Open locally
   ```

Simply open index.html in your browser to view.

Deploy

Push your versioned branch to any static hosting service (e.g., Vercel, GitHub Pages) for live deployment.

🧩 How It Works
index.html
Landing page showcasing featured recipes with preview cards.

recipes.html
Displays a grid/list of all available recipes with images, titles, and links.

about.html
Information about the project’s vision, purpose, and creator.

contact.html
A simple form for users to reach out or submit feedback.

styles.css
Contains responsive design rules, layout styling, fonts, and color definitions.

app.js
Optional JavaScript for added interactivity, form handling, or dynamic features.

# Simple workflow for deploying static content to GitHub Pages

name: Deploy static content to Pages

on:

# Runs on pushes targeting the default branch

push:
branches: ["main"]

# Allows you to run this workflow manually from the Actions tab

workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages

permissions:
contents: read
pages: write
id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.

# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.

concurrency:
group: "pages"
cancel-in-progress: false

jobs:

# Single deploy job since we're just deploying

deploy:
environment:
name: github-pages
url: ${{ steps.deployment.outputs.page_url }}
runs-on: ubuntu-latest
steps: - name: Checkout
uses: actions/checkout@v3 - name: Setup Pages
uses: actions/configure-pages@v3 - name: Upload artifact
uses: actions/upload-pages-artifact@v2
with: # Upload entire repository
path: "." - name: Deploy to GitHub Pages
id: deployment
uses: actions/deploy-pages@v2
