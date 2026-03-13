# Technology Stack

## Core Technologies

- **Jekyll 4.2**: Static site generator
- **Ruby 3.4**: Runtime environment
- **Bundler**: Dependency management

## Frontend

- **Bootstrap 5**: CSS framework (grid, reboot, utilities modules)
- **Custom CSS**: `css/main.css` for site-specific styles
- **HTML/Liquid**: Templating with Jekyll's Liquid syntax

## Jekyll Plugins

- `jekyll-sitemap`: Automatic sitemap generation

## Deployment

- **AWS S3**: Static file hosting
- **AWS CloudFront**: CDN for content delivery
- **GitHub Actions**: CI/CD pipeline on push to main branch

## Common Commands

### Development
```bash
# Install dependencies
bundle install
# or with local vendor path
make install

# Start development server with live reload
bundle exec jekyll serve --watch
# or
make dev
```

### Build
```bash
# Build production site (outputs to public/)
JEKYLL_ENV=production bundle exec jekyll build -d public
```

### Deployment
Automatic via GitHub Actions on push to main branch:
1. Builds site with Jekyll
2. Syncs to S3 bucket
3. Invalidates CloudFront cache
