# GitHub Actions Deployment Workflow

This repository demonstrates a modern GitHub Actions workflow for deploying a static website to GitHub Pages. The project is based on the roadmap provided by [roadmap.sh](https://roadmap.sh/projects/github-actions-deployment-workflow) and showcases best practices for GitHub Actions deployment using the latest official GitHub Pages actions.

## Features

- **Modern GitHub Actions**: Uses the latest official GitHub Actions for Pages deployment
- **Secure Deployment**: Implements secure deployment practices with proper permissions
- **Continuous Deployment**: Automatically deploys changes pushed to the `main` branch
- **Zero Configuration**: No additional setup required beyond enabling GitHub Pages

## Project Structure

```
.
├── .github
│   └── workflows
│       └── deploy.yml    # GitHub Actions workflow configuration
├── index.html           # Static website with modern styling
└── README.md           # Documentation
```

## Workflow Details

The deployment workflow (`.github/workflows/deploy.yml`) uses the following official GitHub Actions:

- `actions/checkout@v4`: Checks out your repository
- `actions/configure-pages@v4`: Sets up GitHub Pages
- `actions/upload-pages-artifact@v3`: Packages your site
- `actions/deploy-pages@v4`: Deploys to GitHub Pages

### Key Features:

- **Proper Permissions**: Explicitly defined permissions for security
- **Environment Configuration**: Uses the github-pages environment
- **Artifact Handling**: Efficient artifact upload and deployment
- **Clean Workflow**: Minimal, maintainable configuration

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/<your-username>/gh-deployment-workflow.git
   cd gh-deployment-workflow
   ```

2. **Enable GitHub Pages**
   - Go to your repository's Settings > Pages
   - Under "Build and deployment", select "GitHub Actions" as the source

3. **Update Content**
   - Modify `index.html` to update your site's content
   - Push changes to the `main` branch
   ```bash
   git add index.html
   git commit -m "Update content"
   git push origin main
   ```

4. **Access Your Site**
   - Your site will be available at: `https://<username>.github.io/gh-deployment-workflow/`
   - Check the Actions tab for deployment status

## Troubleshooting

If your deployment fails:
1. Check the Actions tab for detailed error messages
2. Verify repository permissions in Settings > Actions > General
3. Ensure GitHub Pages is enabled and configured correctly
4. Confirm all workflow permissions are set properly

## Resources & Further Reading

- **Project Page**: [GitHub Actions Deployment Workflow on roadmap.sh](https://roadmap.sh/projects/github-actions-deployment-workflow)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Official GitHub Pages Actions](https://github.com/actions/configure-pages)

## License

This project is open source and available under the MIT License.

---

Feel free to use this template for your own GitHub Pages deployments! Check out the [roadmap.sh project page](https://roadmap.sh/projects/github-actions-deployment-workflow) for more ideas and enhancements.