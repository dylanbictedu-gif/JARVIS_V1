# GitHub Pages Deployment

Your JARVIS_V1 portfolio is now ready to deploy to GitHub Pages and run continuously online.

## Quick Setup

### 1. Create a GitHub Repository

- Go to [github.com/new](https://github.com/new)
- Create a new repository named `JARVIS_V1` (or any name you prefer)
- Do **NOT** initialize with README, .gitignore, or license

### 2. Connect & Push

Run these commands in your terminal:

```bash
cd /Users/dylan/JARVIS_V1

# Add your GitHub remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/JARVIS_V1.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

- Go to your repository on GitHub
- Click **Settings** → **Pages**
- Under "Source", select **Deploy from a branch**
- Select **main** branch
- Select `/static` as the folder
- Click **Save**

GitHub will build and deploy your site in ~1-2 minutes. Your portfolio will be live at:
```
https://YOUR_USERNAME.github.io/JARVIS_V1
```

## Updates

To update your portfolio:

```bash
cd /Users/dylan/JARVIS_V1
git add -A
git commit -m "Update portfolio"
git push
```

Your changes will automatically deploy within 1-2 minutes.

## No More Boot Command Needed

✅ Your site is now **always running** and accessible 24/7 online
✅ Automatic deployments on every push
✅ No local server needed
