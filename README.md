# Hamed Barzamini - Academic Website

This is the source code for my academic website hosted on GitHub Pages at [barzamini.github.io](https://barzamini.github.io).

## Setup Instructions

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem

### Local Development

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Build and serve the site locally:
   ```bash
   bundle exec jekyll serve
   ```

3. Open your browser and navigate to `http://localhost:4000`

### Deployment to GitHub Pages

1. Create a new repository on GitHub named `barzamini.github.io`

2. Initialize git in this directory (if not already initialized):
   ```bash
   git init
   git remote add origin https://github.com/barzamini/barzamini.github.io.git
   ```

3. Add all files and commit:
   ```bash
   git add .
   git commit -m "Initial commit: Academic website"
   ```

4. Push to GitHub:
   ```bash
   git branch -M main
   git push -u origin main
   ```

5. Enable GitHub Pages:
   - Go to your repository settings on GitHub
   - Navigate to "Pages" in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

6. Your website will be live at `https://barzamini.github.io` within a few minutes

## Project Structure

- `_config.yml` - Jekyll configuration file
- `index.md` - Homepage
- `_pages/` - Additional pages (about, publications, news, cv)
- `_data/` - Data files (publications.yml, news.yml)
- `assets/` - Static assets (images, PDFs)
- `Gemfile` - Ruby dependencies

## Adding Content

### Publications

Edit `_data/publications.yml` to add new publications. Follow the existing format.

### News

Edit `_data/news.yml` to add news items. Use the format:
```yaml
- date: "YYYY-MM-DD"
  content: "Your news item here"
```

### Pages

Edit files in `_pages/` directory to modify page content.

## Customization

- Modify `_config.yml` to update site-wide settings
- Edit theme settings in `_config.yml` (currently using minima theme)
- Add custom CSS in `assets/css/` if needed
- Add images to `assets/img/`

## Notes

- The website uses Jekyll with the minima theme
- All content is written in Markdown
- PDFs should be placed in `assets/pdf/` directory
- Profile images should be placed in `assets/img/` directory

