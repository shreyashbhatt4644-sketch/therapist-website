# Dr. Maya Reynolds - Therapy Website (Lilac Template Style)

A beautiful, calming therapy website inspired by the Lilac Squarespace template, customized for Dr. Maya Reynolds, PsyD.

## 🌸 Design Features

This website replicates the elegant, minimalist aesthetic of the Lilac template with:

- **Soft, Feminine Color Palette**: Muted sage greens, warm beiges, and cream tones
- **Circular Image Displays**: Hero and specialty sections feature elegant circular image frames
- **Clean Typography**: Lora serif for headings, Montserrat sans-serif for body text
- **Generous White Space**: Breathing room that creates a calming, therapeutic feel
- **Smooth Animations**: Subtle scroll effects and transitions
- **Minimalist Layout**: Focus on content without visual clutter

## 📁 Project Structure

```
dr-maya-reynolds-website/
├── index.html          # Main HTML file
├── styles.css          # All CSS styling (Lilac template aesthetic)
├── script.js           # JavaScript functionality
├── images/             # Image assets
│   ├── dr-maya.png     # Dr. Reynolds' professional photo
│   ├── office-1.jpeg   # Office photo 1 (used in hero & specialties)
│   └── office-2.jpeg   # Office photo 2 (used in specialties & office section)
└── README.md           # This file
```

## 🎨 Design Elements

### Color Scheme
- **Primary**: #9B8B7E (Warm taupe)
- **Accent**: #A8C4C0 (Soft sage green)
- **Background**: Cream (#FAF8F6) and white
- **Text**: Charcoal gray (#4A4A4A)

### Typography
- **Headings**: Lora (elegant serif)
- **Body**: Montserrat (clean, modern sans-serif)

### Sections

1. **Hero** - Large circular office photo with elegant headline
2. **Intro** - Centered introductory paragraph
3. **About** - Dr. Reynolds' photo in circular frame with bio
4. **Specialties** - Three circular images showcasing service areas
5. **Approach** - Four cards explaining therapeutic methods
6. **Office** - Location details with office photos
7. **Testimonial** - Featured quote in elegant typography
8. **CTA** - Gradient background with call-to-action
9. **Contact Info** - Email, phone, and address
10. **Footer** - Simple, clean footer

## 🚀 How to Use

### View Locally

**Option 1: Open directly**
- Double-click `index.html` to open in your browser

**Option 2: VS Code Live Server**
1. Install "Live Server" extension in VS Code
2. Right-click `index.html`
3. Select "Open with Live Server"

**Option 3: Python Server**
```bash
cd dr-maya-reynolds-website
python -m http.server 8000
# Visit http://localhost:8000
```

## 📤 Deployment

### GitHub Pages (Free)
1. Create a GitHub repository
2. Upload all files
3. Go to Settings → Pages
4. Select main branch as source
5. Your site will be live at `https://username.github.io/repo-name`

### Netlify (Recommended)
1. Drag and drop your folder to https://app.netlify.com/drop
2. Get instant deployment with free SSL
3. Optional: Add custom domain

## 🎯 Customization

### Change Colors
Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #9B8B7E;    /* Warm taupe */
    --accent-color: #A8C4C0;     /* Soft sage */
    /* Customize these colors */
}
```

### Update Content
All content is in `index.html`. Each section is clearly marked with comments.

### Replace Photos
Simply replace the images in the `images/` folder with the same filenames, or update the image paths in `index.html`.

### Add/Remove Specialties
Find the "Specialties Section" in `index.html` and copy/paste the `.specialty-card` divs.

## ✨ Features

- ✅ Fully responsive (mobile, tablet, desktop)
- ✅ Smooth scroll navigation
- ✅ Circular image displays
- ✅ Fade-in animations
- ✅ Mobile-friendly hamburger menu
- ✅ Parallax hero effect
- ✅ Gradient CTA section
- ✅ Clean, semantic HTML
- ✅ Optimized performance
- ✅ Accessibility features

## 📱 Mobile Responsive

The website automatically adapts to all screen sizes:
- Desktop (1200px+)
- Laptop (968px - 1200px)
- Tablet (640px - 968px)
- Mobile (< 640px)

## 🔧 Technical Details

### No Dependencies Required
- Pure HTML5, CSS3, and Vanilla JavaScript
- Fonts from Google Fonts CDN
- No build process needed
- No npm packages required

### Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 🌟 What Makes This Different

This version matches the **Lilac Squarespace template** aesthetic:

1. **Circular Images** - Hero and specialty sections use elegant circular frames
2. **Soft Color Palette** - Muted, therapeutic colors instead of bold ones
3. **Minimal Navigation** - Simple, clean header
4. **Generous Spacing** - Lots of breathing room
5. **Elegant Typography** - Serif headings with sans-serif body
6. **Gradient CTA** - Beautiful gradient background for call-to-action
7. **Centered Content** - Many sections use centered alignment
8. **Soft Shadows** - Subtle shadows on images

## 📋 Before Going Live

- [ ] Update contact information (email, phone, address)
- [ ] Test on multiple devices and browsers
- [ ] Set up contact form backend (Formspree, Netlify Forms, etc.)
- [ ] Add privacy policy page (for HIPAA compliance)
- [ ] Configure SSL certificate (automatic with Netlify/GitHub Pages)
- [ ] Submit to Google Search Console

## 🆘 Need Help?

### Common Questions

**Q: How do I change the hero image?**
A: Replace `images/office-1.jpeg` or update the `src` attribute in the HTML

**Q: Can I add more specialties?**
A: Yes! Copy a `.specialty-card` div and customize the content

**Q: How do I make the contact form work?**
A: Add a form handler like Formspree or use Netlify Forms

**Q: Can I change the color scheme?**
A: Yes! Edit the CSS variables at the top of `styles.css`

## 📞 Contact Form Integration

To make the contact section functional:

### Option 1: Formspree (Easiest)
1. Go to https://formspree.io
2. Create a free account
3. Get your form endpoint
4. Add a contact form in HTML with the Formspree action URL

### Option 2: Netlify Forms
If deploying to Netlify, add `data-netlify="true"` to your form tag.

### Option 3: EmailJS
1. Sign up at https://emailjs.com
2. Configure email service
3. Add EmailJS SDK and update JavaScript

## 🎨 Design Philosophy

This website embodies:
- **Serenity** - Calming colors and spacious layout
- **Professionalism** - Clean, polished design
- **Approachability** - Warm, welcoming aesthetic
- **Trust** - Elegant, credible presentation
- **Simplicity** - Easy to navigate and understand

## 📊 Performance

- Lightweight (< 100KB total assets)
- Fast loading times
- Optimized images
- Minimal JavaScript
- SEO-friendly structure

## 🔒 Privacy & HIPAA

**Important**: The current setup is for informational purposes only. For HIPAA compliance:

1. Use HIPAA-compliant form services
2. Add a privacy policy page
3. Implement proper data encryption
4. Consider using a secure patient portal
5. Add appropriate disclaimers

## 🎯 Future Enhancements

Optional additions:
- [ ] Blog section
- [ ] Online booking integration
- [ ] Client testimonials (with consent)
- [ ] Resources library
- [ ] Newsletter signup
- [ ] Insurance information page

## 📝 License

Created for Dr. Maya Reynolds, PsyD. All rights reserved.

---

**Last Updated**: February 2026  
**Style**: Lilac Template Inspired  
**Tech Stack**: HTML5, CSS3, Vanilla JavaScript
