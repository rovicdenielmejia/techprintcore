# TechPrint Core Website - Deployment Guide

## Quick Deployment Options

### 1. GitHub Pages (Recommended - Free)

1. **Create GitHub Repository:**
   - Go to [GitHub.com](https://github.com)
   - Click "New repository"
   - Name: `techprint-core-website`
   - Make it public
   - Don't initialize with README (we already have one)

2. **Push to GitHub:**
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/techprint-core-website.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Scroll to "Pages" section
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
   - Save

4. **Access Your Website:**
   - URL: `https://YOUR_USERNAME.github.io/techprint-core-website`

### 3. Netlify (Easy Drag & Drop)

1. **Go to [Netlify.com](https://netlify.com)**
2. **Sign up/Login**
3. **Drag and drop your project folder** to the deploy area
4. **Get instant URL** (e.g., `https://amazing-name-123456.netlify.app`)

### 2. Vercel (Recommended for this project)

1. **Go to [Vercel.com](https://vercel.com)**
2. **Sign up with GitHub**
3. **Import your repository**
4. **Deploy** — `vercel.json` is picked up automatically for clean URLs
5. **URLs**: `yoursite.vercel.app/`, `/about`, `/services`, etc. (no `.html` in the address bar)

### 4. Firebase Hosting

1. **Install Firebase CLI:**
   ```bash
   npm install -g firebase-tools
   ```

2. **Initialize Firebase:**
   ```bash
   firebase init hosting
   ```

3. **Deploy:**
   ```bash
   firebase deploy
   ```

## File Structure for Deployment

```
techprint-core-website/
├── vercel.json             # Vercel: clean URLs (no .html in address bar)
├── home.html               # Homepage (entry point)
├── About.html              # About page
├── Services.html           # Services page
├── Pricing.html            # Pricing page
├── loyalty perks.html      # Loyalty program
├── Contact us.html         # Contact page
├── Products.html           # Products page
├── styles.css              # Main stylesheet
├── Logo Circle White.png   # Logo (header/favicon)
├── interior.jpg            # Interior image
├── Loyalty Card/           # Loyalty card images
├── README.md               # Documentation
├── .gitignore              # Git ignore file
└── DEPLOYMENT.md           # This file
```

## Important Notes

### Clean URLs (Vercel)
The `vercel.json` rewrites enable extensionless URLs. Visitors see:
- `yoursite.com/` or `yoursite.com/home` (not `home.html`)
- `yoursite.com/about`, `/services`, `/pricing`, `/loyalty-perks`, `/contact`, `/products`

No subfolders or duplicate `index.html` files are needed—all pages are the root `.html` files; Vercel rewrites handle the clean URLs.

### Form Functionality
- **Contact Form**: Currently uses simulated email integration
- **For Production**: Replace with real email service (EmailJS, Formspree, etc.)

### Required Updates for Production

1. **Email Service Integration:**
   - Sign up for EmailJS, Formspree, or similar service
   - Replace simulated email sending with real API calls


2. **Domain Setup (Optional):**
   - Purchase custom domain
   - Configure DNS settings
   - Set up SSL certificate

## Testing Checklist

- [ ] All pages load correctly
- [ ] Navigation works on all pages
- [ ] Forms submit successfully
- [ ] Mobile responsiveness works
- [ ] All images load properly
- [ ] Contact information is correct
- [ ] Social media links work
- [ ] Email integration functions

## Support

For technical support or questions about deployment:
- **Email**: techprintcoreph@gmail.com
- **Phone**: 0954-176-3978

## License

© 2025 TechPrint Core. All Rights Reserved.
