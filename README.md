# Viet Nguyen's Personal Website

A personal website built with [Hugo](https://gohugo.io/) using the [Hugo Coder](https://github.com/luizdepra/hugo-coder) theme.

## 🚀 Quick Start

### Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) (version 0.124.0 or higher)
- [Git](https://git-scm.com/)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/vietwillnguyen/vietwillnguyen.github.io.git
cd vietwillnguyen.github.io
```

2. Install Hugo theme dependencies:
```bash
git submodule update --init --recursive
```

## 📝 Hugo Basics

### What is Hugo?
Hugo is a fast, modern static site generator written in Go. It's perfect for blogs, documentation sites, and personal websites.

### Key Hugo Concepts:
- **Content**: Markdown files in the `content/` directory
- **Layouts**: HTML templates in the `layouts/` directory
- **Static Assets**: Images, CSS, JS files in the `static/` directory
- **Configuration**: Site settings in `hugo.toml` or `hugo.yaml`
- **Themes**: Pre-built designs (we're using Hugo Coder)

### Project Structure
```
vietwillnguyen.github.io/
├── content/          # Your content (blog posts, pages)
├── layouts/          # Custom HTML templates
├── static/           # Static assets (images, CSS, JS)
├── themes/           # Hugo themes
├── assets/           # Source files for processing
├── data/             # Data files
├── i18n/             # Internationalization
├── archetypes/       # Content templates
├── hugo.toml         # Site configuration
└── public/           # Generated site (don't edit)
```

## ✍️ Adding Content

### Creating a New Blog Post

1. Create a new markdown file in `content/posts/`:
```bash
hugo new posts/my-new-post.md
```

2. Edit the front matter at the top of the file:
```yaml
---
title: "My New Post"
date: 2024-01-15
description: "A brief description of the post"
tags: ["hugo", "web-development"]
categories: ["tutorial"]
draft: false
---
```

3. Write your content below the front matter using Markdown.

### Creating a New Page

1. Create a new markdown file in `content/`:
```bash
hugo new my-page.md
```

2. Edit the front matter:
```yaml
---
title: "My Page"
description: "Page description"
---
```

### Content Types
- **Posts**: Blog articles in `content/posts/`
- **Pages**: Static pages in `content/`
- **Drafts**: Set `draft: true` to hide from production

## 🏃‍♂️ Running the Site

### Development Server

1. Start the Hugo development server:
```bash
hugo server -D
```

2. Open your browser and go to `http://localhost:1313`

The `-D` flag includes draft content. Remove it to exclude drafts.

### Build for Production

1. Build the site:
```bash
hugo
```

This creates a `public/` directory with your static site.

### Useful Hugo Commands

```bash
# Start development server
hugo server

# Build site
hugo

# Create new content
hugo new posts/post-name.md

# List all content
hugo list all

# Check site configuration
hugo config
```

## 🤖 GitHub Actions

This repository includes automated workflows for testing and deployment:

### Available Workflows

1. **Deploy Hugo site to Pages** (`.github/workflows/hugo.yaml`)
   - **Triggers**: Push to `master` branch, manual trigger
   - **Actions**: Builds Hugo site and deploys to GitHub Pages
   - **Features**: Concurrent deployment protection, automatic Hugo installation

2. **Test Hugo site** (`.github/workflows/test.yaml`)
   - **Triggers**: Push to `master`/`develop` branches, pull requests
   - **Actions**: Validates Hugo config, builds site, checks for errors
   - **Features**: HTML validation, broken link detection

### How to Use

1. **Automatic**: Just push to `master` branch - deployment happens automatically
2. **Manual**: Go to Actions tab → Select workflow → "Run workflow"
3. **Monitor**: Check the Actions tab to see build status and logs

### Workflow Benefits

- ✅ **No manual deployment steps**
- ✅ **Automatic testing on every push**
- ✅ **Catch errors before they reach production**
- ✅ **Version control for deployment process**
- ✅ **Rollback capability through GitHub**

## 🚀 Deployment

This site is configured for automatic deployment using GitHub Actions:

1. **Automatic Deployment**:
   - Push changes to the `master` branch
   - GitHub Actions automatically builds and deploys to GitHub Pages
   - No manual steps required!

2. **Workflow Features**:
   - **Build Testing**: Validates Hugo configuration and builds the site
   - **Automatic Deployment**: Deploys to GitHub Pages on successful build
   - **Concurrent Protection**: Prevents multiple deployments running simultaneously
   - **Manual Trigger**: Can be run manually from the Actions tab

3. **Manual Deployment** (fallback):
   ```bash
   # Build the site
   hugo
   
   # Push to GitHub (if using gh-pages branch)
   git add public/
   git commit -m "Update site"
   git push origin gh-pages
   ```

### Other Deployment Options

- **Netlify**: Drag and drop the `public/` folder
- **Vercel**: Connect your GitHub repository
- **AWS S3**: Upload `public/` contents to S3 bucket
- **Any web server**: Upload `public/` contents to your server

## 🎨 Customization

### Theme Configuration

The site uses the Hugo Coder theme. Customize it by:

1. **Colors**: Modify `colorScheme` in `hugo.toml`
2. **Social Links**: Update the `[[params.social]]` sections
3. **Menu**: Add items to the `[[menu.main]]` section
4. **Custom CSS**: Uncomment and modify the `customCSS` parameter

### Adding Custom Styles

1. Create `assets/css/custom.css`
2. Uncomment `customCSS = ["css/custom.css"]` in `hugo.toml`
3. Add your custom styles

### Adding Custom JavaScript

1. Create `assets/js/custom.js`
2. Uncomment `customJS = ["js/custom.js"]` in `hugo.toml`
3. Add your custom scripts

## 📚 Useful Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Hugo Coder Theme](https://github.com/luizdepra/hugo-coder)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages](https://pages.github.com/)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally with `hugo server`
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Built with ❤️ using Hugo** 