# Private Mobile Massage · São Paulo - Website

Professional, responsive website for a private mobile massage service targeting international travelers in São Paulo.

## Features

- **Responsive Design**: Works perfectly on mobile, tablet, and desktop
- **Professional Layout**: Warm organic elegance design with terracotta and sage green accents
- **WhatsApp Integration**: Direct booking through WhatsApp
- **Therapist Profile**: Professional presentation with credentials
- **Transparent Pricing**: Clear pricing structure for different time slots
- **Comprehensive FAQ**: Answers to common questions
- **Optimized Performance**: Fast loading with optimized assets

## Deployment Instructions

### For GitHub Pages

1. **Create a GitHub Repository**
   - Go to github.com and create a new repository named `sp-mobile-massage` or similar
   - Clone it to your local machine

2. **Copy Files**
   - Copy all files from this folder to your repository root
   - Ensure `index.html` is in the root directory

3. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit: Mobile massage website"
   git push origin main
   ```

4. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click Save

5. **Your site will be live at**: `https://yourusername.github.io/sp-mobile-massage`

### For Other Hosting (Netlify, Vercel, etc.)

1. **Connect Repository**
   - Connect your GitHub repository to Netlify/Vercel
   - Select the repository

2. **Configure Build Settings**
   - Build command: (leave empty - static site)
   - Publish directory: `.` (root)

3. **Deploy**
   - Click Deploy
   - Your site will be live within minutes

### For Traditional Web Hosting

1. **Upload Files via FTP**
   - Connect to your hosting via FTP
   - Upload all files to your public_html or www directory
   - Ensure `index.html` is in the root

2. **Access Your Site**
   - Visit your domain in a browser

## File Structure

```
├── index.html              # Main HTML file
├── assets/
│   ├── index-*.css        # Compiled CSS (Tailwind)
│   └── index-*.js         # Compiled JavaScript (React)
├── __manus__/
│   └── debug-collector.js # Debug utilities
└── README.md              # This file
```

## Customization

To modify the website, you'll need to edit the source code and rebuild. The current deployment is a compiled production build.

### To Make Changes:

1. Contact the developer with your requirements
2. Changes will be made to the source code
3. The project will be rebuilt and redeployed

## WhatsApp Link

The WhatsApp booking link is configured to: `https://wa.me/message/BQYQWPM2BOPZN1`

To update this link, contact the developer.

## Support

For issues or questions about the website, please contact the developer.

---

**Created**: February 2026
**Design**: Warm Organic Elegance with Terracotta & Sage Green
**Technology**: React 19 + Tailwind CSS 4 + Vite
