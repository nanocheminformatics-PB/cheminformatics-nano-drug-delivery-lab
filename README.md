# Cheminformatics & Nano Drug Delivery Lab website

A responsive, modern-scientific static website for the **Cheminformatics and Nano Drug Delivery Lab, Department of Bioinformatics, Alagappa University**. Designed for GitHub Pages with editable content through Pages CMS.

## What's included

- Responsive landing page and research-theme cards
- Research project gallery
- Searchable publications with DOI and publisher links
- Interactive 3D molecular viewer powered by 3Dmol.js, loading PDB coordinates from RCSB PDB
- Team profiles and news/announcements
- JSON-based content files, editable through [Pages CMS](https://pagescms.org/)
- No build step and no paid hosting required

## 1. Publish on GitHub Pages

1. Create a GitHub repository. For a user site, name it `YOUR-USERNAME.github.io`; for a project site, any repository name works.
2. Upload all files and folders from this package to the repository's root. Keep `.pages.yml` and the `assets`, `data`, `admin`, and `images` folders.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Wait for the Pages deployment to finish. Your site will be at `https://YOUR-USERNAME.github.io/` for a user site, or `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/` for a project site.

If using a project site, the relative links in this site are designed to work from the repository subpath.

## 2. Edit content with Pages CMS

This project uses [Pages CMS](https://pagescms.org/), a hosted GitHub content editor. It edits JSON files in your repository and commits the changes to GitHub.

1. Push the site to GitHub first.
2. Open `https://pagescms.org/` and sign in with GitHub.
3. Authorize access only to the repository you intend to edit, if repository-scoped access is offered.
4. Open/import your repository. Pages CMS reads `.pages.yml` to build forms for Research themes, Projects, Publications, Team, and News.
5. Edit records and save. The CMS commits updates to the JSON files; GitHub Pages then republishes the website.

**CMS configuration note:** Pages CMS schema features can evolve. If the CMS flags a field-schema issue, follow its current `.pages.yml` documentation. The website still works without the CMS: edit the JSON files directly in `data/`.

## 3. Before public launch

- Replace the placeholder contact email in `index.html` (`REPLACE_WITH_OFFICIAL_EMAIL`).
- Replace the sample team entries with verified names, designations, biographies and approved photos.
- Replace the sample publication record with real citation metadata and DOI URLs. Delete the placeholder record if there are no publications to list yet.
- Replace illustrative project descriptions with approved project summaries, funding details, dates and outcomes.
- Confirm the lab name, department name, university branding and all institutional links are accurate and approved.
- Add an official privacy notice if collecting personal data through forms or analytics.
- Check mobile layout, keyboard navigation, outbound links and the browser console.

## 4. Interactive molecular viewer

The viewer loads a PDB file from `https://files.rcsb.org/download/{PDB_ID}.pdb` and renders it using 3Dmol.js from its public CDN. It needs an internet connection. It is a public structure viewer, not a molecular docking or simulation tool.

## 5. Storage and privacy

GitHub Pages hosts static files. Do not place API keys, passwords, confidential research data, patient information, unpublished sensitive data or credentials in this public repository. Keep large simulation trajectories and raw experimental datasets in suitable institutional or research-data storage, linking to them where appropriate.

## 6. Local preview

You can preview with any static local server, for example:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`. Opening `index.html` directly may prevent the browser from fetching the JSON content files because of local-file security restrictions.

## Folder structure

```text
.
├── index.html
├── .pages.yml
├── README.md
├── assets/
│   ├── app.js
│   ├── styles.css
│   ├── lab-mark.svg
│   └── favicon.svg
├── data/
│   ├── research.json
│   ├── projects.json
│   ├── publications.json
│   ├── team.json
│   └── news.json
├── admin/
│   └── README.md
└── images/
    └── README.md
```
