# CLAUDE.md - Clean Theme

This file provides guidance to Claude Code when working with the "Clean" theme
for the Korean personal blog.

## Theme Overview

Clean is a custom Pelican theme designed for Korean content with a minimalist
aesthetic. It features Korean web fonts, responsive design, and modern web
standards support.

## Directory Structure

```
clean/
├── CLAUDE.md              # This documentation file
├── README.md              # Basic theme information
├── static/                # Static assets
│   └── css/
│       ├── pygments.css   # Syntax highlighting styles
│       └── style.css      # Main theme stylesheet
└── templates/             # Jinja2 templates
    ├── _include/          # Reusable template components
    │   ├── buy_me_a_coffee.html  # Donation widget
    │   ├── footer.html           # Site footer
    │   ├── ga.html              # Google Analytics
    │   ├── gads.html            # Google AdSense
    │   ├── giscus.html          # Giscus comments
    │   ├── head.html            # HTML head section
    │   ├── js.html              # JavaScript includes
    │   ├── nav.html             # Navigation menu
    │   ├── pagination.html      # Page navigation
    │   ├── title.html           # Site title display
    │   └── utterances.html      # Utterances comments
    ├── archives.html        # Archive page template
    ├── article.html         # Individual article template
    ├── categories.html      # Categories index template
    ├── category.html        # Single category template
    ├── index.html           # Homepage template
    ├── page.html            # Static page template
    ├── shell.html           # Base template (extends all others)
    ├── tag.html             # Single tag template
    └── tags.html            # Tags index template
```

## Key Features

### Typography & Fonts
- **Korean Fonts**: NanumSquareNeo for body text
- **Decorative Fonts**: ChusaLove for site title, Binggrae for article titles
- **English Fonts**: IBM Plex Sans for headers
- **Font Loading**: Google Fonts and Naver fonts integration

### Responsive Design
- Bootstrap-based responsive grid system
- Mobile-friendly navigation and layout
- Flexible container widths

### SEO & Social
- Open Graph meta tags for social sharing
- Twitter Card support
- Korean language meta tags (ko-KR)
- Article metadata with published/modified dates

### Comment Systems
- Giscus integration for GitHub-based comments
- Utterances support as alternative
- Conditional loading based on configuration

### Analytics & Monetization
- Google Analytics integration
- Google AdSense support
- Buy Me a Coffee donation widget

## Template Hierarchy

1. **shell.html** - Base template with HTML structure, meta tags, navigation
2. **index.html** - Homepage with article summaries and pagination
3. **article.html** - Individual post template with comments and metadata
4. **page.html** - Static pages template
5. **archives.html** - Chronological article listing
6. **categories.html/category.html** - Category-based navigation
7. **tags.html/tag.html** - Tag-based navigation

## CSS Variables

The theme uses CSS custom properties for easy customization:

```css
:root {
  --site-title-font: 'ChusaLove', serif;
  --article-title-font: 'Binggrae', serif;
  --article-title-font-size: 1.8rem;
  --header-font: 'IBM Plex Sans', sans-serif;
  --body-font: 'NanumSquareNeo', sans-serif;
  --body-font-size: .95rem;
}
```

## Framework Dependencies

- **Bootstrap**: Responsive grid and components
- **Font Awesome**: Icon fonts for UI elements
- **Pygments**: Syntax highlighting for code blocks

## Customization Guidelines

When modifying this theme:

1. **Maintain Korean Typography**: Preserve Korean font selections and sizing
2. **Respect Template Structure**: Use the established template hierarchy
3. **Follow Bootstrap Conventions**: Maintain responsive grid patterns
4. **Update CSS Variables**: Use custom properties for consistent theming
5. **Test Mobile Layout**: Ensure responsive behavior across devices

## Template Variables

Key Pelican variables used throughout templates:

- `SITENAME`, `AUTHOR` - Site metadata
- `DEFAULT_LANG` - Language settings (ko-KR)
- `SITEURL` - Base URL for links
- `article.title`, `article.summary`, `article.tags` - Article metadata
- `article.locale_date`, `article.locale_modified` - Localized dates

## Integration Notes

This theme integrates with the main blog's configuration:
- Uses Korean timezone (Asia/Seoul)
- Supports both Markdown and reStructuredText
- Compatible with Mermaid.js diagrams
- Works with custom CLI management tools