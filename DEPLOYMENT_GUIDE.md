# Deployment Guide for Git Sites

This guide explains how to deploy your Private Mobile Massage website to various Git-based hosting platforms.

## Quick Start

Your website is ready to deploy as-is. All files are static HTML, CSS, and JavaScript.

### What You Have

- `index.html` - Main website file (contains the entire app)
- `assets/` - CSS and JavaScript files
- `__manus__/` - Debug utilities
- `package.json` - Project metadata
- `README.md` - Documentation

## Deployment Options

### Option 1: GitHub Pages (Free, Recommended)

**Steps:**

1. **Create a GitHub Account** (if you don't have one)
   - Go to github.com and sign up

2. **Create a New Repository**
   - Click "New" or go to github.com/new
   - Repository name: `sp-mobile-massage` (or any name you prefer)
   - Description: "Private Mobile Massage Service Website"
   - Choose "Public" (required for free GitHub Pages)
   - Click "Create repository"

3. **Upload Files**
   - Option A: Use GitHub's web interface
     - Click "Add file" → "Upload files"
     - Drag and drop all files from this folder
     - Commit with message: "Initial commit: Mobile massage website"
   
   - Option B: Use Git command line
     ```bash
     git clone https://github.com/YOUR_USERNAME/sp-mobile-massage.git
     cd sp-mobile-massage
     # Copy all files from this folder here
     git add .
     git commit -m "Initial commit: Mobile massage website"
     git push origin main
     ```

4. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Under "Build and deployment":
     - Source: "Deploy from a branch"
     - Branch: "main"
     - Folder: "/ (root)"
   - Click "Save"

5. **Access Your Site**
   - Wait 1-2 minutes
   - Your site will be live at: `https://YOUR_USERNAME.github.io/sp-mobile-massage`

### Option 2: Netlify (Free, Easy)

**Steps:**

1. **Sign Up**
   - Go to netlify.com
   - Click "Sign up"
   - Choose "GitHub" to connect your account

2. **Create New Site**
   - Click "New site from Git"
   - Select "GitHub"
   - Authorize Netlify to access your GitHub
   - Select the `sp-mobile-massage` repository

3. **Configure**
   - Build command: (leave empty)
   - Publish directory: `.` (or leave empty)
   - Click "Deploy site"

4. **Access Your Site**
   - Netlify will generate a URL like: `https://random-name.netlify.app`
   - You can customize the domain in Site settings

### Option 3: Vercel (Free, Fast)

**Steps:**

1. **Sign Up**
   - Go to vercel.com
   - Click "Sign Up"
   - Choose "GitHub"

2. **Import Project**
   - Click "New Project"
   - Select "Import Git Repository"
   - Select your `sp-mobile-massage` repository

3. **Deploy**
   - Framework: "Other" (static site)
   - Click "Deploy"

4. **Access Your Site**
   - Your site will be live at: `https://sp-mobile-massage.vercel.app`

### Option 4: GitLab Pages (Free)

**Steps:**

1. **Create GitLab Account**
   - Go to gitlab.com and sign up

2. **Create New Project**
   - Click "New project"
   - Name: `sp-mobile-massage`
   - Visibility: "Public"
   - Create project

3. **Upload Files**
   - Use web interface or Git command line (same as GitHub)

4. **Create `.gitlab-ci.yml`**
   - Add this file to your repository root:
   ```yaml
   pages:
     stage: deploy
     script:
       - mkdir .public
       - cp -r * .public
       - mv .public public
     artifacts:
       paths:
         - public
     only:
       - main
   ```

5. **Access Your Site**
   - Your site will be live at: `https://YOUR_USERNAME.gitlab.io/sp-mobile-massage`

### Option 5: Traditional Web Hosting (FTP)

**Steps:**

1. **Get FTP Credentials**
   - Contact your hosting provider
   - Get FTP host, username, and password

2. **Connect via FTP**
   - Use FTP client (FileZilla, WinSCP, etc.)
   - Connect with provided credentials

3. **Upload Files**
   - Navigate to `public_html` or `www` folder
   - Upload all files from this folder
   - Ensure `index.html` is in the root

4. **Access Your Site**
   - Visit your domain in browser

## Custom Domain

After deploying, you can add a custom domain:

- **GitHub Pages**: Settings → Pages → Custom domain
- **Netlify**: Site settings → Domain management
- **Vercel**: Settings → Domains
- **GitLab Pages**: Settings → Pages → Domains and certificates

## Updating Your Website

To make changes:

1. Edit files in your repository
2. Commit and push changes
3. Site will automatically redeploy (usually within 1-2 minutes)

## Troubleshooting

**Site shows 404 error:**
- Ensure `index.html` is in the root directory
- Check that GitHub Pages is enabled (if using GitHub)

**Site looks broken:**
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Check browser console for errors (F12)

**WhatsApp link not working:**
- Ensure you're clicking the WhatsApp button
- Check that your WhatsApp number is correct in the link

## Support

For deployment issues:
- GitHub Pages: docs.github.com/en/pages
- Netlify: docs.netlify.com
- Vercel: vercel.com/docs
- GitLab Pages: docs.gitlab.com/ee/user/project/pages/

---

**Website Version**: 1.0.0
**Last Updated**: February 2026
**Technology**: React 19 + Tailwind CSS 4 (Static Build)
