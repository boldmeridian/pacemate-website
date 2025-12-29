# Deploy PaceMate Website to Netlify - Step-by-Step Guide

This guide will walk you through deploying your PaceMate website to Netlify in about 10 minutes.

## Prerequisites

- GitHub account (free at github.com)
- Netlify account (free at netlify.com)
- Your website files (already created ✓)

---

## Step 1: Push Website to GitHub

### 1.1 Create a GitHub Repository

1. Go to [github.com](https://github.com) and log in
2. Click the **+** icon in the top-right corner
3. Select **New repository**
4. Fill in the details:
   - **Repository name:** `pacemate-website`
   - **Description:** "PaceMate landing page website"
   - **Visibility:** Public (required for free Netlify)
   - **Initialize with:** Skip (we'll add files manually)
5. Click **Create repository**

### 1.2 Upload Website Files to GitHub

**Option A: Using Git Command Line (Recommended)**

```bash
# Navigate to your website folder
cd /home/ubuntu/pacemate-website

# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: PaceMate website"

# Add remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/pacemate-website.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Option B: Using GitHub Web Interface (Easier)**

1. Go to your new repository on GitHub
2. Click **Add file** → **Upload files**
3. Drag and drop all files from `/home/ubuntu/pacemate-website/`:
   - `index.html`
   - `privacy.html`
   - `terms.html`
   - `contact.html`
   - `README.md`
4. Add commit message: "Initial commit: PaceMate website"
5. Click **Commit changes**

---

## Step 2: Connect Netlify to GitHub

### 2.1 Sign Up for Netlify

1. Go to [netlify.com](https://netlify.com)
2. Click **Sign up**
3. Click **GitHub** (to sign up with your GitHub account)
4. Authorize Netlify to access your GitHub account
5. Click **Authorize netlify**

### 2.2 Create New Site from Git

1. After signing in, you'll see the Netlify dashboard
2. Click **New site from Git** (or **Add new site**)
3. Click **GitHub** (to connect your GitHub repository)
4. You may need to authorize Netlify again - click **Authorize Netlify by Netlify**

---

## Step 3: Select Your Repository

### 3.1 Choose Repository

1. Search for `pacemate-website` in the search box
2. Click on your `pacemate-website` repository
3. You should see it highlighted

### 3.2 Configure Build Settings

1. **Branch to deploy:** Select `main` (default)
2. **Build command:** Leave blank (we don't need to build anything)
3. **Publish directory:** Leave blank or enter `.` (current directory)
4. Click **Deploy site**

---

## Step 4: Wait for Deployment

Netlify will now build and deploy your website:

1. You'll see a deployment log showing progress
2. Wait for the message: **"Site is live"** ✓
3. Your site will be assigned a random URL like: `https://pacemate-abc123.netlify.app`

---

## Step 5: Configure Custom Domain (Optional but Recommended)

### 5.1 Add Custom Domain

1. In Netlify dashboard, go to your site
2. Click **Domain settings**
3. Click **Add domain**
4. Enter your domain: `pacemate.app` (or your domain)
5. Click **Verify**

### 5.2 Update DNS Records

1. Go to your domain registrar (GoDaddy, Namecheap, etc.)
2. Find DNS settings
3. Add the DNS records provided by Netlify:
   - Type: `CNAME`
   - Name: `www`
   - Value: (provided by Netlify)
4. Wait 24-48 hours for DNS to propagate

### 5.3 Enable SSL (HTTPS)

1. Back in Netlify, go to **Domain settings**
2. Scroll to **HTTPS**
3. Click **Enable HTTPS** (Netlify provides free SSL)
4. Wait for certificate to be issued (usually 1-5 minutes)

---

## Step 6: Update Website Links

Before your site goes live, update these links in your HTML files:

### 6.1 Update App Store Links

In `index.html` and `contact.html`, find and replace:

**Before:**
```html
<a href="https://apps.apple.com/app/pacemate" class="btn btn-primary">Download on iOS</a>
<a href="https://play.google.com/store/apps/details?id=space.manus.pacemate" class="btn btn-primary">Get on Android</a>
```

**After:**
```html
<a href="https://apps.apple.com/us/app/pacemate/id1234567890" class="btn btn-primary">Download on iOS</a>
<a href="https://play.google.com/store/apps/details?id=space.manus.pacemate" class="btn btn-primary">Get on Android</a>
```

(Replace with actual App Store links once your apps are published)

### 6.2 Update Email Addresses

In `contact.html`, replace:
- `support@pacemate.app` → Your actual support email
- `privacy@pacemate.app` → Your actual privacy email
- `legal@pacemate.app` → Your actual legal email

### 6.3 Update Website URLs

Replace all instances of `https://pacemate.app` with your actual domain.

### 6.4 Commit Changes

```bash
cd /home/ubuntu/pacemate-website
git add .
git commit -m "Update links and email addresses"
git push
```

Netlify will automatically redeploy your site with the changes.

---

## Step 7: Test Your Website

1. Visit your Netlify URL: `https://pacemate-abc123.netlify.app`
2. Or your custom domain: `https://pacemate.app`
3. Test all pages:
   - ✓ Homepage loads correctly
   - ✓ All links work
   - ✓ Navigation works
   - ✓ Responsive on mobile
   - ✓ Privacy policy displays
   - ✓ Terms of service displays
   - ✓ Contact page displays

---

## Step 8: Use in App Store Listings

Once your website is live, add these URLs to your app store listings:

**iOS App Store:**
- Privacy Policy URL: `https://pacemate.app/privacy.html`
- Support URL: `https://pacemate.app/contact.html`

**Google Play Store:**
- Privacy Policy URL: `https://pacemate.app/privacy.html`
- Support URL: `https://pacemate.app/contact.html`

---

## Troubleshooting

### Site shows "404 Not Found"

**Solution:** Make sure your files are in the root directory of your GitHub repository, not in a subfolder.

### Site doesn't update after pushing changes

**Solution:** 
1. Wait 1-2 minutes for Netlify to redeploy
2. Check the **Deploys** tab in Netlify dashboard
3. Clear your browser cache (Ctrl+Shift+Delete)

### Custom domain not working

**Solution:**
1. Wait 24-48 hours for DNS to propagate
2. Check DNS records are correct in your registrar
3. Use [MXToolbox](https://mxtoolbox.com/dnsLookup.aspx) to verify DNS

### HTTPS not working

**Solution:**
1. Wait 5-10 minutes for SSL certificate to be issued
2. Check **Domain settings** → **HTTPS** status
3. Try accessing with `https://` instead of `http://`

---

## Next Steps

1. ✓ Deploy website to Netlify
2. ✓ Set up custom domain
3. ✓ Update app store links
4. ✓ Submit app to iOS App Store
5. ✓ Submit app to Google Play Store
6. ✓ Monitor support emails

---

## Support

- **Netlify Help:** https://docs.netlify.com
- **GitHub Help:** https://docs.github.com
- **PaceMate Support:** support@pacemate.app

---

**You're all set! Your website will be live in minutes. 🚀**
