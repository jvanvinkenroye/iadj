# ichautomatisierdasjetzt.de

Blog about digitalization, automation, and tech experiments.

## Tech Stack

- **SSG**: [Zola](https://www.getzola.org/)
- **Theme**: [tabi](https://github.com/welpo/tabi)
- **Hosting**: Firebase Hosting
- **CI/CD**: GitHub Actions

## Local Development

```bash
# Install Zola
brew install zola

# Clone with submodules
git clone --recurse-submodules <repo-url>

# Local preview
zola serve
```

The site will be available at `http://127.0.0.1:1111`.

## Deployment

- **Push to `main`**: Automatically deploys to production via GitHub Actions
- **Pull Request**: Creates a preview deployment (expires after 7 days)

### Required GitHub Secrets

- `FIREBASE_SERVICE_ACCOUNT`: Firebase service account JSON (set up via `firebase init hosting:github`)

## Project Structure

```
iadj/
├── config.toml          # Zola configuration
├── content/             # Markdown content
│   ├── _index.md        # Homepage
│   └── blog/            # Blog posts
├── static/              # Static assets
├── templates/           # Template overrides
├── themes/tabi/         # tabi theme (git submodule)
├── firebase.json        # Firebase Hosting config
├── .firebaserc          # Firebase project config
└── .github/workflows/   # CI/CD pipelines
```
