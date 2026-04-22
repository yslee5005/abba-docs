# abba-docs

Public legal & help documents for the **Abba — Prayer & Quiet Time** iOS app, hosted via GitHub Pages.

**Live URL (after setup):** https://yslee5005.github.io/abba-docs/

---

## File Structure

```
abba-docs/
├── _config.yml          # Jekyll site config
├── index.md             # Landing page with navigation
├── privacy.md           # Privacy Policy (English)
├── privacy-ko.md        # 개인정보 처리방침 (Korean)
├── terms.md             # Terms of Service (English)
├── terms-ko.md          # 서비스 이용약관 (Korean)
├── help.md              # Help & FAQ (English)
├── help-ko.md           # 도움말 및 FAQ (Korean)
└── README.md            # This file (not built by Jekyll)
```

---

## 🚀 First-Time Setup — Publishing via GitHub Pages

### 1. Create the GitHub repository

```bash
# Option A: via GitHub CLI (recommended)
cd /tmp/abba-docs
git init
git add .
git commit -m "Initial legal docs for Abba"
gh repo create yslee5005/abba-docs --public --source=. --push

# Option B: via GitHub web
# 1. Create a new public repo named "abba-docs" on github.com
# 2. Then locally:
cd /tmp/abba-docs
git init
git remote add origin https://github.com/yslee5005/abba-docs.git
git add .
git commit -m "Initial legal docs for Abba"
git branch -M main
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to `https://github.com/yslee5005/abba-docs/settings/pages`
2. Under **Source**, select **Deploy from a branch**
3. Set branch to **main**, folder to **/ (root)**
4. Click **Save**
5. Wait 1–2 minutes. Your site will be live at:

   `https://yslee5005.github.io/abba-docs/`

### 3. Verify URLs for App Store Connect

Open these URLs in a browser to confirm they load:

- `https://yslee5005.github.io/abba-docs/` (landing)
- `https://yslee5005.github.io/abba-docs/privacy.html` (Privacy Policy — submit this to App Store Connect)
- `https://yslee5005.github.io/abba-docs/terms.html` (Terms — submit as EULA if needed)
- `https://yslee5005.github.io/abba-docs/help.html` (Help — submit as Support URL)

> ⚠️ GitHub Pages serves `.md` files as `.html`. Always link to `.html` in App Store Connect.

---

## ✍️ How to Update Documents

### Edit a Markdown file
1. Open the `.md` file on GitHub (click the pencil icon) or locally.
2. Make your changes.
3. Update the **"Last Updated"** date at the top.
4. Commit and push.
5. GitHub Pages rebuilds automatically within 1–2 minutes.

### Local preview (optional)
```bash
# Install Ruby + bundler once
gem install jekyll bundler

# In the repo
bundle init
echo 'gem "jekyll"' >> Gemfile
echo 'gem "jekyll-seo-tag"' >> Gemfile
bundle install

# Preview at http://localhost:4000/abba-docs/
bundle exec jekyll serve
```

---

## 🌐 Optional: Custom Domain (e.g. abba.ystech.app)

1. In your domain registrar (Namecheap, Cloudflare, etc.), add a **CNAME** record:
   - Name: `abba` (or whatever subdomain)
   - Target: `yslee5005.github.io`
2. Add a `CNAME` file in the repo root containing just the domain:
   ```
   abba.ystech.app
   ```
3. In **repo Settings → Pages → Custom domain**, enter `abba.ystech.app` and save.
4. Enable **Enforce HTTPS** after DNS propagates (usually within 1 hour).
5. Update `_config.yml`:
   ```yaml
   baseurl: ""
   url: https://abba.ystech.app
   ```

---

## 🌏 Translation Update Guide

Currently supported languages: **English (en)** + **Korean (ko)**.

When updating any document, please:
1. Update the English `.md` first.
2. Translate the changes to `-ko.md`.
3. Keep the **"Last Updated"** date in sync across both.
4. If you add a new translation (e.g. `privacy-ja.md`), add a link in `index.md`.

---

## 📋 Placeholders to Replace Later

These values are currently placeholders — replace them when real information is available:

| Placeholder | Current Value | Replace With |
|---|---|---|
| Support email | `rrallvv@gmail.com` | Dedicated support address (e.g. `support@abba.app`) |
| Company identity | "Abba team (independent developer project)" | Registered legal entity name + address |
| Governing law jurisdiction | "Republic of Korea / Seoul courts" | Confirm with lawyer based on where you incorporate |
| Bundle ID | `com.ystech.abba` | Should match App Store Connect |
| Subscription prices | USD 6.99 / 49.99 | Update if pricing changes |
| Abba Pro feature names | Scripture Deep, Prayer Coaching | Update as product evolves |

---

## ⚖️ Legal Disclaimer

**This documentation is a template starting point, not legal advice.** It was drafted to cover GDPR, CCPA, COPPA, and PIPA principles at a reasonable level for an early-stage indie app. Before relying on it for a production launch with paying subscribers in multiple jurisdictions, you should have a licensed attorney review it — especially the Privacy Policy and Terms of Service. Laws change, and specific jurisdictions (EU, California, Korea) can require custom language.

---

## Maintainer

- **GitHub:** [@yslee5005](https://github.com/yslee5005)
- **Email:** rrallvv@gmail.com
