# Setup Instructions for GitHub

## Quick Start Guide

This repository is ready to be pushed to GitHub. Follow these steps:

### Option 1: Using GitHub Web Interface (Easiest)

1. **Go to GitHub**: Visit https://github.com/new
2. **Create new repository**:
   - Repository name: `tech-layoffs-outages-analysis`
   - Description: "Interactive analysis of tech layoffs and their correlation with service outages"
   - Make it Public or Private (your choice)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
3. **Get the repository URL** (it will look like: `https://github.com/YOUR_USERNAME/tech-layoffs-outages-analysis.git`)

4. **Push your local repository**:
   ```bash
   cd /home/claude/tech-layoffs-outages-analysis
   git remote add origin https://github.com/YOUR_USERNAME/tech-layoffs-outages-analysis.git
   git branch -M main
   git push -u origin main
   ```

### Option 2: Using GitHub CLI

If you have GitHub CLI installed and authenticated:

```bash
cd /home/claude/tech-layoffs-outages-analysis
gh repo create tech-layoffs-outages-analysis --public --source=. --remote=origin --push
```

### Option 3: Manual Upload

1. Download the entire `/home/claude/tech-layoffs-outages-analysis` folder
2. Create a new repository on GitHub
3. Upload files through GitHub's web interface

## After Pushing to GitHub

### Enable GitHub Pages (Optional)

To make the interactive visualization accessible online:

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **main** branch and **/ (root)** folder
4. Click **Save**
5. Your visualization will be available at: `https://YOUR_USERNAME.github.io/tech-layoffs-outages-analysis/`

### Update the Footer Link

After creating the repository, update the GitHub link in `index.html`:

```html
<!-- Find this line in index.html and update with your actual GitHub username -->
<p><a href="https://github.com/YOUR_USERNAME/tech-layoffs-outages-analysis">📁 View on GitHub</a></p>
```

## Repository Structure

```
tech-layoffs-outages-analysis/
├── .gitignore              # Git ignore rules
├── README.md               # Project documentation
├── SOURCES.md              # Data sources and citations
├── index.html              # Interactive visualization
└── SETUP_INSTRUCTIONS.md   # This file
```

## Troubleshooting

### If you get authentication errors:

1. **HTTPS method**: GitHub will prompt for username and personal access token (PAT)
   - Generate a PAT at: https://github.com/settings/tokens
   - Use the PAT instead of your password

2. **SSH method**: Set up SSH keys
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   # Add the public key to GitHub at: https://github.com/settings/keys
   # Then use SSH URL: git@github.com:YOUR_USERNAME/tech-layoffs-outages-analysis.git
   ```

### If the remote already exists:

```bash
git remote remove origin
git remote add origin YOUR_GITHUB_URL
```

## Next Steps

After pushing to GitHub, you can:

1. **Share the visualization**: Send people to your GitHub Pages URL
2. **Collaborate**: Others can fork and contribute
3. **Track changes**: Use GitHub's issue tracker and pull requests
4. **Add more data**: Update the analysis as new layoffs/outages occur

## Current Status

✅ Repository initialized
✅ All files committed
✅ Ready to push to GitHub
⏳ Waiting for remote repository creation

---

**Questions?** Open an issue on GitHub after pushing the repository!
