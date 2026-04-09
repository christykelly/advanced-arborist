# GitHub Setup Checklist - Advanced Arborist LLC

## 1. Create the GitHub Repository
- [ ] Create a new repository (e.g., `theflyingb/advanced-arborist`)
- [ ] Push all files from this folder to the repo

## 2. Update Decap CMS Config
- [ ] Open `admin/config.yml`
- [ ] Change `repo: GITHUB_USERNAME/REPO_NAME` to your actual repo (e.g., `theflyingb/advanced-arborist`)
- [ ] Commit and push the change

## 3. Enable GitHub Pages
- [ ] Go to repo Settings > Pages
- [ ] Under "Source," select **Deploy from a branch**
- [ ] Select **main** branch and **/ (root)** folder
- [ ] Click Save
- [ ] Wait a minute, then verify the site loads at `https://YOURUSERNAME.github.io/REPONAME/`

## 4. Connect Custom Domain
- [ ] In repo Settings > Pages > Custom domain, enter your domain (e.g., `wearetreepeople.com`)
- [ ] Add these DNS records at your domain registrar:
  - **A records** pointing to GitHub Pages IPs:
    - `185.199.108.153`
    - `185.199.109.153`
    - `185.199.110.153`
    - `185.199.111.153`
  - **CNAME record**: `www` pointing to `YOURUSERNAME.github.io`
- [ ] Check "Enforce HTTPS" once DNS propagates (can take up to 24 hours)

## 5. Enable CMS Login (GitHub OAuth)
The CMS needs OAuth to let editors log in with GitHub. Options:

### Option A: Netlify Identity (easiest if using Netlify)
If you deploy via Netlify instead of GitHub Pages, Netlify Identity handles auth automatically.

### Option B: External OAuth Provider
For GitHub Pages, you need an external OAuth app:
- [ ] Register a new OAuth App at https://github.com/settings/developers
  - Application name: `Advanced Arborist CMS`
  - Homepage URL: `https://wearetreepeople.com`
  - Authorization callback URL: `https://wearetreepeople.com/callback`
- [ ] Deploy an OAuth provider on Railway or similar
- [ ] Add `base_url` to the backend config in `admin/config.yml`

### Option C: Netlify CMS GitHub Backend (with Netlify)
- [ ] Connect repo to Netlify
- [ ] Enable Netlify Identity
- [ ] Enable Git Gateway in Netlify Identity settings
- [ ] Update `admin/config.yml` backend to use `git-gateway` instead of `github`

## Notes
- Single-page static HTML site — no build step needed
- The `_data/` folder contains all CMS-editable content as YAML files
- Content changes made through the CMS appear as commits in your repo
- The "Get Started" buttons email hello@wearetreepeople.com — this is handled by `mailto:` links, no form service needed
