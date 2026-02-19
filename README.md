# NexStratus GTM Sprints Q1

Internal-only presentation. Not indexed by search engines or AI crawlers.

## Deploy to GitHub + Vercel

### 1. Create a GitHub repo

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

### 2. Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click **Add New → Project**
3. Import your GitHub repo
4. Leave all build settings as default (Framework: **Other**)
5. Click **Deploy**

Vercel will serve `nexstratus_gtm_sprints_v4.html` at the root URL `/` automatically via `vercel.json`.

### 3. Optional: Password-protect on Vercel

In your Vercel project → **Settings → Password Protection** — add a password so only people with the link AND password can view it.

## Crawler Blocking

This project includes three layers of crawler/AI blocking:

| Layer | File | Covers |
|---|---|---|
| HTML meta tags | `nexstratus_gtm_sprints_v4.html` | Googlebot, Bingbot, GPTBot, ClaudeBot, PerplexityBot, CCBot, and more |
| HTTP headers | `vercel.json` | `X-Robots-Tag` header sent with every response |
| robots.txt | `robots.txt` | All crawlers including AI training bots |
