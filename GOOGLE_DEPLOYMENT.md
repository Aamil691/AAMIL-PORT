# 🚀 Google Deployment Guide for Aamil's Portfolio

This guide will help you deploy your portfolio website to various Google platforms.

## 📱 Option 1: Google Sites (Easiest - Free)

### Step 1: Prepare Your Files
1. **Zip your portfolio folder**:
   - Right-click on your portfolio folder
   - Select "Send to" → "Compressed (zipped) folder"
   - This creates a `.zip` file

### Step 2: Upload to Google Drive
1. Go to [drive.google.com](https://drive.google.com)
2. Click "New" → "File upload"
3. Select your portfolio `.zip` file
4. Wait for upload to complete

### Step 3: Create Google Site
1. Go to [sites.google.com](https://sites.google.com)
2. Click "Create" → "New site"
3. Choose a template (or start blank)
4. Name your site (e.g., "Aamil Rais Portfolio")

### Step 4: Embed Your Portfolio
1. **Method A - Iframe Embed**:
   - Click the "+" button to add content
   - Select "Embed" → "Embed code"
   - Use this code (replace with your Drive link):
   ```html
   <iframe src="YOUR_GOOGLE_DRIVE_LINK" width="100%" height="800px" frameborder="0"></iframe>
   ```

2. **Method B - Direct HTML**:
   - Copy the content from your `index.html`
   - Paste it into a "Text" element
   - Add CSS and JavaScript separately

### Step 5: Publish
1. Click "Publish" in the top right
2. Choose your URL (e.g., `sites.google.com/view/aamil-portfolio`)
3. Click "Publish"

---

## 🔥 Option 2: Firebase Hosting (Professional - Free Tier)

### Step 1: Install Firebase CLI
```bash
npm install -g firebase-tools
```

### Step 2: Login to Firebase
```bash
firebase login
```

### Step 3: Initialize Project
```bash
# Create a new directory for deployment
mkdir portfolio-deploy
cd portfolio-deploy

# Copy your portfolio files here
# Then initialize Firebase
firebase init hosting
```

### Step 4: Configure Firebase
When prompted:
- **Select project**: Create new project or use existing
- **Public directory**: `.` (current directory)
- **Single-page app**: `No`
- **Overwrite index.html**: `No`

### Step 5: Deploy
```bash
firebase deploy
```

### Step 6: Get Your URL
Firebase will give you a URL like:
`https://your-project-id.web.app`

---

## ☁️ Option 3: Google Cloud Platform (Advanced - Paid)

### Step 1: Set Up Google Cloud
1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Create a new project
3. Enable Cloud Storage and Cloud CDN

### Step 2: Upload Files
1. Go to Cloud Storage
2. Create a new bucket
3. Upload your portfolio files
4. Make bucket public

### Step 3: Configure Website
1. Go to bucket settings
2. Set main page: `index.html`
3. Set error page: `index.html` (for SPA routing)

### Step 4: Get Your URL
Your site will be available at:
`https://storage.googleapis.com/YOUR_BUCKET_NAME/index.html`

---

## 🌐 Option 4: Google Domains + Any Hosting

### Step 1: Buy Domain
1. Go to [domains.google](https://domains.google)
2. Search for your desired domain
3. Purchase (e.g., `aamilrais.com`)

### Step 2: Choose Hosting
- **Firebase Hosting** (Recommended)
- **Netlify** (Drag & Drop)
- **GitHub Pages** (Free)

### Step 3: Connect Domain
1. Go to your hosting provider's DNS settings
2. Add your Google Domain
3. Update nameservers if required

---

## 📋 Quick Deployment Checklist

### Before Deploying:
- [ ] Test website locally
- [ ] Check all links work
- [ ] Verify mobile responsiveness
- [ ] Optimize images (if any)
- [ ] Test contact form

### After Deploying:
- [ ] Test website on deployed URL
- [ ] Check mobile and desktop views
- [ ] Verify all sections load properly
- [ ] Test contact form functionality
- [ ] Share your portfolio URL!

---

## 🎯 Recommended Approach for Beginners

1. **Start with Google Sites** (Free, Easy)
2. **Upgrade to Firebase** (Free, Professional)
3. **Add custom domain** (Optional, Professional)

---

## 🆘 Troubleshooting

### Common Issues:

**Google Sites:**
- If HTML doesn't render: Use iframe method
- If styling breaks: Add CSS separately

**Firebase:**
- If deployment fails: Check file permissions
- If site doesn't load: Verify public directory setting

**General:**
- Clear browser cache
- Check browser console for errors
- Verify all files are uploaded

---

## 📞 Need Help?

- **Email**: aamilrais34@gmail.com
- **LinkedIn**: [linkedin.com/in/aamil-rais](https://linkedin.com/in/aamil-rais)
- **GitHub**: [github.com/Aamil691](https://github.com/Aamil691)

---

**Happy Deploying! 🚀**

*Your portfolio will be live on the web in no time!*
