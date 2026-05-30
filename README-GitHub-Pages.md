# OCR AS Physics - No-Hassle iPad Setup

This setup is designed to avoid OneDrive preview issues on iPad.

## Why this works

- OneDrive preview can block JavaScript, which breaks dashboard behavior.
- GitHub Pages serves normal HTTPS pages, so the dashboard works consistently on iPad Safari.

## Free limits (important)

- GitHub is free for this setup.
- Keep each file under 100 MB (your current PDFs are below this).
- If your repo later approaches 1 GB+, move PDFs to OneDrive share links and keep only app files on GitHub Pages.

## Publish steps

1. Create a new GitHub repository.
2. Upload the full folder contents (including `index.html`, `topics-data.json`, and `Topic Questions`).
3. In GitHub: Settings > Pages.
4. Source: Deploy from a branch.
5. Branch: `main` and folder `/ (root)`.
6. Save, wait for deployment, then open your Pages URL.

## Day-to-day use for your son

1. Open the GitHub Pages URL in iPad Safari.
2. Use Share > Add to Home Screen.
3. Launch from the home icon like an app.

## Bulk topic management (no code edits)

- Edit `topics-data.json` to add or update many files.
- Or use dashboard buttons:
  - Export topics template
  - Import topics file

Topic format example:

```json
{
  "id": "m5-new-topic",
  "module": "Module 5 - New module",
  "title": "New topic title",
  "tq": "Topic Questions/Module 5 - New module/my-topic-TQ.pdf",
  "ms": "Topic Questions/Module 5 - New module/my-topic-MS.pdf"
}
```

You can also use full HTTPS links in `tq` / `ms` if PDFs are hosted elsewhere.

## Optional: combine with OneDrive for very large libraries

- Keep `index.html` + `topics-data.json` on GitHub Pages.
- Store PDFs in OneDrive.
- Put full OneDrive share links in `topics-data.json`.

This keeps hosting lightweight while still giving stable iPad access.
