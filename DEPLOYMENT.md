# Deployment Guide

This guide will help you deploy your website to GitHub Pages.

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name the repository: `barzamini.github.io` (must match your GitHub username)
5. Make it **public** (required for free GitHub Pages)
6. **Do NOT** initialize with README, .gitignore, or license
7. Click "Create repository"

## Step 2: Initialize Git and Push

Open a terminal in the website directory (`/home/hamed/projects/hyper/website`) and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Academic website"

# Add remote repository (replace with your actual GitHub URL if different)
git remote add origin https://github.com/barzamini/barzamini.github.io.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/barzamini/barzamini.github.io`
2. Click on "Settings" (top menu)
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click "Save"

## Step 4: Wait for Deployment

- GitHub will build your site using GitHub Actions (configured in `.github/workflows/jekyll.yml`)
- This usually takes 1-2 minutes
- You can check the deployment status in the "Actions" tab of your repository
- Once complete, your site will be live at: `https://barzamini.github.io`

## Step 5: Verify Your Site

1. Visit `https://barzamini.github.io` in your browser
2. Check that all pages load correctly:
   - Home page
   - About page
   - Publications page
   - News page
   - CV page
3. Verify PDF links work (CV downloads, publication PDFs)

## Updating Your Website

After making changes to your website:

```bash
# Navigate to website directory
cd /home/hamed/projects/hyper/website

# Add changed files
git add .

# Commit changes
git commit -m "Update website content"

# Push to GitHub
git push origin main
```

GitHub Actions will automatically rebuild and deploy your site.

## Troubleshooting

### Site not updating
- Check the "Actions" tab in your repository for build errors
- Ensure all files are committed and pushed
- Wait a few minutes for GitHub to rebuild

### Build errors
- Check that `Gemfile` is correct
- Verify `_config.yml` syntax is valid YAML
- Check that all Markdown files have proper front matter

### PDFs not loading
- Ensure PDF files are in `assets/pdf/` directory
- Check that PDF paths in `_data/publications.yml` match actual filenames
- Verify PDFs are committed to the repository

## Local Testing

To test your site locally before deploying:

```bash
# Install dependencies
bundle install

# Build and serve locally
bundle exec jekyll serve

# Open http://localhost:4000 in your browser
```

## Notes

- Your website will be publicly accessible at `https://barzamini.github.io`
- Changes may take a few minutes to appear after pushing
- The site uses GitHub Actions for automatic building and deployment
- All content is stored in this repository

