# RynthCore Website

Official website for RynthCore and RynthSuite - Modern Asheron's Call modding platform.

**Live Site:** [github.com/tombohar/rynthcore-website](https://github.com/tombohar/rynthcore-website)

## 📋 Pages

- **Home** (`index.html`) — Product overview and features
- **Commands** (`command-line.html`) — 40+ RynthAi commands reference
- **Expressions** (`expressions.html`) — 80+ AC expression variables
- **RynthAi** (`rynthai.html`) — Feature documentation
- **Releases** (`releases.html`) — Download latest versions
- **Readme** (`readme.html`) — Project information

## 🚀 Quick Start

### Option 1: GitHub Pages (Recommended)

#### Create a new GitHub Pages repository:

```bash
# 1. Create new repo: rynthcore-website
# (or use your GitHub username: tombohar.github.io)

# 2. Clone it locally
git clone https://github.com/tombohar/rynthcore-website.git
cd rynthcore-website

# 3. Copy all HTML files here
cp /c/projects/website/nexcore/*.html .

# 4. Create a .gitignore
cat > .gitignore << EOF
.DS_Store
Thumbs.db
*.log
EOF

# 5. Commit and push
git add .
git commit -m "Initial website commit"
git push origin main
```

#### Enable GitHub Pages:

1. Go to repo **Settings** → **Pages**
2. Under "Source," select **Deploy from a branch**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**
5. Wait ~2 minutes for the site to build

**Your site will be live at:**
- `https://tombohar.github.io/rynthcore-website/` (if separate repo)
- `https://tombohar.github.io/` (if using tombohar.github.io repo)

---

### Option 2: Custom Domain (Optional)

Point your domain to GitHub Pages:

1. **DNS Setup** (in your domain provider):
   ```
   A record:  185.199.108.153
   A record:  185.199.109.153
   A record:  185.199.110.153
   A record:  185.199.111.153
   
   CNAME:     www → tombohar.github.io (if separate repo)
   ```

2. **GitHub Setup:**
   - Settings → Pages → Custom domain
   - Enter: `rynthcore.dev` (or your domain)
   - Check "Enforce HTTPS"

3. **GitHub will auto-create CNAME file**

---

### Option 3: Alternative Hosting (Netlify/Vercel)

#### Netlify:
```bash
# 1. Connect your GitHub repo at: netlify.com
# 2. Select repository
# 3. Build settings:
#    - Build command: (leave empty)
#    - Publish directory: /
# 4. Deploy!
```

#### Vercel:
```bash
# 1. Go to vercel.com → New Project
# 2. Import your GitHub repo
# 3. Deploy automatically
```

---

## 📦 File Structure

```
rynthcore-website/
├── index.html              # Home page
├── command-line.html       # Commands reference
├── expressions.html        # Expression variables
├── rynthai.html           # RynthAi features
├── releases.html          # Download page
├── readme.html            # Project readme
├── assets/
│   └── logo.svg           # Brand logo
├── README.md              # This file
└── .gitignore
```

---

## 🔗 Links & Resources

- **RynthCore Repository:** https://github.com/tombohar/RynthCore
- **RynthSuite Repository:** https://github.com/tombohar/RynthSuite
- **GitHub Pages Docs:** https://pages.github.com/
- **Custom Domains:** https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

---

## ✏️ Making Updates

### To update the website:

```bash
# 1. Edit HTML files locally
# 2. Commit changes
git add .
git commit -m "Update: [description of changes]"
git push origin main

# 3. GitHub Pages auto-deploys in ~1-2 minutes
# 4. Check https://github.com/tombohar/rynthcore-website/deployments
```

---

## 🎨 Customization

### Change branding colors:
Edit the color definitions in each HTML file's `<style>` section:
```html
primary: '#26C1A6',    // Main teal
accent: '#E2B348',     // Gold
dark: '#0B1218',       // Dark bg
```

### Update GitHub links:
All GitHub links point to:
- `https://github.com/tombohar/RynthCore`
- `https://github.com/tombohar/RynthSuite`

Search & replace these URLs if you want to change them.

---

## 📊 Analytics (Optional)

Add Google Analytics or Plausible.io tracking by adding a script tag to the `<head>` section of each HTML file.

---

## 🆘 Troubleshooting

### Site not showing up?
- Wait 2-3 minutes after first push
- Check Settings → Pages → Source is set correctly
- Verify `main` branch is selected

### Getting 404 errors?
- Ensure all HTML files are in the root directory
- Check file names are lowercase and match links
- Clear browser cache (Ctrl+Shift+Delete)

### Custom domain not working?
- DNS changes can take up to 48 hours to propagate
- Check CNAME file exists in repo (GitHub creates it)
- Verify DNS records are correct

---

## 📝 License

Website content for RynthCore and RynthSuite projects.
See individual project repositories for license details.

---

**Last Updated:** April 18, 2026
