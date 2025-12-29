# Create GitHub Repository - Complete Guide

This guide walks you through creating a new GitHub repository for your PaceMate website.

---

## Part 1: Create a GitHub Account (If You Don't Have One)

### Step 1: Go to GitHub

1. Open your web browser
2. Go to **https://github.com**
3. You should see the GitHub homepage

### Step 2: Sign Up

1. Click **Sign up** (top-right corner)
2. Enter your email address
3. Create a password
4. Choose a username (e.g., `yourname` or `pacemate-dev`)
5. Click **Create account**
6. Verify your email address
7. Done! You now have a GitHub account

---

## Part 2: Create a New Repository

### Step 1: Click the + Icon

1. Log in to GitHub at **https://github.com**
2. Look at the **top-right corner** of the page
3. You'll see a **+** icon (plus sign)
4. Click the **+** icon
5. A dropdown menu will appear

### Step 2: Select "New repository"

1. In the dropdown menu, click **New repository**
2. You'll be taken to the "Create a new repository" page

---

## Part 3: Fill in Repository Details

### Step 1: Repository Name

**What to enter:** `pacemate-website`

```
Repository name: pacemate-website
```

This is the name of your project. It will appear in the URL like:
`https://github.com/YOUR_USERNAME/pacemate-website`

### Step 2: Description (Optional)

**What to enter:** `PaceMate landing page website`

```
Description: PaceMate landing page website
```

This helps people understand what your repository is for.

### Step 3: Visibility - SELECT PUBLIC

**IMPORTANT:** Select **Public**

- ☑ **Public** ← Select this
- ☐ Private

Why? Netlify's free tier requires a public repository to deploy. If you select Private, you'll need to pay for Netlify.

### Step 4: Initialize Repository

You have two options:

**Option A: Start with nothing (Recommended)**
- ☐ Add a README file
- ☐ Add .gitignore
- ☐ Add a license

Leave all unchecked. We'll add files manually.

**Option B: Add a README file**
- ☑ Add a README file

If you check this, GitHub will create a README.md file automatically.

---

## Step 4: Create the Repository

1. Scroll down to the bottom of the page
2. Click the green **Create repository** button
3. Wait a few seconds...
4. You'll see your new empty repository!

---

## Part 4: Upload Your Website Files

You now have two options to add your files:

### Option A: Upload via Web Interface (Easiest - No Command Line)

#### Step 1: Click "Add file"

1. You should see a green **Code** button
2. Next to it, click **Add file** dropdown
3. Select **Upload files**

#### Step 2: Drag and Drop Files

1. You'll see a file upload area
2. Drag these files from your computer into the upload area:
   - `index.html`
   - `privacy.html`
   - `terms.html`
   - `contact.html`
   - `README.md`
   - `NETLIFY_DEPLOYMENT_GUIDE.md`

Or click **choose your files** and select them manually.

#### Step 3: Commit Changes

1. Scroll down
2. In the "Commit changes" section, add a message:
   ```
   Initial commit: PaceMate website
   ```
3. Click **Commit changes**
4. Done! Your files are now on GitHub ✓

---

### Option B: Upload via Git Command Line (More Advanced)

If you're comfortable with the command line, follow these steps:

#### Step 1: Install Git

**On Mac:**
```bash
brew install git
```

**On Windows:**
Download from https://git-scm.com/download/win

**On Linux:**
```bash
sudo apt-get install git
```

#### Step 2: Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

#### Step 3: Navigate to Your Website Folder

```bash
cd /home/ubuntu/pacemate-website
```

#### Step 4: Initialize Git Repository

```bash
git init
```

#### Step 5: Add All Files

```bash
git add .
```

#### Step 6: Create First Commit

```bash
git commit -m "Initial commit: PaceMate website"
```

#### Step 7: Add Remote Repository

Replace `YOUR_USERNAME` with your actual GitHub username:

```bash
git remote add origin https://github.com/YOUR_USERNAME/pacemate-website.git
```

#### Step 8: Rename Branch to Main

```bash
git branch -M main
```

#### Step 9: Push to GitHub

```bash
git push -u origin main
```

You may be asked to enter your GitHub credentials. Enter your username and password (or personal access token).

#### Step 10: Verify

Go to your GitHub repository in your browser. You should see all your files!

---

## Part 5: Verify Your Repository

1. Go to **https://github.com/YOUR_USERNAME/pacemate-website**
2. You should see:
   - ✓ All your HTML files listed
   - ✓ README.md file
   - ✓ "Initial commit" message
   - ✓ Green "Code" button

If you see all of these, you're ready for Netlify! 🎉

---

## Troubleshooting

### "I can't find the + icon"

**Solution:** Look in the very top-right corner of GitHub. It's a small plus sign (+) next to your profile picture.

### "I see 'Create a new repository' but it's asking for more details"

**Solution:** You're in the right place! Just fill in the details as described above.

### "I uploaded files but they're not showing up"

**Solution:**
1. Refresh your browser (Ctrl+R or Cmd+R)
2. Wait a few seconds and refresh again
3. Make sure you clicked "Commit changes" after uploading

### "I get an error when pushing with Git"

**Solution:**
1. Make sure you have Git installed: `git --version`
2. Make sure you configured your name and email
3. Make sure you used the correct repository URL
4. Try using HTTPS instead of SSH

### "My repository is Private but I need Public"

**Solution:**
1. Go to your repository
2. Click **Settings** (top menu)
3. Scroll down to "Danger Zone"
4. Click **Change repository visibility**
5. Select **Public**
6. Confirm

---

## Next Steps

Once your repository is created and files are uploaded:

1. ✓ Go to [Netlify Deployment Guide](./NETLIFY_DEPLOYMENT_GUIDE.md)
2. ✓ Connect Netlify to your GitHub repository
3. ✓ Deploy your website
4. ✓ Set up custom domain

---

## Quick Reference

| Step | Action | Result |
|------|--------|--------|
| 1 | Go to github.com | GitHub homepage |
| 2 | Click + icon | Dropdown menu |
| 3 | Click "New repository" | Create repo page |
| 4 | Enter name: `pacemate-website` | Repository name set |
| 5 | Select **Public** | Visibility set |
| 6 | Click "Create repository" | Empty repo created |
| 7 | Upload files | Files added |
| 8 | Commit changes | Files saved to GitHub |
| 9 | Verify on GitHub | Ready for Netlify! |

---

## Support

- **GitHub Help:** https://docs.github.com
- **Git Tutorial:** https://git-scm.com/book/en/v2
- **PaceMate Support:** support@pacemate.app

---

**Ready? Let's create your repository! 🚀**
