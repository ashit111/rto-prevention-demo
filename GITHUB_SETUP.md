# GitHub Pages Setup Instructions

## Prerequisites
You need a GitHub account. If you don't have one, create it at: https://github.com/signup

## Step-by-Step Instructions

### Step 1: Configure Git (One-time setup)
Open Terminal and run these commands (replace with your info):

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Step 2: Create Repository on GitHub

1. Go to: https://github.com/new
2. Fill in:
   - **Repository name:** `rto-prevention-demo`
   - **Description:** "Working prototype of RTO Prevention Hub - Investor Demo"
   - **Visibility:** PUBLIC (must be public for free GitHub Pages)
   - **DO NOT initialize with README, .gitignore, or license**
3. Click "Create repository"

### Step 3: Link Local Repo to GitHub

After creating the repo, GitHub will show a URL like:
`https://github.com/YOUR_USERNAME/rto-prevention-demo.git`

Run these commands in Terminal:

```bash
cd /Users/ashitranjan/RTO_Prevention_Demo

# Replace YOUR_USERNAME with your actual GitHub username
git remote add origin https://github.com/YOUR_USERNAME/rto-prevention-demo.git

git branch -M main

git push -u origin main
```

**Note:** You may be asked to authenticate:
- If you have 2FA enabled, you'll need a Personal Access Token (not your password)
- To create a token: GitHub → Settings → Developer settings → Personal access tokens → Generate new token

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar under "Code and automation")
4. Under "Build and deployment":
   - **Source:** Deploy from a branch
   - **Branch:** Select `main` and `/ (root)` → Click **Save**
5. Wait 2-3 minutes

### Step 5: Access Your Live Demo

Your demo will be live at:
```
https://YOUR_USERNAME.github.io/rto-prevention-demo/
```

Share this URL with investors!

---

## Quick Reference

Once set up, to update your demo:

```bash
cd /Users/ashitranjan/RTO_Prevention_Demo
git add .
git commit -m "Update demo"
git push
```

Changes appear live in 1-2 minutes.

---

## Troubleshooting

**Problem:** Git push asks for password but rejects it
**Solution:** Use Personal Access Token instead:
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token with `repo` scope
3. Use token as password when prompted

**Problem:** 404 error on GitHub Pages URL
**Solution:**
- Wait 2-3 minutes after enabling Pages
- Check repository is PUBLIC
- Check Pages is enabled in Settings → Pages

**Problem:** Cannot push - authentication failed
**Solution:**
- Use `git remote -v` to verify remote URL
- Try HTTPS instead of SSH (or vice versa)
- Generate Personal Access Token (see above)

---

## Your Demo Components

Once live, you can share these direct links:
- Main launcher: `https://YOUR_USERNAME.github.io/rto-prevention-demo/`
- Customer checkout: `https://YOUR_USERNAME.github.io/rto-prevention-demo/customer-checkout.html`
- Hub operations: `https://YOUR_USERNAME.github.io/rto-prevention-demo/hub-operations.html`
- Hub dashboard: `https://YOUR_USERNAME.github.io/rto-prevention-demo/hub-dashboard.html`
- Customer pickup: `https://YOUR_USERNAME.github.io/rto-prevention-demo/customer-pickup.html`
- Platform dashboard: `https://YOUR_USERNAME.github.io/rto-prevention-demo/platform-dashboard.html`
- 3PL integration: `https://YOUR_USERNAME.github.io/rto-prevention-demo/3pl-integration.html`
