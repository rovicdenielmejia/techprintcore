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

### 2. Netlify (Easy Drag & Drop)

1. **Go to [Netlify.com](https://netlify.com)**
2. **Sign up/Login**
3. **Drag and drop your project folder** to the deploy area
4. **Get instant URL** (e.g., `https://amazing-name-123456.netlify.app`)

### 3. Vercel (Fast & Global)

1. **Go to [Vercel.com](https://vercel.com)**
2. **Sign up with GitHub**
3. **Import your repository**
4. **Deploy automatically**

### 4. Firebase Hosting (Google)

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
├── index.html              # Homepage (entry point)
├── about.html              # About page
├── Services.html           # Services page
├── Pricing.html            # Pricing page
├── loyalty perks.html      # Loyalty program
├── Contact us.html         # Contact page
├── styles.css              # Main stylesheet
├── trace.svg               # Logo
├── interior.jpg            # Interior image
├── Loyalty Card/           # Loyalty card images
├── README.md               # Documentation
├── .gitignore              # Git ignore file
└── DEPLOYMENT.md           # This file
```

## Important Notes

### Form Functionality
- **Contact Form**: Currently uses simulated email/Trello integration
- **For Production**: Replace with real email service (EmailJS, Formspree, etc.)
- **Trello Integration**: Requires API keys for production use

### Required Updates for Production

1. **Email Service Integration:**
   - Sign up for EmailJS, Formspree, or similar service
   - Replace simulated email sending with real API calls

2. **Trello Integration:**
   - Get Trello API key and token
   - Replace simulated Trello card creation with real API calls

3. **Domain Setup (Optional):**
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

© 2024 TechPrint Core. All Rights Reserved.
