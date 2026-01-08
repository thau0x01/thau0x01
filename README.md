# Personal Resume Website

A personal resume website built with [Hugo](https://gohugo.io/) and the [Blowfish](https://blowfish.page/) theme, configured for deployment to GitHub Pages.

## Overview

This website serves as a professional portfolio and resume for an Information Security Specialist focused on Red Team operations, penetration testing, and offensive security.

## Features

- Clean, modern design using the Blowfish theme
- Responsive layout that works on all devices
- Dark mode support with automatic switching
- Sections for:
  - About/Professional Summary
  - Work Experience
  - Education
  - Technical Skills
  - Professional Certifications
  - Security Projects

## Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (v0.152.2 or later)
- [Git](https://git-scm.com/)

## Getting Started

1. **Clone the repository** (or if you haven't pushed to GitHub yet, initialize git):
   ```bash
   git clone <your-repo-url>
   cd thau0x01
   ```

2. **Initialize and update the theme submodule**:
   ```bash
   git submodule update --init --recursive
   ```

3. **Update the baseURL** in `config/_default/hugo.toml`:
   ```toml
   baseURL = "https://YOUR_USERNAME.github.io"
   ```
   Replace `YOUR_USERNAME` with your GitHub username.

4. **Update author information** in `config/_default/languages.en.toml`:
   - Add your name, email, and profile image path
   - Add links to your social profiles (GitHub, Twitter, LinkedIn, etc.)

5. **Preview the site locally**:
   ```bash
   hugo server
   ```
   Then visit `http://localhost:1313` in your browser.

6. **Build the site**:
   ```bash
   hugo
   ```
   This generates the static site in the `public/` directory.

## Customization

### Content

Edit the markdown files in the `content/` directory:

- `content/_index.md` - Homepage
- `content/about.md` - About/Professional Summary
- `content/experience/` - Work experience entries
- `content/education/` - Education entries
- `content/skills/` - Technical skills
- `content/certifications/` - Professional certifications
- `content/projects/` - Security projects and research

### Configuration

Edit configuration files in `config/_default/`:

- `hugo.toml` - Main Hugo configuration (baseURL, site metadata)
- `params.toml` - Theme parameters (colors, layouts, features)
- `menus.toml` - Navigation menu structure
- `languages.en.toml` - Language configuration including author profile information

### Theme

The Blowfish theme is included as a Git submodule. To update it:

```bash
git submodule update --remote themes/blowfish
```

For more customization options, see the [Blowfish documentation](https://blowfish.page/docs/).

## Deployment to GitHub Pages

This repository is configured to automatically deploy to GitHub Pages using GitHub Actions.

### Setup Instructions

1. **Create a GitHub repository** (if you haven't already):
   - Repository name: `YOUR_USERNAME.github.io` (replace with your GitHub username)
   - Or use a custom repository name

2. **Push your code to GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Navigate to Settings → Pages
   - Under "Source", select "GitHub Actions"
   - The workflow will automatically build and deploy your site

4. **Update the baseURL** (if using a custom repository name):
   - If your repository is `YOUR_USERNAME.github.io`, the site will be at `https://YOUR_USERNAME.github.io`
   - If using a custom repository name, the site will be at `https://YOUR_USERNAME.github.io/REPOSITORY_NAME/`
   - Update the `baseURL` in `config/_default/hugo.toml` accordingly

### Manual Deployment (Alternative)

If you prefer to deploy manually:

1. Build the site:
   ```bash
   hugo
   ```

2. Push the `public/` directory to the `gh-pages` branch:
   ```bash
   git subtree push --prefix public origin gh-pages
   ```

## Future Enhancements

- Cyberpunk color scheme customization
- Custom CSS/styling modifications
- Advanced theme customization

## License

This project is open source and available under the [MIT License](LICENSE).

## Credits

- Built with [Hugo](https://gohugo.io/)
- Theme: [Blowfish](https://github.com/nunocoracao/blowfish) by [nunocoracao](https://github.com/nunocoracao)
