# Manish Kumar - Portfolio Website

Modern, minimalist portfolio website for Azure Cloud Engineer, DevOps Engineer & FinOps Consultant.

🔗 **Live Site:** https://kumammanish.github.io

##  About

Azure Cloud Engineer and FinOps Consultant with 12+ years of experience in cloud infrastructure management, DevOps automation, and enterprise cloud consulting. Specialized in achieving 20-30% cost optimization through FinOps strategies and improving system reliability through AI-powered automation.

Currently based in Amsterdam, Netherlands, working as Senior DevOps Engineer and FinOps Consultant.

##  Features

- **Modern Design**: Clean, developer-focused aesthetic with smooth animations
- **Fully Responsive**: Optimized for desktop, tablet, and mobile devices
- **Fast Loading**: Pure HTML/CSS/JS with no dependencies
- **Dark Theme**: Easy on the eyes with a professional color scheme
- **Interactive Experience Tabs**: Clean way to showcase multiple roles
- **Project Showcase**: Highlight your best work with detailed descriptions
- **Skills Display**: Organized technology categories
- **SEO Optimized**: Meta tags for social media sharing

##  Built With

- HTML5
- CSS3 (CSS Grid, Flexbox, Animations)
- Vanilla JavaScript
- Font Awesome Icons
- Google Fonts (Inter)

##  Structure

```
kumam.github.io/
├── index.html              # Main portfolio page
├── README.md              # This file
├── .gitignore             # Git ignore file
└── assets/
    └── images/
        └── profile.png    # Profile photo
```

##  Customization

### Already Configured

The portfolio has been pre-configured with Manish Kumar's information. If you need to update any details:

### 1. Personal Information

Current settings in `index.html`:
- Name: Manish Kumar
- GitHub: kumam
- Email: kumam.manish@gmail.com
- LinkedIn: https://www.linkedin.com/in/kumam/
- Logo: `{'<MK />'}`
- Profile image: `assets/images/profile.png`

### 2. Colors

Modify CSS variables in `:root`:
```css
--bg-dark: #0a192f;      /* Main background */
--accent: #64ffda;       /* Accent color */
--text-primary: #ccd6f6; /* Primary text */
```

### 3. Content Sections

- **Hero**: Update intro text and description
- **About**: Add your bio and tech stack
- **Experience**: Update job tabs with your roles
- **Projects**: Replace with your actual projects
- **Skills**: Add/remove skill categories
- **Contact**: Update email and social links

## 📝 Deployment to GitHub Pages

1. **Create Repository**
   - Go to GitHub → New Repository
   - Name: `[yourusername].github.io`
   - Set to Public

2. **Upload Files**
   - Upload `index.html` and `assets/` folder
   - Or use Git commands (see below)

3. **Enable GitHub Pages**
   - Settings → Pages
   - Source: Deploy from branch
   - Branch: main → / (root)
   - Save

4. **Wait 5-10 minutes**
   - Your site will be live at `https://[yourusername].github.io`

##  Local Development

```bash
# Clone repository
git clone https://github.com/[yourusername]/[yourusername].github.io.git

# Open in browser
open index.html
# or use a local server:
python -m http.server 8000
```

##  Making Updates

```bash
# Make changes to files
# Then commit and push:

git add .
git commit -m "Update experience section"
git push origin main

# Changes will be live in 1-2 minutes
```

##  Social Links

Add your profiles in the side panels:
- GitHub: https://github.com/kumam
- LinkedIn: https://www.linkedin.com/in/kumam/
- Email: kumam.manish@gmail.com

##  Before Going Live

- [ ] Replace all placeholder text
- [ ] Add your profile photo (300x300px minimum, PNG format)
- [ ] Update all social media links
- [ ] Test on mobile device
- [ ] Verify all navigation works
- [ ] Check email link opens mail client
- [ ] Test on different browsers

##  Features Breakdown

### Navigation
- Fixed header with smooth scroll
- Mobile-responsive hamburger menu
- Animated link underlines

### Sections
1. **Hero**: Eye-catching intro with call-to-action
2. **About**: Bio with profile picture and tech stack
3. **Experience**: Tabbed interface for multiple roles
4. **Projects**: Card-based project showcase
5. **Skills**: Organized technology categories
6. **Contact**: Simple, clean contact section

### Design Elements
- Monospace code aesthetics (`< />` tags)
- Smooth scroll animations
- Hover effects on interactive elements
- Grayscale to color profile picture transition
- Fixed social media sidebars (desktop)

##  Analytics (Optional)

Add Google Analytics by inserting before `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## � License

Free to use for personal portfolios. No attribution required.

##  Issues?

- **Profile image not showing**: Check path is `assets/images/profile.png`
- **Layout broken**: Ensure all HTML tags are properly closed
- **Mobile menu not working**: Check JavaScript console for errors
- **Site not deploying**: Wait 10 minutes, verify repository is public

##  Tips

- Use high-quality profile photo (500x500px recommended)
- Keep project descriptions concise (2-3 sentences)
- Highlight measurable achievements in experience
- Test on actual mobile devices, not just browser resize
- Update regularly with new projects and skills

##  Contact

Questions or collaboration opportunities? Reach out at kumam.manish@gmail.com

---

** Azure Cloud Engineer | DevOps Engineer | Azure FinOps Consultant**

Built with ❤️ | Hosted on GitHub Pages | Last updated: October 2025
