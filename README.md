# Anil Kumar Cherukuri — Portfolio

Static portfolio site served by a tiny Express server, ready for Railway.

## Run locally
```
npm install
npm start
# open http://localhost:3000
```

## Deploy to Railway

### Option A — from GitHub (recommended)
1. Push this folder to a new GitHub repo.
2. Go to https://railway.app → **New Project** → **Deploy from GitHub repo** → pick the repo.
3. Railway detects Node.js, runs `npm install` and `npm start`. Nothing else to configure.
4. Open the service → **Settings** → **Networking** → **Generate Domain** to get a public URL.
   Add a custom domain there if you own one.

### Option B — Railway CLI
```
npm i -g @railway/cli
railway login
railway init        # creates a new project
railway up          # uploads and deploys
railway domain      # generates a public URL
```

## Editing
Everything visible lives in `public/index.html` (content, CSS and a small script in one file).
Colors and fonts are CSS variables at the top of the `<style>` block.

## Custom domain on Railway
1. Buy the domain at any registrar (Namecheap, Cloudflare, Porkbun, GoDaddy).
2. Railway → your service → **Settings → Networking → Custom Domain** → enter the domain.
3. Add the CNAME record Railway shows you at the registrar (for the root domain use the registrar's ALIAS/ANAME/CNAME-flattening option, or point `www` and redirect root to it).
4. Railway issues the SSL certificate automatically once DNS propagates.
