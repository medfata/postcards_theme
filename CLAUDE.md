# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Codebase Overview

This is a Shopify theme called "Shapes" (v3.0.0) by Switch Themes, customized for Postcards Shop - a candle company selling Hawaiian-inspired scents. The theme is a comprehensive e-commerce implementation with advanced features for product presentation, marketing, and user experience.

## Theme Structure

### Core Shopify Directories
- `assets/` - CSS, JS, fonts, and media files including bundled JS modules and theme-specific assets
- `config/` - Theme configuration files (`settings_schema.json`, `settings_data.json`)
- `layout/` - Base theme templates and GemPages/third-party layout variants
- `locales/` - Internationalization files for multiple languages (DA, DE, ES, FR, IT, NL, PT-BR, PT-PT)
- `sections/` - Reusable theme sections for different page components
- `snippets/` - Small, reusable template components
- `templates/` - Page-specific templates and their JSON configurations

### Template Architecture

**Template Variants:**
- Standard Shopify templates (`.json` files)
- GemPages variants (prefixed with `gem-` or `gp-`)
- Custom templates for specific pages (`postcards.json`, `postcards-packs.json`, etc.)
- Backup templates (`gem-backup-default.json`)

**Section Types:**
- `main-*` sections for core page functionality
- `ss-*` sections (custom Switch Themes sections)
- Standard content sections (hero, featured collections, testimonials)
- Marketing sections (countdown bars, scrolling text, video embeds)

### Key Components

**Product System:**
- Modular product blocks (`product-block-*.liquid` snippets)
- Variant selection and quick-buy functionality  
- Product tile system with hover effects and animations
- Savings tags and promotional badges
- Pack/bundle product support

**Navigation & Layout:**
- Header/footer group configurations
- Mobile-responsive drawer navigation
- Predictive search functionality
- Localization support

**Interactive Features:**
- Island architecture for JavaScript components (`island-*.bundle.js`)
- PhotoSwipe gallery integration
- Video embeds (Vimeo, YouTube)
- Custom animations and shape effects

## Third-Party Integrations

The theme includes several app integrations:
- **GemPages** - Page builder (`gp-*` prefixed files)
- **Instafeed** - Instagram feed integration
- **Okendo** - Reviews system
- **Klaviyo** - Email marketing
- **GoAffPro** - Affiliate marketing
- **Accessibly** - Accessibility features
- **Alia** - Customer account features

## Development Patterns

### Liquid Conventions
- Extensive use of `liquid` tags for logic
- Metafields for product customization (`product.metafields.metadata.*`)
- Snippet-based component architecture
- Schema-driven section configuration

### Styling System
- CSS custom properties for theme variables
- Responsive design with mobile-first approach
- Shape and animation systems
- Color scheme variants (6 predefined schemes)

### JavaScript Architecture
- ES modules with dynamic imports
- Event-driven cart updates (`theme:update:cart`)
- Island components for specific functionality
- Theme event system for custom interactions

## Common Development Tasks

### Theme Deployment
This is an exported Shopify theme - use Shopify CLI or theme development tools:
```bash
shopify theme serve    # Local development
shopify theme push     # Deploy to store
shopify theme pull     # Sync from store
```

### Working with Sections
- Sections are configured via JSON schema
- Use existing section patterns as templates
- Test responsive behavior across devices
- Validate color scheme compatibility

### Product Customization
- Product variants managed through `product-template.liquid`
- Savings/promotional tags configured via section settings
- Metafields used for additional product data
- Bundle/pack products have specialized templates

### App Integration
- Check `config/settings_data.json` for app block configurations  
- GemPages sections use custom prefixed naming
- Review app-specific snippets before modifications

## Browser Support & Performance
- Modern browser features with progressive enhancement
- Lazy loading for images and videos
- Bundle optimization with ES module shims
- Critical CSS inlining support

## Important Notes
- Always test changes across multiple color schemes
- Preserve existing metafield structures when modifying product templates
- GemPages files should generally not be modified directly
- Theme uses Switch Themes documentation: https://help.switchthemes.co/shapes/