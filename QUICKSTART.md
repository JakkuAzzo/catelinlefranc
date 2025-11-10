# Quick Reference Guide

## File Structure Overview

```
catelinlefranc/
│
├── index.html              ← Main homepage (START HERE)
│
├── css/
│   ├── style.css          ← Main styles for all pages
│   └── project.css        ← Additional styles for project pages
│
├── js/
│   └── script.js          ← All JavaScript functionality
│
├── images/                 ← ADD YOUR PHOTOS HERE
│   └── README.md          ← Image guidelines
│
├── projects/              ← Project detail pages
│   └── some-way-of-togetherness.html
│
├── vintage/               ← Vintage camera series pages
│   └── 1927-houghton-butcher.html
│
├── README.md              ← Full documentation
├── DEPLOYMENT.md          ← How to deploy to GitHub Pages
├── .gitignore            ← Files to ignore in Git
└── QUICKSTART.md         ← This file!
```

## 🚀 Getting Started in 5 Minutes

### Step 1: Add Your Images

Place your photos in the `images/` folder with these names:

**Required:**
- `hero-bg.jpg` - Main background image (1920x1080px)
- `about-placeholder.jpg` - Your photo for About section (600x800px)
- `placeholder-1.jpg` to `placeholder-8.jpg` - Portfolio thumbnails (800x1000px)

**Optional (for project pages):**
- `project-1-1.jpg`, `project-1-2.jpg`, etc. - Project detail images
- `vintage-1927-1.jpg`, `vintage-1927-2.jpg`, etc. - Vintage camera images

### Step 2: Update Content

Open `index.html` and find these sections to edit:

#### Hero Section (Lines ~40-50)
```html
<h1 class="hero-title">
    <span class="hero-subtitle">Photography by</span>
    Catelin Le Franc  ← Change name if needed
</h1>
```

#### About Section (Lines ~200-220)
```html
<p class="about-description">
    Your bio text here...  ← Update your biography
</p>
```

#### Contact Section (Lines ~260-280)
```html
<p>contact@catelinlefranc.com</p>  ← Update email
<p>@catelinlefranc</p>              ← Update social handle
```

### Step 3: Test Locally

1. Double-click `index.html` to open in your browser
2. Navigate through all sections
3. Test the portfolio filter buttons
4. Check mobile view (resize browser window)

### Step 4: Deploy to GitHub Pages

Follow the instructions in `DEPLOYMENT.md` or quick version:

```bash
# In terminal, navigate to project folder
cd path/to/catelinlefranc

# Initialize git
git init
git add .
git commit -m "Initial commit"

# Create GitHub repo, then:
git remote add origin https://github.com/yourusername/yourrepo.git
git push -u origin main
```

Then enable GitHub Pages in your repository settings.

## 📝 Common Customizations

### Change Colors

Edit `css/style.css` (lines 1-12):

```css
:root {
    --primary-color: #2c2c2c;     ← Dark color
    --accent-color: #d4a373;      ← Highlight color
    /* Change these hex codes to your preferred colors */
}
```

### Add Portfolio Item

In `index.html`, copy this template and paste in the portfolio grid:

```html
<div class="portfolio-item" data-category="projects">
    <div class="portfolio-image">
        <img src="images/your-image.jpg" alt="Description">
        <div class="portfolio-overlay">
            <div class="portfolio-info">
                <h3>Project Title</h3>
                <p>Category</p>
                <a href="projects/your-project.html" class="portfolio-link">View Project</a>
            </div>
        </div>
    </div>
</div>
```

### Change Fonts

1. Go to [Google Fonts](https://fonts.google.com/)
2. Select your fonts
3. Copy the `<link>` tag
4. Replace the existing Google Fonts link in `index.html` (line ~13)
5. Update font families in `css/style.css`

## 🎨 Portfolio Categories

The site has two main categories:

1. **Projects** - Contemporary photography projects
   - Use `data-category="projects"`
   
2. **Vintage** - Vintage camera experimentations
   - Use `data-category="vintage"`

You can add more categories by:
1. Adding filter buttons in HTML
2. Adding corresponding `data-category` attributes
3. Updating the JavaScript filter logic

## 🐛 Troubleshooting

### Images Not Showing?
- Check file names match exactly (case-sensitive!)
- Ensure images are in `/images` folder
- Check file paths in HTML

### Styles Not Working?
- Clear browser cache (Ctrl+Shift+R / Cmd+Shift+R)
- Check CSS file path in HTML
- Look for typos in class names

### Mobile Menu Not Working?
- Check that `js/script.js` is linked in HTML
- Open browser console (F12) to see errors
- Ensure JavaScript is enabled

## 📱 Testing Checklist

Before deploying:

- [ ] All images load correctly
- [ ] All links work (internal and external)
- [ ] Mobile menu opens and closes
- [ ] Portfolio filters work
- [ ] Contact form fields are functional
- [ ] Test on mobile device or browser responsive mode
- [ ] Check all pages (index, project pages)
- [ ] Social media links are correct
- [ ] Content has no typos or placeholder text

## 🔗 Important Links

- **Main Site**: `index.html`
- **Styles**: `css/style.css`
- **Scripts**: `js/script.js`
- **Full Docs**: `README.md`
- **Deploy Guide**: `DEPLOYMENT.md`

## 💡 Tips

1. **Optimize Images**: Use [TinyPNG](https://tinypng.com/) before adding to site
2. **Test Mobile**: Always check mobile view before deploying
3. **Backup**: Keep original high-res images in a separate folder
4. **Version Control**: Commit changes regularly with clear messages
5. **Browser Test**: Check in Chrome, Firefox, Safari, and mobile browsers

## 📞 Need Help?

1. Check `README.md` for detailed documentation
2. Check `DEPLOYMENT.md` for deployment issues
3. Look at the sample pages (`projects/` and `vintage/` folders)
4. Search GitHub Issues or Stack Overflow for common problems

## ✅ Launch Checklist

Ready to go live? Make sure:

- [ ] All placeholder images replaced with real photos
- [ ] All text content updated (no "Lorem Ipsum")
- [ ] Contact information is correct
- [ ] Social media links are updated
- [ ] Tested on multiple devices
- [ ] Images are optimized
- [ ] Typos and grammar checked
- [ ] Links all work
- [ ] Analytics added (optional)
- [ ] Custom domain configured (optional)

---

**You're ready to showcase your photography! 📸**

If you followed all steps, your site should be live and looking great!
