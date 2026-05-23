# RegardingRetirement.com

Free retirement tools and honest guidance for Americans 55+.

---

## Repo Structure

```
/
├── index.html                          ← Homepage
├── vercel.json                         ← Vercel routing config
└── tools/
    ├── retirement-score.html           ← Tool 01: Am I On Track?
    ├── ss-breakeven-calculator.html    ← Tool 02: SS Break-Even
    ├── retirement-savings-gap.html     ← Tool 03: Savings Gap
    ├── rmd-calculator.html             ← Tool 04: RMD Calculator
    ├── medicare-penalty-calculator.html← Tool 05: Medicare Penalty
    ├── inflation-calculator.html       ← Tool 06: Inflation Impact
    ├── retirement-paycheck-builder.html← Tool 07: Paycheck Builder
    ├── healthcare-cost-estimator.html  ← Tool 08: Healthcare Estimator
    ├── roth-conversion-estimator.html  ← Tool 09: Roth Conversion
    └── spousal-benefit-optimizer.html  ← Tool 10: Spousal Optimizer
```

---

## Deployment (GitHub → Vercel → regardingretirement.com)

**Same workflow as CoolOldTrucks.com.**

### Step 1 — Create the GitHub repo
1. Go to github.com → New repository
2. Name it: `regarding-retirement`
3. Set to Public
4. Do NOT initialize with README (you have one)
5. Create repository

### Step 2 — Push files to GitHub
Using GitHub's browser editor (mobile-friendly):
1. Open the repo
2. Click "Add file" → "Upload files"
3. Upload `index.html` and `vercel.json` first
4. Create a `tools/` folder: click "Add file" → type `tools/retirement-score.html` in the filename box — GitHub creates the folder automatically
5. Upload all 10 tool HTML files into `tools/`
6. Commit each batch

### Step 3 — Connect Vercel
1. Go to vercel.com → New Project
2. Import the `regarding-retirement` GitHub repo
3. Framework preset: **Other** (plain HTML)
4. Root directory: `/` (leave as default)
5. Click Deploy
6. Vercel gives you a `.vercel.app` preview URL — test it

### Step 4 — Connect your domain
1. In Vercel project → Settings → Domains
2. Add `regardingretirement.com`
3. Add `www.regardingretirement.com`
4. Vercel shows you DNS records to add
5. Go to Namecheap → Advanced DNS
6. Add the A record and CNAME exactly as Vercel shows
7. DNS propagates in 5–30 minutes
8. Vercel auto-provisions SSL — site goes live at https://regardingretirement.com

### Step 5 — Wire the email form
1. Sign up at kit.com (free to 10K subscribers)
2. Create a form → get the form action URL
3. In `index.html`, find the `handleEmail` function
4. Replace the `// TODO` comment with a fetch to your Kit endpoint
5. Commit → Vercel auto-deploys

---

## After Launch

- Update YouTube links in `index.html` once videos are live with real URLs
- Update tool URLs in each video description to match live site paths
- Add Google Search Console: Settings → add `regardingretirement.com` → verify via HTML tag in `<head>`
- Add Google Analytics if desired: paste GA4 script before `</head>`

---

## Channel
YouTube: @RetirementClarity
Email: regardingretirement@gmail.com
