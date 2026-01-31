# Jekyll Template for QuantCDN

[![Deploy to QuantCDN](https://www.quantcdn.io/img/quant-deploy-btn-sml.svg)](https://dashboard.quantcdn.io/projects/add/jamstack/ssg-jekyll)

A production-ready Jekyll template configured for deployment to QuantCDN.

## Features

- Jekyll 4.x with Minima theme
- Blog-aware static site generation
- Liquid templating
- Markdown support
- SEO optimization with jekyll-seo-tag
- Automatic sitemap generation
- RSS feed support
- GitHub Actions deployment workflow

## Quick Start

### Local Development

1. Install Ruby (2.7 or higher recommended)

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Start the development server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open [http://localhost:4000](http://localhost:4000) in your browser

### Building for Production

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

The static site will be generated in the `_site` directory.

## Deployment to QuantCDN

### Automatic Deployment

This template includes a GitHub Actions workflow that automatically deploys to QuantCDN on push to the `main` branch.

Configure the following secrets in your GitHub repository:

- `QUANT_CUSTOMER` - Your Quant customer ID
- `QUANT_PROJECT` - Your Quant project name
- `QUANT_TOKEN` - Your Quant API token

### Manual Deployment

You can also deploy manually using the [Quant CLI](https://docs.quantcdn.io/docs/cli/getting-started):

```bash
# Build the site
JEKYLL_ENV=production bundle exec jekyll build

# Deploy to Quant
quant deploy --dir _site
```

## Project Structure

```
├── _config.yml          # Jekyll configuration
├── _posts/              # Blog posts
├── about.md             # About page
├── index.md             # Homepage
├── Gemfile              # Ruby dependencies
└── .github/workflows/   # CI/CD configuration
```

## Customization

### Site Configuration

Edit `_config.yml` to update:

- Site title and description
- Base URL and URL
- Theme settings
- Plugin configuration

### Adding Content

- **Pages**: Create `.md` or `.html` files in the root directory
- **Posts**: Add files to `_posts/` following the naming convention `YYYY-MM-DD-title.md`
- **Drafts**: Add files to `_drafts/` for work-in-progress posts

### Theming

This template uses the [Minima](https://github.com/jekyll/minima) theme. You can:

- Override theme files by creating files with the same path in your project
- Switch to a different theme by updating the `theme` setting in `_config.yml`
- Create a custom theme

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Minima Theme](https://github.com/jekyll/minima)
- [Quant Documentation](https://docs.quantcdn.io/)
- [Liquid Template Language](https://shopify.github.io/liquid/)

## License

This template is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
