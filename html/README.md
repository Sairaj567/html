# Sairaj Nagargoje — Personal Portfolio

A clean, responsive personal portfolio built with HTML, CSS, and JavaScript. This site showcases projects, skills, and experience, and can be easily customized.

## Structure

The main site is in this folder. Key paths:

- `index.html` — main page markup
- `assets/css/style.css` — styles
- `assets/js/script.js` — interactions (navigation, filters, modal)
- `assets/images/` — images and icons

## Run locally

You can open `index.html` directly in a browser. For a smoother experience (routing, assets), serve it with a simple local server.

Windows PowerShell (Python):

```powershell
# In the html folder
python -m http.server 5500
# Then open http://localhost:5500/
```

Node (if installed):

```powershell
# In the html folder
npx serve . -l 5500
# Then open http://localhost:5500/
```

## Customize

- Name, title, and About: edit in `index.html` (About section). Replace the TODO note with your specific focus areas (e.g., full‑stack, cloud, IoT, blockchain).
- Contact info: update email, phone, birthday, and location in the sidebar.
- Social links: replace the LinkedIn/GitHub/Twitter `href` values.
- Projects: update the Portfolio section cards and images in `assets/images/`.
- Skills: adjust names and percentages in the Resume → My skills list.

## Deploy

This is a static site; you can host it on any static hosting provider:

- GitHub Pages: push the `html/` contents to a repo and enable Pages.
- Netlify/Vercel: drag‑and‑drop the `html/` folder or connect your repo; publish the `html` directory.
- Any static file server: upload the folder as-is.

## Credits

Originally inspired by the vCard portfolio template by CodeWithSadee. Customized for Sairaj Nagargoje.

## License

MIT
