# Zola Sveltia Source - Setup Guide

## ✅ Setup Status

### Completed:
- ✅ Repository cloned
- ✅ npm dependencies installed (Lightning CSS CLI)
- ✅ package.json configured
- ✅ Project structure ready

### Required:
- ⚠️ **Zola binary** - Needs to be installed

---

## Installation Guide

### Step 1: Install Zola

**Windows (with Chocolatey):**
```bash
choco install zola
```

**Windows (with Scoop):**
```bash
scoop install zola
```

**Other methods:**
Visit https://www.getzola.org/documentation/getting-started/installation/ for detailed installation instructions.

**Verify installation:**
```bash
zola --version
```

---

## Development

Once Zola is installed, run the development server:

```bash
zola serve --extra-watch-path settings
```

This will:
- Start a local development server (usually http://localhost:1111)
- Watch for changes in templates, content, and settings
- Auto-rebuild when files change

---

## Building for Production

To build the project for production:

```bash
zola build && npm run build
```

This will:
- Build the Zola site to the `public/` directory
- Minify and bundle CSS using Lightning CSS
- Target the last 2 versions of browsers

---

## Project Structure

```
d:\Coding\Projects\isedan-blog/
├── config.toml           # Site configuration
├── content/              # Blog posts and pages
├── settings/             # Sveltia CMS settings
├── templates/            # Zola HTML templates
├── static/               # Static assets (CSS, JS, images)
├── theme.toml            # Theme configuration
├── package.json          # npm dependencies
├── wrangler.toml         # Cloudflare Workers config
└── zola                  # Zola binary executable
```

---

## Deployment

This project can be deployed to:
- **Cloudflare Pages** - Direct integration with Git
- **Cloudflare Workers** - For more advanced serverless needs

See `wrangler.toml` for Cloudflare configuration.

---

## Next Steps

1. Install Zola from https://www.getzola.org/
2. Run `zola serve --extra-watch-path settings` to start development
3. Visit http://localhost:1111 to view your site
4. Configure Sveltia CMS backend for content management
5. Customize the site appearance through Design & Branding menu

---

## Useful Commands

- `zola serve --extra-watch-path settings` - Development server with settings watch
- `zola build` - Build for production
- `npm run build` - Minify and bundle CSS
- `npm fund` - Check package funding information

---

## License

WTFPL (Do What The Fuck You Want To Public License)
