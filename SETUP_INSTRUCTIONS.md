# Setup Instructions for Your Personal Website

## Quick Start Guide

Your Jekyll-based personal academic website has been created! Follow these steps to customize and deploy it.

## 📋 Required Actions Before Deployment

### 1. Add Your Profile Photo
- Replace `assets/img/profile.jpg` with your actual photo
- Recommended size: 400x400 pixels (square format)
- JPG or PNG format

### 2. Add Your CV
- Replace `assets/CV_Samadhi_Senanayake.pdf` with your actual CV PDF

### 3. Update Your Email Address
- Edit `_data/social.yml`
- Replace `your.email@example.com` with your professional email address

### 4. Add Optional Links (if available)
- In `_data/social.yml`, uncomment and add:
  - Google Scholar profile
  - ORCID ID
  - ResearchGate or other academic profiles

## 🚀 Deploy to GitHub Pages

1. **Initialize git and commit** (if not already done):
   ```bash
   git add .
   git commit -m "Initial website setup"
   ```

2. **Create GitHub repository**:
   - Go to https://github.com/new
   - Repository name: `samadhisenanayake.github.io` (or your GitHub username + .github.io)
   - Make it Public
   - Do NOT initialize with README (you already have one)

3. **Push to GitHub**:
   ```bash
   git remote add origin https://github.com/samadhisenanayake/samadhisenanayake.github.io.git
   git branch -M main
   git push -u origin main
   ```

4. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click "Settings" → "Pages"
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Click "Save"

5. **Wait 2-5 minutes** for GitHub to build your site

6. **Visit your site**: `https://samadhisenanayake.github.io`

## 🔧 Local Development

To preview your site locally before deploying:

```bash
# Install Jekyll (first time only)
gem install jekyll bundler

# Serve the site locally
jekyll serve

# Visit http://localhost:4000 in your browser
```

## 📝 Customization Tips

### Adding New Publications
Edit `_data/publications.yml` and add new entries following the existing format:

```yaml
- title: "Your Paper Title"
  authors: "Author list with <strong>Senanayake, S.</strong> highlighted"
  venue: "Journal Name"
  volume: "Volume(Issue):Pages"
  year: 2025
  type: "journal"  # or "preprint"
  doi: "DOI number"
  link: "https://doi.org/..."
  summary: "Brief 1-3 sentence summary for general audience"
```

Don't forget to also add the BibTeX entry to `publications.bib`!

### Updating Your Bio
Edit the content in `index.md` under the `#about` section.

### Changing Colors
The main accent color is green (#059669). To change it:
- Open `assets/css/style.css`
- Search for `#059669` and replace with your preferred color

## 📧 Need Help?

If you encounter issues:
1. Check GitHub Pages build status in your repo's Actions tab
2. Verify all links in `_data/social.yml` are correct
3. Ensure your profile photo and CV files are properly added

## 🎨 Website Sections

Your site includes:
- **Hero**: Name, tagline, photo, and quick links
- **About**: Biography and education background
- **Research**: Research interests and technical skills
- **Publications**: Organized by type (journal/preprint) with summaries
- **CV**: Education and experience highlights
- **Contact**: Professional contact information

All sections can be edited in `index.md`.

---

Good luck with your new website! 🎉
