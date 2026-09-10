# Automated Testing Strategy — hosted document

`index.html` is fully self-contained (fonts, runtime and styles inlined). No build step, no dependencies.

## Deploy on Cloudflare Pages (free)

1. Commit this `site/` folder to a GitHub repo.
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Pick the repo, then set:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `site`
4. **Save and Deploy**. Every push to the branch redeploys.

If you'd rather host the repo root, move `index.html` up one level and set the output directory to `/`.

## Regenerating

Edit `Testing Strategy.dc.html` in the project, then re-bundle to `site/index.html` — don't edit `index.html` by hand.
