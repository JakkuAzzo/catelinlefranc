# Catelin Le Franc - Photography Portfolio

A modern, sleek portfolio website showcasing the photography work of Catelin Le Franc, featuring vintage camera experimentations and contemporary projects.

![Portfolio Preview](https://via.placeholder.com/1200x600/2c2c2c/ffffff?text=Catelin+Le+Franc+Photography)

## 🎨 Features

- **Responsive Design**: Fully responsive layout that works seamlessly on all devices
- **Smooth Animations**: CSS animations and transitions for an engaging user experience
- **Portfolio Filtering**: Interactive filtering system for browsing different project categories
- **Modern UI/UX**: Clean, artistic design with attention to detail
- **Performance Optimized**: Lazy loading images, debounced scroll events, and efficient code
- **GitHub Pages Ready**: Static site that can be easily deployed to GitHub Pages
- **SEO Friendly**: Semantic HTML and proper meta tags for search engine optimization

## 🛠️ Technologies Used

- **HTML5**: Semantic markup for better accessibility and SEO
- **CSS3**: Modern CSS features including:
  - CSS Grid & Flexbox for layouts
  - CSS Custom Properties (variables)
  - CSS Animations and Transitions
  - Media Queries for responsiveness
- **Vanilla JavaScript**: No dependencies, pure JS for all interactions
- **Google Fonts**: Playfair Display (headings) and Raleway (body text)

## 📁 Project Structure

```
catelinlefranc/
├── index.html              # Main homepage
├── css/
│   ├── style.css          # Main stylesheet
│   └── project.css        # Project page styles
├── js/
│   └── script.js          # JavaScript functionality
├── images/                # Image assets
│   ├── hero-bg.jpg
│   ├── about-placeholder.jpg
│   └── placeholder-*.jpg  # Portfolio images
├── projects/              # Individual project pages
│   ├── some-way-of-togetherness.html
│   ├── contemporary.html
│   └── recent.html
├── vintage/               # Vintage camera series pages
│   ├── 1927-houghton-butcher.html
│   ├── 1934-zeiss-ikon.html
│   ├── 1938-zeiss-ikon-klio.html
│   ├── 1940s-kodak-brownie.html
│   └── 1978-kodak-ektra.html
├── README.md              # This file
├── DEPLOYMENT.md          # Deployment instructions
└── .gitignore            # Git ignore file
```

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/catelinlefranc.git
cd catelinlefranc
```

### 2. Add Your Images

Replace placeholder images in the `/images` directory with your actual photography:

**Required Images:**
- `hero-bg.jpg` - Hero section background (1920x1080px recommended)
- `about-placeholder.jpg` - About section image (600x800px recommended)
- `placeholder-1.jpg` through `placeholder-8.jpg` - Portfolio grid images (800x1000px, 4:5 ratio)

### 3. Customize Content

Edit `index.html` to update:
- Personal information in the About section
- Contact details
- Social media links
- Portfolio project titles and descriptions

### 4. Preview Locally

Open `index.html` in your web browser to preview the site locally.

### 5. Deploy to GitHub Pages

See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed deployment instructions.

## 📸 Image Guidelines

### Optimization
- Compress images before uploading using tools like:
  - [TinyPNG](https://tinypng.com/)
  - [Squoosh](https://squoosh.app/)
  - [ImageOptim](https://imageoptim.com/) (Mac)
- Target file size: Under 500KB for large images, under 200KB for portfolio items

### Dimensions
- **Hero Background**: 1920x1080px (16:9 ratio)
- **Portfolio Images**: 800x1000px (4:5 ratio)
- **About Image**: 600x800px (3:4 ratio)

### Formats
- Use `.jpg` for photographs
- Use `.png` for images requiring transparency
- Consider `.webp` for better compression (with jpg fallback)

## 🎨 Customization

### Colors

Edit CSS variables in `css/style.css`:

```css
:root {
    --primary-color: #2c2c2c;      /* Dark gray */
    --secondary-color: #8b7355;    /* Warm brown */
    --accent-color: #d4a373;       /* Light brown/gold */
    --text-primary: #1a1a1a;       /* Nearly black */
    --text-secondary: #666;         /* Medium gray */
    --bg-light: #f8f8f8;           /* Off-white */
    --bg-white: #ffffff;           /* Pure white */
}
```

### Fonts

Current fonts: **Playfair Display** (headings) and **Raleway** (body)

To change fonts, update the Google Fonts link in HTML:

```html
<link href="https://fonts.googleapis.com/css2?family=Your+Font&display=swap" rel="stylesheet">
```

Then update CSS:

```css
body {
    font-family: 'Your Font', sans-serif;
}
```

### Portfolio Items

Add or modify portfolio items in the portfolio grid section of `index.html`. Each item follows this structure:

```html
<div class="portfolio-item" data-category="projects">
    <div class="portfolio-image">
        <img src="images/your-image.jpg" alt="Description" loading="lazy">
        <div class="portfolio-overlay">
            <div class="portfolio-info">
                <h3>Project Title</h3>
                <p>Project Category</p>
                <a href="path/to/project.html" class="portfolio-link">View Project</a>
            </div>
        </div>
    </div>
</div>
```

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📱 Responsive Breakpoints

- **Desktop**: > 1200px
- **Tablet**: 768px - 1199px
- **Mobile**: < 768px
- **Small Mobile**: < 480px

## ⚡ Performance Features

- Lazy loading images for faster initial page load
- Debounced scroll events to reduce CPU usage
- CSS animations with GPU acceleration
- Optimized asset loading strategy
- Minimal JavaScript dependencies (zero external libraries)
- Efficient DOM manipulation

## 🔒 Security

- No sensitive information in code
- All external links open in secure context
- Form validation to prevent malicious input
- HTTPS recommended for deployment

## 📄 License

© 2025 Catelin Le Franc. All rights reserved.

This website template is for Catelin Le Franc's use. Please do not redistribute or use for other projects without permission.

## 🤝 Contributing

This is a personal portfolio site. If you find bugs or have suggestions, please open an issue.

## 📞 Contact

For inquiries about this website or photography services, please use the contact form on the website.

## 🙏 Acknowledgments

- Design inspiration from contemporary photography portfolios
- Icons from inline SVG
- Fonts from Google Fonts
- Color palette inspired by vintage photography aesthetics

## 📚 Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [HTML Best Practices](https://github.com/hail2u/html-best-practices)
- [CSS Guidelines](https://cssguidelin.es/)
- [JavaScript Best Practices](https://github.com/ryanmcdermott/clean-code-javascript)

---

**Built with ❤️ for showcasing photographic artistry**

For deployment instructions, see [DEPLOYMENT.md](DEPLOYMENT.md)
```
