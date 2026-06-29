# mimo-sandbox

Static test page repository for MiMo Code builds. Served by Caddy on Railway.

## How it works

```
public/
├── index.html          # Landing page (this repo's root)
├── page-name/
│   └── index.html      # Each test page in its own folder
└── ...
```

## Publishing a page

```bash
# 1. Create the page folder and write HTML
mkdir -p public/my-page

# 2. Add your HTML
cat > public/my-page/index.html << 'EOF'
<!DOCTYPE html>
<html>...</html>
EOF

# 3. Commit and push — Railway auto-deploys in ~30s
git add public/my-page/
git commit -m "add my-page"
git push
```

## Live URL

Once deployed, your page is live at:
`https://<railway-domain>/my-page/`

## Architecture

- **Source of truth:** This GitHub repo
- **Web server:** Caddy (file_server browse)
- **Hosting:** Railway (auto-deploy on push)
- **Agent:** MiMo Code builds pages, commits, pushes

## Agent instructions

When building a test page:
1. Write HTML to `public/<page-name>/index.html`
2. Use inline CSS (no external dependencies)
3. `git add . && git commit -m "add <page-name>" && git push`
4. Log the deploy to Obsidian tracker at `5. Agents/Hermes/MiMo/sandbox-tracker.md`
