# Push Updated Files to GitHub

This guide shows you how to push your updated website files to GitHub using Git.

---

## Prerequisites

- Git installed on your computer
- GitHub account
- Your `pacemate-website` repository already created
- Updated files ready to push

---

## Step 1: Install Git (If You Don't Have It)

### Check if Git is Installed

Open your terminal/command prompt and type:

```bash
git --version
```

If you see a version number (like `git version 2.40.0`), you have Git installed. Skip to Step 2.

If you get an error, install Git:

**On Mac:**
```bash
brew install git
```

**On Windows:**
Download from: https://git-scm.com/download/win

**On Linux:**
```bash
sudo apt-get install git
```

---

## Step 2: Configure Git (First Time Only)

Open your terminal and run these commands (replace with your info):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@gmail.com"
```

Example:
```bash
git config --global user.name "John Doe"
git config --global user.email "john@example.com"
```

---

## Step 3: Navigate to Your Website Folder

Open your terminal and navigate to your website folder:

```bash
cd /home/ubuntu/pacemate-website
```

Or on Windows:
```bash
cd C:\Users\YourName\pacemate-website
```

---

## Step 4: Check Git Status

See what files have changed:

```bash
git status
```

You should see:
- `index.html` (modified)
- `contact.html` (modified)
- `README.md` (modified)

---

## Step 5: Add Files to Staging Area

Add all changed files:

```bash
git add .
```

Or add specific files:
```bash
git add index.html contact.html README.md
```

---

## Step 6: Create a Commit

Create a commit with a descriptive message:

```bash
git commit -m "Update: Single support email and remove free advertising"
```

You should see output like:
```
[main abc1234] Update: Single support email and remove free advertising
 3 files changed, 15 insertions(+), 8 deletions(-)
```

---

## Step 7: Push to GitHub

Push your changes to GitHub:

```bash
git push origin main
```

You may be asked to enter your GitHub credentials:
- **Username:** Your GitHub username
- **Password:** Your GitHub personal access token (or password if using HTTPS)

---

## Step 8: Verify on GitHub

1. Go to your GitHub repository: `https://github.com/YOUR_USERNAME/pacemate-website`
2. You should see:
   - ✓ Updated commit message
   - ✓ "3 files changed" indicator
   - ✓ Latest files showing your changes

---

## Step 9: Netlify Auto-Deploys

If you've already connected Netlify to GitHub:

1. Netlify will automatically detect the changes
2. It will rebuild and redeploy your website
3. Check your Netlify dashboard for deployment status
4. Your website will be updated in 1-2 minutes

---

## Troubleshooting

### "fatal: not a git repository"

**Problem:** You're not in the right folder

**Solution:**
```bash
cd /home/ubuntu/pacemate-website
git status
```

### "fatal: The current branch main has no upstream branch"

**Problem:** First time pushing to this branch

**Solution:**
```bash
git push -u origin main
```

### "Authentication failed"

**Problem:** Wrong credentials

**Solution:**
1. If using HTTPS, you need a Personal Access Token (not your password)
2. Go to GitHub Settings → Developer settings → Personal access tokens
3. Create a new token with `repo` permissions
4. Use the token as your password

Or use SSH instead:
```bash
git remote set-url origin git@github.com:YOUR_USERNAME/pacemate-website.git
```

### "Please tell me who you are"

**Problem:** Git user not configured

**Solution:**
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@gmail.com"
```

### Changes not showing on GitHub

**Solution:**
1. Wait 30 seconds and refresh GitHub
2. Check `git status` to see if there are uncommitted changes
3. Try pushing again: `git push origin main`

### Website not updating on Netlify

**Solution:**
1. Check Netlify dashboard → Deploys tab
2. Look for the latest deployment
3. If it failed, click on it to see error logs
4. Common issues: Wrong build settings, missing files
5. Try manually triggering a deploy in Netlify

---

## Quick Command Reference

```bash
# Check status
git status

# Add files
git add .

# Commit
git commit -m "Your message here"

# Push to GitHub
git push origin main

# View commit history
git log

# See what changed
git diff
```

---

## What Happens Next

1. ✓ Files pushed to GitHub
2. ✓ Netlify detects changes
3. ✓ Netlify rebuilds website
4. ✓ Website updates automatically
5. ✓ Your changes go live!

---

## Support

- **Git Help:** https://git-scm.com/book
- **GitHub Help:** https://docs.github.com
- **Netlify Help:** https://docs.netlify.com

---

**Ready to push? Run the commands above and your website will be updated! 🚀**
