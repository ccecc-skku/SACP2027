# SACP 2027 Conference Website — GitHub / Netlify deployment

This folder is ready to be committed to the GitHub repository connected to Netlify.
The public domain is assumed to be `https://sacp2027.skku.edu`.

## Files

- `index.html` — current conference website, including GA4 tracking
- `images/myeongnyundang.png` — the existing hero image extracted from the original HTML
- `images/myeongnyundang-social.jpg` — 1200×630 social-media preview image made from the same Myeongnyundang photograph
- `downloads/` — folder reserved for the downloadable CFP files

## Social-media preview

`index.html` now includes Open Graph and Twitter/X metadata. The preview image is:

`https://sacp2027.skku.edu/images/myeongnyundang-social.jpg`

After deployment, Facebook may continue to show an older cached image until the URL is re-scraped in Meta Sharing Debugger.

## CFP downloads

Add the final CFP files to `downloads/` with these exact names:

- `SACP_2027_CFP.pdf`
- `SACP_2027_CFP.docx`

Recommended website links once the files are added:

```html
<a href="downloads/SACP_2027_CFP.pdf" target="_blank" rel="noopener">Download CFP (PDF)</a>
<a href="downloads/SACP_2027_CFP.docx" download>Download CFP (Word)</a>
```

Do not rename the files unless the corresponding links in `index.html` are changed.

## Deployment workflow

1. Copy these files/folders into the root of the existing GitHub repository used by Netlify.
2. Commit and push to the branch Netlify deploys (commonly `main`).
3. Netlify should build/deploy automatically.
4. Verify:
   - `https://sacp2027.skku.edu/`
   - `https://sacp2027.skku.edu/images/myeongnyundang-social.jpg`
5. After the CFP files are added, also verify their `/downloads/...` URLs.

No change to the SKKU custom-domain configuration should be necessary if the existing Netlify site is already serving `sacp2027.skku.edu`.
