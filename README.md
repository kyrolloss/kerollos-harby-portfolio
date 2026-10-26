# Kerollos Harby — Portfolio

Static, English-language portfolio for GitHub Pages. Repository: https://github.com/kyrolloss/kerollos-harby-portfolio. Site URL: https://kyrolloss.github.io/kerollos-harby-portfolio/.

## Preview locally

Open PowerShell in this folder and run:

```powershell
python -m http.server 8765
```

Then open <http://localhost:8765>. Direct project routes work because each page has its own `index.html`.

To regenerate the HTML after editing the supplied content or contact configuration, run:

```powershell
python build.py
```

The generator reads `data/02-projects.json`, `data/ASSET-MANIFEST.json`, and `owner-profile.json`. Screenshot files are bundled in `assets/screenshots/`; they are served locally and are not hotlinked.

## Publish after approval

1. The public repository `kyrolloss/kerollos-harby-portfolio` is created for this site.
2. Before relying on the public site, confirm rights to republish supplied screenshots and the ONE collage/mobile images. No downloaded original client-site images are included. The contact phone number is public on the site.
3. The generator reads the deployed URL from `owner-profile.json` and writes the matching sitemap and robots file.
4. In PowerShell, open this folder and run the following commands, replacing the remote URL with the repository you created:

   ```powershell
   git init
   git add .
   git commit -m "Add portfolio website"
   git branch -M main
   git remote add origin https://github.com/kyrolloss/kerollos-harby-portfolio.git
   git push -u origin main
   ```

5. In GitHub, open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
6. Wait for the Pages deployment to complete, open the URL GitHub shows, and verify the homepage, project index, a case study, contact links, and mobile layout. Share the public URL only after that verification.

The repository exists. The public site is deployed when GitHub Pages finishes the first deployment from `main` (root).

## Owner configuration and launch items

- `owner-profile.json` holds the provided phone number, LinkedIn profile URL, and GitHub Pages base URL used by the generated pages.
- Confirm each person’s role/contribution for every project before adding first-person authorship claims. Current pages explicitly avoid claiming who designed or built the projects.
- Contact phone and LinkedIn are provided. Email, portrait, location, role title, biography, availability, and tools are omitted because none were supplied.
- Confirm permission to republish the screenshot captures before publishing.
- Dhofar Sooq has no public case-study page because it was unreachable and has no verified features or images. Its source record remains in the project JSON.
- The “Graduation Project Henna” source label is flagged on its page; the live site currently presents BrainWave, a mind-map and blog product. Excited.sa is described using the current event-planning content from the research package.
- The owner identifies the dental application as ONE; its linked sign-in page currently displays Smart Dental System, and the owner confirms these are the same app. The case study combines 31 earlier mobile captures with two additional ONE-branded captures and the supplied collage cover. The dashboard requires sign-in, and sample data in the captures is fake. Confirm image reuse rights before public launch.

## Adding a project

Add its verified record and screenshot entries to `data/02-projects.json` and `data/ASSET-MANIFEST.json`, place genuine captures under `assets/screenshots/{project-id}/`, then run `python build.py`. Keep service and feature descriptions grounded in evidence, and do not pad galleries with duplicate images.
