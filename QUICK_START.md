# Quick Start Guide

Your GitHub Pages website is ready! Here's what you need to do:

## 🚀 Deploy to GitHub Pages

1. **Create the repository on GitHub:**
   - Go to https://github.com/new
   - Repository name: `barzamini.github.io`
   - Make it **public**
   - Click "Create repository"

2. **Push your website:**
   ```bash
   cd /home/hamed/projects/hyper/website
   git init
   git add .
   git commit -m "Initial commit: Academic website"
   git remote add origin https://github.com/barzamini/barzamini.github.io.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: Deploy from branch
   - Branch: `main`, Folder: `/ (root)`
   - Click Save

4. **Wait 1-2 minutes** and visit: **https://barzamini.github.io**

## 📁 What's Included

- ✅ Homepage with bio and research highlights
- ✅ About page with education and experience
- ✅ Publications page (8 publications from your CV)
- ✅ News page with recent updates
- ✅ CV page with download links
- ✅ All PDFs copied to assets/pdf/
- ✅ Responsive design with navigation
- ✅ GitHub Actions workflow for automatic deployment

## ✏️ Customize Your Site

### Add/Edit Publications
Edit `_data/publications.yml`

### Add News Items
Edit `_data/news.yml`

### Update Personal Info
Edit `_config.yml`

### Modify Pages
Edit files in `_pages/` directory

## 🧪 Test Locally

```bash
cd /home/hamed/projects/hyper/website
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```

## 📚 More Help

See `README.md` and `DEPLOYMENT.md` for detailed instructions.

