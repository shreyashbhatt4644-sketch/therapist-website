# Deployment Guide - Dr. Maya Reynolds Website

This guide will walk you through deploying your website to various platforms.

## 📋 Pre-Deployment Checklist

- [ ] Test website locally in multiple browsers
- [ ] Check all links work correctly
- [ ] Verify images load properly
- [ ] Test contact form
- [ ] Check mobile responsiveness
- [ ] Review all content for accuracy
- [ ] Ensure contact information is correct

## 🚀 Deployment Options

### Option 1: GitHub Pages (Free & Easy)

**Step 1: Create GitHub Repository**
```bash
# Initialize git in your project folder
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Dr. Maya Reynolds therapy website"
```

**Step 2: Create Repository on GitHub**
1. Go to https://github.com
2. Click the "+" icon → "New repository"
3. Name it: `dr-maya-reynolds-website`
4. Don't initialize with README (you already have one)
5. Click "Create repository"

**Step 3: Push to GitHub**
```bash
# Replace YOUR_USERNAME with your GitHub username
git remote add origin https://github.com/YOUR_USERNAME/dr-maya-reynolds-website.git
git branch -M main
git push -u origin main
```

**Step 4: Enable GitHub Pages**
1. Go to repository Settings
2. Click "Pages" in the left sidebar
3. Under "Source", select "main" branch
4. Click "Save"
5. Wait a few minutes
6. Your site will be live at: `https://YOUR_USERNAME.github.io/dr-maya-reynolds-website`

**Custom Domain (Optional)**
1. Buy a domain (e.g., drreynoldstherapy.com)
2. In repository Settings → Pages
3. Add your custom domain
4. Configure DNS with your domain provider:
   - Add CNAME record pointing to YOUR_USERNAME.github.io
   - Add A records for GitHub Pages IPs

---

### Option 2: Netlify (Recommended for Custom Domains)

**Method A: Drag & Drop (Fastest)**
1. Go to https://app.netlify.com
2. Sign up / Log in
3. Drag your project folder onto the page
4. Done! You get a URL like `random-name-123.netlify.app`

**Method B: Continuous Deployment from Git**
1. Push your code to GitHub (see Option 1 steps 1-3)
2. Go to https://app.netlify.com
3. Click "Add new site" → "Import an existing project"
4. Connect to GitHub
5. Select your repository
6. Build settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty or enter `.`)
7. Click "Deploy site"

**Custom Domain on Netlify**
1. Click "Domain settings"
2. Click "Add custom domain"
3. Enter your domain name
4. Follow DNS configuration instructions
5. Netlify provides free SSL certificate

**Benefits of Netlify:**
- ✅ Free SSL certificate (HTTPS)
- ✅ Automatic deployments on git push
- ✅ Easy custom domain setup
- ✅ Form handling without backend code
- ✅ Fast global CDN

---

### Option 3: Vercel (Great for Developers)

**Step 1: Install Vercel CLI**
```bash
npm install -g vercel
```

**Step 2: Deploy**
```bash
# Navigate to your project folder
cd path/to/dr-maya-reynolds-website

# Deploy
vercel

# Follow the prompts:
# - Set up and deploy? Yes
# - Which scope? (your account)
# - Link to existing project? No
# - What's your project's name? dr-maya-reynolds-website
# - In which directory is your code located? ./
```

**Step 3: Production Deployment**
```bash
vercel --prod
```

**Custom Domain on Vercel**
```bash
vercel domains add yourdomain.com
```

---

### Option 4: Traditional Web Hosting (cPanel/FTP)

**Requirements:**
- Web hosting account
- FTP credentials
- FTP client (FileZilla, Cyberduck, etc.)

**Steps:**
1. **Download FileZilla** from https://filezilla-project.org

2. **Connect to your host:**
   - Host: ftp.yourdomain.com
   - Username: (from hosting provider)
   - Password: (from hosting provider)
   - Port: 21

3. **Upload files:**
   - Navigate to `public_html` or `www` folder
   - Upload all project files:
     - index.html
     - styles.css
     - script.js
     - images/ folder (with all contents)

4. **Visit your domain:**
   - Go to http://yourdomain.com
   - Your website should be live!

**Note:** Make sure your hosting supports:
- HTML5
- SSL certificate (for HTTPS)
- At least 100MB storage

