AIworld — README
=================

Files created:
- index.html   (the site; rename to index.html if you like)
- README.md            (this file)

How to "club" your Perplexity JSON + Gemini images into this site
----------------------------------------------------------------
1) Folder structure (recommended - place all files in one project folder):
   /AIworld/
     index.html              <- move or rename AIworld_index.html to index.html
     /images/
       hero.png              <- hero image generated from Gemini
       logo.png              <- logo from Gemini
       cat1.png              <- category 1 image
       cat2.png              <- category 2 image
       cat3.png              <- category 3 image

2) If you already have a JSON from Perplexity:
   - Ensure the file is named exactly `data.json` and placed beside index.html.
   - The script in index.html expects keys like `site_name`, `hero_headline`, `categories` (array), etc.
   - If your JSON uses different key names, either rename keys or open index.html and edit the loader script to map fields.

3) Local preview:
   - For security reasons, modern browsers block fetch() from file://. Use a tiny static server:
     python3 -m http.server 8000
     then open http://localhost:8000 in your browser.
   - Or use any static server (Node's `http-server`, VSCode Live Server, etc.).

4) Deploy (GitHub Pages - free):
   - Create a new GitHub repo and push all files.
   - If you name the repo `username.github.io` the site will be served at that URL.
   - Or enable GitHub Pages from the repo settings (Branch: main, folder: /root).

   Git commands example:
     git init
     git add .
     git commit -m "Initial AIworld site"
     git branch -M main
     git remote add origin https://github.com/YOURNAME/YOURREPO.git
     git push -u origin main

5) Deploy (Netlify - free):
   - Drag & drop the folder or connect the GitHub repo.
   - Netlify auto-deploys static sites.

6) Notes:
   - If your Perplexity JSON includes absolute URLs for images, place those values in `logo`, `hero_image`, and category `image` fields; the site will use them directly.
   - To change CTAs or add more categories, edit data.json (or update the fields in the loader script).
   - If you want to pre-render the site (no JS), you can copy the resolved values from data.json into the HTML directly and skip the fetch step.

Questions & next steps:
- Want me to convert your Perplexity JSON (paste it here) into a ready `data.json` I can save for you?
- Want me to bundle a ZIP containing index.html + sample_data.json so you can download everything in one go?

