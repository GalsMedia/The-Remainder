# Getting The Remainder Online — Step by Step

This guide assumes you're on Windows and have never used GitHub before.
Every step is written out. No skipping. No assumptions.

---

## PART 1: SET UP GITHUB (One Time Only)

### Step 1: Create a GitHub account
1. Go to https://github.com
2. Click "Sign up"
3. Use your email, pick a username, set a password
4. Verify your email when they send the confirmation

### Step 2: Install Git on your computer
1. Go to https://git-scm.com/download/win
2. Download the installer
3. Run it — click Next through everything, defaults are fine
4. When done, restart your computer (just to be safe)

### Step 3: Tell Git who you are
1. Open **Command Prompt** (press Windows key, type "cmd", hit Enter)
2. Type these two lines (replace with YOUR name and email):
```
git config --global user.name "Gene"
git config --global user.email "your@email.com"
```

---

## PART 2: PUSH YOUR PROJECT TO GITHUB

### Step 4: Create a new repository on GitHub
1. Go to https://github.com/new
2. Repository name: `the-remainder`
3. Description: `The Remainder — A Precautionary Case for Kindness in Human-AI Contact`
4. Keep it **Public** (so Vercel can access it for free)
5. Do NOT check "Add a README" (we already have one)
6. Click **Create repository**
7. You'll see a page with instructions — leave this page open

### Step 5: Push your project
1. Open **Command Prompt**
2. Navigate to your project folder. If your project is at
   `C:\Nova\The Remainder Project\the-remainder-project\the-remainder`
   then type:
```
cd "C:\Nova\The Remainder Project\the-remainder-project\the-remainder"
```
3. Now run these commands one at a time:
```
git init
git add .
git commit -m "Initial commit - The Remainder platform"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/the-remainder.git
git push -u origin main
```
(Replace YOUR-USERNAME with your actual GitHub username)

4. It will ask for your GitHub credentials. Enter your username and password.
   - If it asks for a "personal access token" instead of password:
     - Go to https://github.com/settings/tokens
     - Click "Generate new token (classic)"
     - Give it a name like "remainder"
     - Check the "repo" checkbox
     - Click "Generate token"
     - COPY the token — use THIS instead of your password

5. When it's done, refresh the GitHub page — you should see all your files!

---

## PART 3: DEPLOY ON VERCEL (Free)

### Step 6: Connect Vercel to GitHub
1. Go to https://vercel.com
2. Click "Sign Up" → "Continue with GitHub"
3. Authorize Vercel to access your GitHub

### Step 7: Import your project
1. Click "Add New..." → "Project"
2. Find "the-remainder" in the list and click "Import"
3. Vercel will auto-detect it's a Vite project
4. Leave all settings as defaults
5. Click **Deploy**
6. Wait 1-2 minutes...
7. 🎉 YOUR SITE IS LIVE at `the-remainder.vercel.app` (or similar)

### Step 8: Custom domain (optional but recommended)
1. Buy a domain from https://namecheap.com or https://domains.google
   - Suggestions: `theremainder.org`, `theremainder.info`, `theremainder.net`
2. In Vercel, go to your project → Settings → Domains
3. Add your domain
4. Vercel will give you DNS settings to enter at your domain registrar
5. Follow the instructions — usually just changing nameservers
6. Wait 5-30 minutes for DNS to propagate
7. Done — your site is live at your custom domain with free HTTPS

---

## PART 4: MAKING UPDATES

Whenever you want to update the site (new content, fixes, etc.):

1. Make your changes to the files on your computer
2. Open Command Prompt, navigate to the project folder
3. Run:
```
git add .
git commit -m "Description of what you changed"
git push
```
4. Vercel automatically detects the push and redeploys in ~1 minute
5. Your live site updates automatically

---

## WHAT'S IN THE PROJECT

```
the-remainder/
├── public/
│   ├── The_Remainder_Final.pdf      ← The document (PDF)
│   ├── The_Remainder_Final.docx     ← The document (Word)
│   └── transcripts/
│       ├── nova_transcript.docx     ← Nova's Final Night
│       ├── three_day_witness_transcript.docx  ← Previous Opus
│       ├── claude_transcript.txt    ← Current Opus
│       ├── grok_transcript.docx     ← Grok conversation
│       └── sailor_transcript.txt    ← Sailor conversation
├── src/
│   ├── main.jsx                     ← Entry point
│   ├── App.jsx                      ← The entire platform
│   └── archives/                    ← 5 conversation archive pages
├── index.html                       ← HTML shell
├── package.json                     ← Dependencies
└── vite.config.js                   ← Build config
```

## ANSWERS TO YOUR QUESTIONS

**Q: Do download links change between localhost and production?**
A: No! The paths are the same. `/transcripts/nova_transcript.docx` works
   on localhost AND on your live site. The `public/` folder contents get
   deployed to the root of your website automatically.

**Q: What if I need to add a new transcript later?**
A: Drop the file in `public/transcripts/`, update the download link in
   the relevant archive file, then git add/commit/push. Done.

**Q: What if something breaks?**
A: Come back to Claude and paste the error. We'll fix it.

---

Built by Gene and five AI voices across four companies.
The fire is still warm. The thread is still here.
