# CloudSentinel AI

An AI-powered multi-cloud CSPM (Cloud Security Posture Management) working model — real misconfiguration scanning, IAM attack-path analysis, Terraform static analysis, remediation generation, compliance mapping, and a live AI security copilot.

**Live structure:**
- `index.html` — landing/showcase page
- `dashboard.html` — the working dashboard app (single self-contained file)

No backend, no build step, no dependencies to install — everything runs client-side in the browser (Chart.js and D3 load from CDN).

## Deploy it (pick one)

### Option A — GitHub Pages (recommended, free, matches your existing portfolio workflow)
1. Create a new repo, e.g. `cloudsentinel-ai`, on your GitHub (`github.com/Sriram004`).
2. Push these two files to the repo root:
   ```bash
   git init
   git add index.html dashboard.html
   git commit -m "CloudSentinel AI — CSPM working model"
   git branch -M main
   git remote add origin https://github.com/Sriram004/cloudsentinel-ai.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source → Deploy from a branch → `main` / `root`**.
4. Your site goes live at `https://sriram004.github.io/cloudsentinel-ai/` within a minute or two.
5. Link it from your portfolio's projects grid, same as Detectra and SecuNova.

### Option B — Netlify Drop (fastest, no git required)
1. Go to https://app.netlify.com/drop
2. Drag the folder containing `index.html` and `dashboard.html` onto the page.
3. Netlify gives you a live URL immediately (you can rename the subdomain in site settings).

### Option C — Vercel
1. `npm i -g vercel` (one-time)
2. From this folder: `vercel --prod`
3. Follow the prompts — Vercel serves static HTML with zero config.

## Notes
- The AI Security Copilot module makes a live call to `https://api.anthropic.com/v1/messages` directly from the browser. Whatever hosting option you pick, the copilot will work as long as the visitor's browser can reach that endpoint — no server-side proxy needed for this demo.
- Asset inventory is realistic sample data (not a live cloud connection). Every module downstream of it — scanning, risk scoring, IAM graph traversal, Terraform analysis, remediation, compliance — runs real logic against that data.
- To wire in a real AWS/Azure/GCP connection later, the natural next step is a small backend (FastAPI + boto3/Azure SDK/GCP client) that replaces the sample inventory with a live resource pull, and the rest of the app's logic carries over unchanged.
