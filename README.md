# GitHub Actions Deployment Workflow

This repository demonstrates a simple GitHub Actions workflow for deploying a static website (a single `index.html` file) to GitHub Pages. The project is based on the roadmap provided by [roadmap.sh](https://roadmap.sh/projects/github-actions-deployment-workflow), which you can check out as the project page for more ideas and enhancements.

## Overview

This project features:
- **GitHub Actions Workflow**: Automatically deploys changes pushed to the `main` branch (when `index.html` is updated) to GitHub Pages.
- **Static Deployment**: No build steps or static site generators are used—this project focuses on a straightforward deployment of a simple HTML file.
- **Continuous Deployment**: Every time you update `index.html` and push your changes, the workflow triggers and updates your live site.

## Project Structure

```
.
├── .github
│   └── workflows
│       └── deploy.yml    # GitHub Actions workflow file
├── index.html          # Your static website
└── README.md           # This file
```

## GitHub Actions Workflow

The workflow defined in `.github/workflows/deploy.yml`:
- **Triggers on Changes**: It listens for pushes to the `main` branch that affect the `index.html` file.
- **Deploys to GitHub Pages**: Uses the [peaceiris/actions-gh-pages](https://github.com/peaceiris/actions-gh-pages) action to publish your site directly from the repository's root.

## Setup & Usage

1. **Fork or Clone the Repository**
   ```bash
   git clone https://github.com/<your-username>/<repository-name>.git
   cd <repository-name>
   ```

2. **Customize Your `index.html`**
   - Edit the `index.html` file to update your site's content.

3. **Commit & Push Changes**
   ```bash
   git add index.html
   git commit -m "Update index.html"
   git push origin main
   ```

4. **Verify Deployment**
   - Visit your live site at: `https://<your-username>.github.io/<repository-name>/`
   - Monitor the GitHub Actions tab in your repository for workflow progress and logs.

## Resources & Further Reading

- **Roadmap Project Page**: [GitHub Actions Deployment Workflow on roadmap.sh](https://roadmap.sh/projects/github-actions-deployment-workflow)
- **GitHub Actions Documentation**: [docs.github.com/en/actions](https://docs.github.com/en/actions)
- **GitHub Pages Documentation**: [docs.github.com/en/pages](https://docs.github.com/en/pages)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to enhance the workflow, add new features, or integrate more complex build processes as you continue your journey with GitHub Actions and continuous deployment!