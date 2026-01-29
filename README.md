# Saketh Varma - Personal Website

Personal academic website for Saketh Varma, hosted at [sakethvarma.com](https://sakethvarma.com)

## Setup Instructions

### 1. Create GitHub Repository

1. Go to GitHub and create a new repository
2. Name it: `sakethvarma.github.io` (or `yourusername.github.io`)
3. Make it public
4. Don't initialize with README (you already have these files)

### 2. Upload Files to GitHub

```bash
# Navigate to this folder
cd sakethvarma-github-pages

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit - Personal website"

# Add your GitHub repository as remote
git remote add origin https://github.com/yourusername/sakethvarma.github.io.git

# Push to GitHub
git push -u origin main
```

Note: If you get an error about 'master' vs 'main', use:
```bash
git branch -M main
git push -u origin main
```

### 3. Configure Custom Domain (sakethvarma.com)

#### On Your Domain Registrar:
1. Go to your domain registrar (where you bought sakethvarma.com)
2. Add these DNS records:

**For apex domain (sakethvarma.com):**
```
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

**For www subdomain:**
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

#### On GitHub:
1. Go to your repository settings
2. Scroll to "Pages" section
3. Under "Custom domain", enter: `sakethvarma.com`
4. Check "Enforce HTTPS" (after DNS propagates)

DNS changes can take 24-48 hours to propagate.

### 4. Customize Your Content

Edit these files to add your information:

**index.html:**
- Update bio and background
- Change university/department links
- Add your email

**research.html:**
- Add your publications
- Update author names and paper titles
- Add links to PDFs/arXiv/Code

**blog.html:**
- Add blog posts
- Update dates and titles

**assets/style.css:**
- Customize colors if desired (currently matches jgaeb.com)

**Add your headshot:**
- Place your photo at: `assets/images/headshot.jpg`
- Recommended size: 400x400px or similar square ratio

### 5. Enable GitHub Pages

1. Go to repository Settings → Pages
2. Source: Deploy from branch
3. Branch: main / (root)
4. Click Save

Your site will be live at:
- `https://yourusername.github.io` (immediately)
- `https://sakethvarma.com` (after DNS propagates)

## File Structure

```
sakethvarma-github-pages/
├── index.html          # Homepage
├── research.html       # Research/Publications page
├── blog.html          # Blog page
├── CNAME              # Custom domain configuration
├── README.md          # This file
└── assets/
    ├── style.css      # Stylesheet
    └── images/
        └── headshot.jpg  # Your profile photo (add this)
```

## Updating Your Website

To make changes:
1. Edit the files locally
2. Commit changes: `git add . && git commit -m "Update description"`
3. Push to GitHub: `git push`
4. Changes will appear live within a few minutes

## Credits

Design inspired by [jgaeb.com](https://jgaeb.com) - Clean, minimal academic portfolio style.

---

© 2021–2026 Saketh Varma
