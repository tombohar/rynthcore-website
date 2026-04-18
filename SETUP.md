# GitHub Pages Setup Guide

Follow these steps to get your RynthCore website live on GitHub Pages in minutes.

## 📋 Prerequisites

- GitHub account (free at github.com)
- Git installed on your computer
- All HTML files from the website

## 🚀 Step-by-Step Setup

### Step 1: Create GitHub Repository

1. Go to **github.com** and sign in
2. Click **+** icon (top right) → **New repository**
3. **Repository name:** `rynthcore-website`
   - Or use: `tombohar.github.io` (your GitHub Pages URL)
4. **Description:** "Official RynthCore website"
5. Select **Public** (required for free GitHub Pages)
6. Click **Create repository**

---

### Step 2: Clone Repository Locally

```bash
# Open terminal/PowerShell and run:
git clone https://github.com/YOUR_USERNAME/rynthcore-website.git
cd rynthcore-website
```

Replace `YOUR_USERNAME` with your actual GitHub username.

---

### Step 3: Add Website Files

```bash
# Copy all HTML files into the repository folder
# Files should be in the root directory:
# - index.html
# - command-line.html
# - expressions.html
# - rynthai.html
# - releases.html
# - readme.html

# Create .gitignore file
echo ".DS_Store
Thumbs.db
*.log" > .gitignore

# Verify files are there
ls -la
```

---

### Step 4: Commit and Push

```bash
# Stage all files
git add .

# Commit with message
git commit -m "Initial website launch"

# Push to GitHub
git push origin main
```

---

### Step 5: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right of repo)
3. Scroll down to **Pages** section (left sidebar)
4. Under "Source":
   - Select **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ (root)**
5. Click **Save**

✅ **Your site is now live!**

---

## 🌐 Access Your Website

### If using `rynthcore-website` repo:
```
https://YOUR_USERNAME.github.io/rynthcore-website/
```

### If using `tombohar.github.io` repo:
```
https://tombohar.github.io/
```

---

## 🎯 Optional: Custom Domain Setup

### If you own a domain (like rynthcore.dev):

#### 1. Create CNAME file in repository:

```bash
echo "rynthcore.dev" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push origin main
```

#### 2. Update DNS at your domain provider:

**If using separate repo (`rynthcore-website`):**

Add **A records** pointing to:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Or add **CNAME record:**
```
www → tombohar.github.io
```

**If using `tombohar.github.io` repo:**

Just add the A records above.

#### 3. Wait 24-48 hours for DNS to propagate

#### 4. GitHub will show green checkmark in Settings → Pages

---

## ✏️ Making Updates

```bash
# 1. Edit HTML files locally
# 2. Stage changes
git add .

# 3. Commit
git commit -m "Update: description of changes"

# 4. Push
git push origin main

# 5. Wait 1-2 minutes for auto-deployment
# 6. Refresh your website
```

---

## 🔍 Checking Deployment Status

1. Go to your repository
2. Click **Deployments** tab
3. You should see recent deployments with status
4. Green checkmark = deployment successful

---

## 🆘 Troubleshooting

### Site shows 404 error
- Wait 2-3 minutes (first deployment takes longer)
- Check Settings → Pages shows correct branch/folder
- Clear browser cache (Ctrl+Shift+Delete)

### Changes aren't showing up
- Did you push? Check `git push` output
- Wait 1-2 minutes for deployment
- Hard refresh browser (Ctrl+F5)

### Custom domain not working
- Check CNAME file exists in repo
- Verify DNS records in your domain provider
- DNS changes take up to 48 hours
- GitHub Settings → Pages should show domain

### GitHub Desktop users

Instead of command line:

1. Clone: File → Clone repository
2. Add files to folder
3. Commit: Click "Commit to main"
4. Publish: Click "Publish branch"
5. GitHub.com → Settings → Pages

---

## 📚 More Help

- **GitHub Pages Docs:** https://pages.github.com/
- **GitHub Pages Custom Domain:** https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
- **DNS Setup Help:** https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

---

## ✅ You're Done!

Your RynthCore website is now live and will automatically update whenever you push changes to GitHub.

**Share your site:**
```
https://tombohar.github.io/rynthcore-website/
```

Happy deploying! 🚀
