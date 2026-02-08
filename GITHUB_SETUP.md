# Quick GitHub Setup Guide

This guide helps you get your website on GitHub in just a few minutes.

## Prerequisites

- Git installed on your computer
- GitHub account (create free at https://github.com)

## Step-by-Step Instructions

### 1. Install Git (if not already installed)

**Windows:**
- Download from https://git-scm.com/download/win
- Run installer with default options

**Mac:**
- Open Terminal
- Type: `git --version`
- If not installed, it will prompt you to install

**Linux:**
```bash
sudo apt-get install git
```

### 2. Configure Git (First Time Only)

Open Terminal/Command Prompt and run:

```bash
# Set your name
git config --global user.name "Your Name"

# Set your email (use GitHub email)
git config --global user.email "your.email@example.com"
```

### 3. Create GitHub Repository

1. Go to https://github.com
2. Log in to your account
3. Click the **"+"** icon (top right) → **"New repository"**
4. Fill in details:
   - **Repository name**: `dr-maya-reynolds-website`
   - **Description**: Professional therapy website for Dr. Maya Reynolds
   - **Public** or **Private**: Choose based on preference
   - **DO NOT** check "Initialize with README" (you already have one)
5. Click **"Create repository"**

### 4. Upload Your Code to GitHub

**Open Terminal/Command Prompt and navigate to your project folder:**

```bash
# Example for Windows:
cd C:\Users\YourName\Documents\dr-maya-reynolds-website

# Example for Mac/Linux:
cd ~/Documents/dr-maya-reynolds-website
```

**Then run these commands one by one:**

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Professional therapy website"

# Add GitHub as remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/dr-maya-reynolds-website.git

# Rename branch to main
git branch -M main

# Push to GitHub
git push -u origin main
```

**Enter your GitHub credentials when prompted.**

### 5. Verify Upload

1. Go to your GitHub repository page
2. Refresh the page
3. You should see all your files!

### 6. Enable GitHub Pages (Make it Live)

1. In your repository, click **"Settings"**
2. Scroll down and click **"Pages"** (in left sidebar)
3. Under **"Source"**:
   - Select **"main"** branch
   - Leave folder as **"/ (root)"**
   - Click **"Save"**
4. Wait 2-5 minutes
5. Refresh the page
6. You'll see: **"Your site is published at https://YOUR_USERNAME.github.io/dr-maya-reynolds-website"**
7. Click the link to view your live website!

## 🎉 You're Done!

Your website is now:
- ✅ Backed up on GitHub
- ✅ Live on the internet
- ✅ Accessible to anyone with the link

## Making Updates

Whenever you make changes to your website:

```bash
# 1. Save your changes in VS Code

# 2. Add changed files
git add .

# 3. Commit changes
git commit -m "Description of what you changed"

# 4. Push to GitHub
git push

# Your website will update automatically in a few minutes!
```

## Common Issues & Solutions

### Issue: "git: command not found"
**Solution:** Git is not installed. Install from https://git-scm.com

### Issue: "Permission denied"
**Solution:** You need to authenticate with GitHub
- Use Personal Access Token instead of password
- Generate at: GitHub → Settings → Developer settings → Personal access tokens

### Issue: "remote origin already exists"
**Solution:** Remove existing remote first:
```bash
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/dr-maya-reynolds-website.git
```

### Issue: "Cannot push"
**Solution:** Pull first, then push:
```bash
git pull origin main --rebase
git push
```

### Issue: "GitHub Pages not working"
**Solution:** 
- Wait 5-10 minutes after enabling
- Check Settings → Pages for error messages
- Ensure index.html is in root folder

## Helpful Commands

```bash
# Check status of your files
git status

# See commit history
git log

# Undo changes before commit
git checkout -- filename.html

# See what's different
git diff

# Create a new branch
git checkout -b new-feature

# Switch branches
git checkout main
```

## Resources

- **Git Documentation**: https://git-scm.com/doc
- **GitHub Guides**: https://guides.github.com
- **GitHub Pages**: https://pages.github.com

## Need Help?

- GitHub Community: https://github.community
- Stack Overflow: https://stackoverflow.com
- Git Documentation: https://git-scm.com/doc

---

**Pro Tip:** Commit your changes frequently! Think of it as saving your work with a description of what you did.

Good commit message examples:
- ✅ "Update office hours on contact page"
- ✅ "Add new service: couples therapy"
- ✅ "Fix mobile menu not closing"
- ❌ "Fixed stuff" (too vague)
- ❌ "asdf" (not helpful)