---

### Option 5: Amazon S3 + CloudFront (Advanced)

**For high-traffic, professional deployment**

**Step 1: Create S3 Bucket**
1. Go to AWS Console → S3
2. Create bucket (name = your domain)
3. Enable static website hosting
4. Upload all files

**Step 2: Configure Permissions**
1. Unblock public access
2. Add bucket policy:
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "PublicReadGetObject",
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
  }]
}
```

**Step 3: Set up CloudFront (CDN)**
1. Create CloudFront distribution
2. Point to S3 bucket
3. Add SSL certificate
4. Configure custom domain

---

## 🔧 Post-Deployment Tasks

### 1. Set Up Contact Form
The contact form needs backend integration. Options:

**A. Formspree (Easiest)**
```html
<!-- In index.html, update the form tag: -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```
1. Go to https://formspree.io
2. Create account
3. Add your form
4. Get form ID
5. Update HTML

**B. Netlify Forms (if using Netlify)**
```html
<!-- Add to form tag: -->
<form name="contact" method="POST" data-netlify="true">
```

**C. EmailJS**
1. Sign up at https://www.emailjs.com
2. Create email service
3. Create email template
4. Update JavaScript code

### 2. Set Up Analytics

**Google Analytics**
```html
<!-- Add before </head> in index.html -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### 3. Enable HTTPS
- GitHub Pages: Automatic with custom domain
- Netlify: Automatic
- Vercel: Automatic
- Traditional hosting: Enable in cPanel or contact host

### 4. Submit to Search Engines

**Google Search Console**
1. Go to https://search.google.com/search-console
2. Add property (your domain)
3. Verify ownership
4. Submit sitemap

**Bing Webmaster Tools**
1. Go to https://www.bing.com/webmasters
2. Add site
3. Verify and submit

### 5. Create Sitemap

Create `sitemap.xml`:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yourdomain.com/</loc>
    <lastmod>2026-02-09</lastmod>
    <priority>1.0</priority>
  </url>
</urlset>
```

### 6. Add robots.txt

Create `robots.txt`:
```
User-agent: *
Allow: /

Sitemap: https://yourdomain.com/sitemap.xml
```

---

## 📱 Testing Your Deployment

1. **Test on multiple devices:**
   - Desktop computer
   - Tablet
   - Mobile phone

2. **Test in multiple browsers:**
   - Chrome
   - Firefox
   - Safari
   - Edge

3. **Check page speed:**
   - https://pagespeed.web.dev
   - Aim for score 90+

4. **Validate HTML:**
   - https://validator.w3.org
   - Fix any errors

5. **Check mobile-friendliness:**
   - https://search.google.com/test/mobile-friendly

6. **Test SSL:**
   - https://www.ssllabs.com/ssltest/
   - Should get A rating

---

## 🆘 Troubleshooting

### Images not loading
- Check file paths are correct
- Ensure images folder uploaded
- Check case sensitivity (image.jpg vs Image.jpg)

### Styles not applying
- Verify styles.css uploaded
- Check link tag in HTML
- Clear browser cache (Ctrl+F5)

### JavaScript not working
- Check script.js uploaded
- Open browser console (F12) for errors
- Verify script tag before </body>

### Form not submitting
- Check form action URL
- Verify backend is configured
- Test form validation

### Custom domain not working
- Check DNS settings (can take 24-48 hours)
- Verify CNAME/A records
- Clear DNS cache: `ipconfig /flushdns`

---

## 📞 Support Resources

- **GitHub Pages**: https://docs.github.com/pages
- **Netlify**: https://docs.netlify.com
- **Vercel**: https://vercel.com/docs
- **Web Hosting**: Contact your hosting provider

---

## ✅ Deployment Checklist

- [ ] Code tested locally
- [ ] Images optimized for web
- [ ] Content reviewed and accurate
- [ ] Contact form configured
- [ ] Analytics added
- [ ] Deployed to hosting platform
- [ ] Custom domain configured (if applicable)
- [ ] HTTPS enabled
- [ ] Tested on mobile devices
- [ ] Submitted to search engines
- [ ] Sitemap created
- [ ] robots.txt added

---

**Congratulations! Your website is now live! 🎉**

For ongoing maintenance and updates, refer to the main README.md file.
