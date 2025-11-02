# Portfolio (React + Vite)
# Portfolio (React + Vite)

This repository is a conversion of your provided static HTML portfolio into a small React app using Vite.

What I added
- `package.json` — manifest with scripts for dev/build/preview
- `vite.config.js` — Vite config with React plugin
- `index.html` — Vite entry that loads `src/main.jsx`
- `src/main.jsx` — React entry
- `src/App.jsx` — App component (now split into components under `src/components/`)
- `src/index.css` — Styles extracted and adapted from your HTML
- `public/image/README.txt` — place images here with the expected filenames

How to run (Windows PowerShell)

1. Install dependencies:

```powershell
cd d:/project
npm install
```

2. Start dev server:

```powershell
npm run dev
```

Open the URL shown by Vite (usually http://localhost:5173).

Notes
- Add your images to `public/image/` as `profile-pic.jpg`, `project-1.png`, and `project-2.png`.
- The app code is now modularized. Components live in `src/components/`.

Contact form
- The app contains a simple contact form in `src/components/Contact.jsx` that can submit to Formspree. To enable it:
	1. Create a Formspree form and get the endpoint (it looks like `https://formspree.io/f/yourFormId`).
	2. Create a `.env` file in the project root with this line:

```
VITE_FORMSPREE_ENDPOINT=https://formspree.io/f/yourFormId
```

	3. Restart the dev server.

If `VITE_FORMSPREE_ENDPOINT` is not set the Contact section will show social links and instructions instead of the form.

Deployment
- Vercel (recommended): Import the project folder in Vercel and deploy. The included `vercel.json` will serve the built `dist` folder.
- GitHub Pages (manual): build the app and push the `dist` content to the `gh-pages` branch or use a Pages workflow. Example local build + serve:

```powershell
npm run build
npx serve -s dist
```

If you'd like, I can add an automated GitHub Actions workflow to publish to GitHub Pages or add a `gh-pages` deploy script.

Extras you can ask for
- Split styles into CSS modules or use Tailwind.
- Add React Router for separate pages.
- Add image optimization / lazy loading.
- Hook a simple serverless endpoint for contact messages.

---

If you want me to proceed with automatic deploy setup (GitHub Actions) or to add the `gh-pages` script, tell me and I'll implement it next.
