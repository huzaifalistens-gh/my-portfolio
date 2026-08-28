# Huzaifa Salim — Portfolio

A single-page portfolio site. Pure static HTML/CSS/JS — no build step, no framework, no `npm install` needed to run it.

## Run it locally

Just open `index.html` in a browser, or serve the folder with any static server, e.g.:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deploy: GitHub → Vercel

**1. Push this folder to GitHub**

```bash
cd portfolio_updated
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

(Create the empty repo on GitHub first at github.com/new, then use the URL it gives you in place of the one above.)

**2. Import into Vercel**

- Go to [vercel.com/new](https://vercel.com/new)
- Click **Import Git Repository**, sign in with GitHub if prompted, and select the repo you just pushed
- Vercel will auto-detect this as a static site — **no build command, no output directory, no environment variables needed.** Leave everything on its defaults and click **Deploy**
- After a few seconds you'll get a live `.vercel.app` URL

**3. Future updates**

Any time you `git push` to `main`, Vercel automatically redeploys. No manual steps after the first setup.

## Project structure

```
index.html          — the whole site (home, projects, FairDrive case study merged in, etc.)
assets/              — real product screenshots used in the FairDrive case study
  ├─ customer/        — rider app screens
  ├─ driver/           — driver app screens
  ├─ admin/            — admin panel screens
  ├─ design-system/    — design system screens
  ├─ decisions/        — screens referenced in the "Decisions" section
  └─ website/          — FairDrive marketing site screens
```

## Known open item

The **"Read the full case study →"** button in the FairDrive footer links to `fairdrive-full-case-study.html`, which doesn't exist yet — it's a placeholder for a future, deeper version of the case study. Until that page is built, that link will 404. Either build that page and drop it in the root next to `index.html`, or point the button somewhere else in the meantime.
