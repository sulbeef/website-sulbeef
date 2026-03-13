# Project Structure

## Directory Organization

```
/
├── _config.yml           # Jekyll configuration
├── _layouts/             # Page layout templates
│   └── base.html         # Base HTML structure
├── _includes/            # Reusable HTML components
│   ├── head.html         # HTML head section
│   ├── header.html       # Site header
│   └── footer.html       # Site footer
├── css/                  # Stylesheets
│   ├── bootstrap-*.css   # Bootstrap modules (grid, reboot, utilities)
│   └── main.css          # Custom site styles
├── js/                   # JavaScript files
├── img/                  # Image assets
├── .well-known/          # Web standards directory (included in build)
├── vendor/               # Bundler dependencies (excluded from build)
└── index.html            # Homepage
```

## Jekyll Conventions

### Layouts
- Stored in `_layouts/`
- `base.html` provides the main HTML structure
- Pages specify layout in front matter: `layout: default`

### Includes
- Stored in `_includes/`
- Reusable components imported with `{% include filename.html %}`
- Current includes: head, header, footer

### Front Matter
- YAML configuration at the top of files between `---` markers
- Used to specify layout and other page metadata

### Content Language
- Site language: Portuguese (pt-BR)
- Set in `_layouts/base.html` with `lang="pt-BR"`

## Build Output
- Development: Jekyll serves from memory
- Production: Built to `public/` directory (configured in CI/CD)

## Excluded from Build
Files listed in `_config.yml` exclude section are not published to the production site.
