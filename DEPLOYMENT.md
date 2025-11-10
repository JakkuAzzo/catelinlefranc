# Deployment Guide for GitHub Pages

This guide will help you deploy your Catelin Le Franc photography portfolio to GitHub Pages.

## Prerequisites

- A GitHub account
- Git installed on your computer
- All your images added to the `images/` directory

## Step-by-Step Deployment

### 1. Prepare Your Repository

First, make sure all your content is ready:
- [ ] All images are in the `images/` directory
- [ ] Images are optimized (compressed)
- [ ] Content in `index.html` is updated with correct information
- [ ] Contact information is correct

### 2. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top-right corner
3. Select "New repository"
4. Name your repository (e.g., `photography-portfolio` or `catelinlefranc`)
5. Make it **Public** (required for free GitHub Pages)
6. **Do NOT** initialize with README, .gitignore, or license (we already have these)
7. Click "Create repository"

### 3. Initialize Git and Push Your Code

Open terminal/command prompt in your project directory and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create your first commit
git commit -m "Initial commit: Photography portfolio website"

# Rename branch to main (if needed)
git branch -M main

# Add your GitHub repository as remote
# Replace YOUR-USERNAME and YOUR-REPO-NAME with actual values
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub
git push -u origin main
```

### 4. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** (gear icon)
3. Scroll down to **Pages** in the left sidebar
4. Under "Source", select **main** branch
5. Keep the folder as **/ (root)**
6. Click **Save**

### 5. Wait for Deployment

- GitHub will build and deploy your site (usually takes 1-3 minutes)
- You'll see a message: "Your site is ready to be published at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`"
- Once deployed, the message will change to: "Your site is published at..."

### 6. Access Your Website

Your website will be available at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

## Custom Domain (Optional)

If you want to use a custom domain like `www.catelinlefranc.com`:

1. Purchase a domain from a registrar (Namecheap, Google Domains, etc.)
2. In your repository, create a file named `CNAME` (no extension) in the root directory
3. Add your domain to this file: `www.catelinlefranc.com`
4. Configure DNS settings with your domain registrar:
   - Add a CNAME record pointing to `YOUR-USERNAME.github.io`
5. In GitHub Pages settings, enter your custom domain
6. Enable "Enforce HTTPS" after DNS propagates (24-48 hours)

### DNS Configuration Example:
```
Type:  CNAME
Name:  www
Value: YOUR-USERNAME.github.io
TTL:   3600
```

For apex domain (without www):
```
Type:  A
Name:  @
Value: 185.199.108.153
       185.199.109.153
       185.199.110.153
       185.199.111.153
```

## Updating Your Website

After making changes:

```bash
# Check what files changed
git status

# Add changed files
git add .

# Commit with a message
git commit -m "Update portfolio images and content"

# Push to GitHub
git push
```

Your site will automatically update within a few minutes.

## Troubleshooting

### Site not loading
- Wait 5-10 minutes after first deployment
- Clear your browser cache
- Try incognito/private browsing mode

### Images not showing
- Check image paths in HTML (use relative paths)
- Ensure images are pushed to GitHub
- Check file names match exactly (case-sensitive)

### 404 Error
- Verify the URL matches: `https://USERNAME.github.io/REPO-NAME/`
- Check that index.html is in the root directory
- Ensure GitHub Pages is enabled in settings

### CSS/JS not loading
- Check file paths in HTML
- Ensure css/ and js/ folders are in root directory
- Verify files are pushed to GitHub

## Performance Tips

1. **Optimize Images**:
   - Use tools like TinyPNG, Squoosh, or ImageOptim
   - Target: <200KB for portfolio images
   - Consider WebP format with JPG fallback

2. **Enable Caching**:
   - GitHub Pages automatically handles this

3. **Monitor Performance**:
   - Use Google PageSpeed Insights
   - Test on multiple devices

## Security

- Never commit sensitive information (passwords, API keys, emails)
- Use contact forms that don't expose your email
- Consider using services like Formspree for forms

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Custom Domain Setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)

## Support

If you encounter issues:
1. Check the [GitHub Status](https://www.githubstatus.com/)
2. Review [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
3. Search [GitHub Community](https://github.community/)

---

**Need help?** Create an issue in your repository or consult the GitHub documentation.
