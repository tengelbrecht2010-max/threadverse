# 🚀 THREADVERSE — Publish to Netlify via GitHub
### Complete Step-by-Step Guide

---

## 📁 Project Structure

```
threadverse/
├── index.html          ← Your main website
├── admin/
│   └── index.html      ← Admin panel (access at /admin)
└── README.md           ← This file
```

---

## STEP 1 — Create a GitHub Account

1. Go to **https://github.com**
2. Click **"Sign up"** (top right)
3. Enter your email, create a password, and choose a username
4. Verify your email address

---

## STEP 2 — Create a New Repository on GitHub

1. Once logged in, click the **"+"** icon (top right) → **"New repository"**
2. Fill in:
   - **Repository name:** `threadverse` (or any name you like)
   - **Description:** `My T-shirt store` (optional)
   - Set to **Public** (required for free Netlify deployment)
   - ✅ Check **"Add a README file"**
3. Click **"Create repository"**

---

## STEP 3 — Upload Your Files to GitHub

### Option A — Upload via Browser (easiest, no coding needed)

1. Inside your new repository, click **"Add file"** → **"Upload files"**
2. Drag and drop your `index.html` file into the upload area
3. Click **"Commit changes"** (green button at the bottom)
4. Now create the admin folder:
   - Click **"Add file"** → **"Create new file"**
   - In the filename box, type: `admin/index.html`
   - Paste the entire contents of your `admin/index.html` file into the editor
   - Click **"Commit new file"**

### Option B — Upload via GitHub Desktop (recommended for future edits)

1. Download **GitHub Desktop** from https://desktop.github.com
2. Install and sign in with your GitHub account
3. Click **"Clone a repository"** → find `threadverse` → choose a local folder
4. Copy your `index.html` and `admin/` folder into that local folder
5. In GitHub Desktop you'll see the files appear under "Changes"
6. Add a summary like `"Initial upload"` → click **"Commit to main"**
7. Click **"Push origin"** (top bar)

---

## STEP 4 — Create a Netlify Account

1. Go to **https://netlify.com**
2. Click **"Sign up"** → choose **"Sign up with GitHub"** (easiest!)
3. Authorize Netlify to access your GitHub
4. You'll land on the Netlify dashboard

---

## STEP 5 — Deploy from GitHub to Netlify

1. On the Netlify dashboard, click **"Add new site"** → **"Import an existing project"**
2. Click **"Deploy with GitHub"**
3. Authorize Netlify to access your repositories if prompted
4. **Find and click** your `threadverse` repository
5. Configure the deploy settings:
   - **Branch to deploy:** `main`
   - **Base directory:** *(leave blank)*
   - **Build command:** *(leave blank — it's a plain HTML site)*
   - **Publish directory:** *(leave blank or type `.`)*
6. Click **"Deploy site"**

---

## STEP 6 — Wait for Deploy (about 30 seconds)

1. Netlify will show a progress bar — wait for it to say **"Published"**
2. You'll get a random URL like: `https://amazing-einstein-abc123.netlify.app`
3. Click it — **your site is live!** 🎉

---

## STEP 7 — Set a Custom Site Name (Free)

1. In Netlify, go to **Site settings** → **General** → **Site details**
2. Click **"Change site name"**
3. Type something like: `threadverse-store`
4. Your new URL will be: `https://threadverse-store.netlify.app`

---

## STEP 8 — Connect a Custom Domain (Optional, e.g. threadverse.co.za)

1. Go to **Site settings** → **Domain management** → **Add custom domain**
2. Type your domain (e.g. `threadverse.co.za`) → click **Verify**
3. Follow the DNS instructions to point your domain to Netlify
4. Netlify will auto-generate a free SSL certificate (HTTPS) ✅

---

## 🔄 How to Update Your Site Later

Every time you change a file and push to GitHub, Netlify **automatically re-deploys** within seconds.

**With GitHub Desktop:**
1. Edit your files locally
2. Open GitHub Desktop → you'll see the changes
3. Write a commit message → **"Commit to main"** → **"Push origin"**
4. Netlify detects the push and redeploys automatically ✅

**Via Browser:**
1. Go to your repo on GitHub.com
2. Click the file you want to edit → click the ✏️ pencil icon
3. Make your changes → **"Commit changes"**
4. Netlify auto-redeploys ✅

---

## 📌 Your Important URLs

| What | URL |
|------|-----|
| Your Website | `https://your-site-name.netlify.app` |
| Admin Panel | `https://your-site-name.netlify.app/admin` |
| GitHub Repo | `https://github.com/yourusername/threadverse` |
| Netlify Dashboard | `https://app.netlify.com` |

---

## 🛡️ Protect Your Admin Panel (Important!)

Your admin panel at `/admin` is currently public. To password-protect it on Netlify:

1. In your project folder, create a file called `netlify.toml` with this content:

```toml
[[headers]]
  for = "/admin/*"
  [headers.values]
    X-Frame-Options = "DENY"
```

2. Then in **Netlify → Site settings → Access control → Password protection**
   - Enable site-wide password (free on Netlify Starter), or
   - Use **Netlify Identity** for proper login (free tier available)

---

## ❓ Troubleshooting

| Problem | Fix |
|---------|-----|
| Site shows 404 | Make sure `index.html` is at the root, not inside a subfolder |
| Admin not loading | Check that `admin/index.html` exists in your repo |
| Changes not showing | Hard refresh: `Ctrl+Shift+R` (Windows) / `Cmd+Shift+R` (Mac) |
| Deploy failed | Check the deploy log in Netlify for errors |

---

*Made with ❤️ — THREADVERSE // WEAR YOUR UNIVERSE*
