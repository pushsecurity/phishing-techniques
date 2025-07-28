# Phishing Techniques Database

A comprehensive Jekyll static site documenting various phishing techniques, their analysis, and countermeasures. This site is designed to be hosted on GitHub Pages and provides an interactive matrix-based interface for exploring different phishing methods across multiple attack phases.

## Features

- **Interactive Matrix Interface**: Main page features a comprehensive table with clickable cells linking to technique pages
- **Multi-Phase Analysis**: Techniques organized across 8 key phases: Targeting, Link Delivery, Link Camouflage, TI Evasion, Anti-Analysis, Page Obfuscation, Defeat MFA & CA, and Account Takeover
- **Individual Technique Pages**: Detailed markdown pages for each phishing technique at `/techniques/{technique-name}`
- **Push Security Branding**: Clean, professional design matching the Push Security aesthetic
- **Responsive Design**: Modern, mobile-friendly design that works on all devices
- **GitHub Pages Ready**: Configured for easy deployment on GitHub Pages
- **SEO Optimized**: Built with Jekyll SEO tag for better search engine visibility

## Site Structure

```
phishing-techniques/
├── _config.yml              # Jekyll configuration
├── _layouts/                # Layout templates
│   ├── default.html         # Main layout with Push Security branding
│   └── technique.html       # Technique page layout
├── _techniques/             # Technique markdown files
│   ├── apps-weak-security.md
│   ├── email-legitimate-app.md
│   ├── trusted-website-hosting.md
│   ├── bot-protection.md
│   ├── dom-structure-changes.md
│   ├── aitm-phishing.md
│   ├── session-theft.md
│   └── ... (more techniques)
├── assets/
│   └── css/
│       └── style.css        # Site styling with Push Security theme
├── index.html               # Main page with technique matrix
├── Gemfile                  # Ruby dependencies
└── README.md               # This file
```

## Getting Started

### Prerequisites

- Ruby (version 2.6 or higher)
- RubyGems
- Git

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/phishing-techniques.git
   cd phishing-techniques
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run the development server**
   ```bash
   bundle exec jekyll serve
   ```

4. **View the site**
   Open your browser and navigate to `http://localhost:4000`

### GitHub Pages Deployment

1. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Enable GitHub Pages**
   - Go to your repository settings on GitHub
   - Navigate to "Pages" in the sidebar
   - Select "Deploy from a branch"
   - Choose the `main` branch and `/ (root)` folder
   - Click "Save"

3. **Update site URL** (Optional)
   - Edit `_config.yml`
   - Update the `url` field with your actual GitHub Pages URL

## Adding New Techniques

### Creating a New Technique Page

1. **Create a new markdown file** in the `_techniques/` directory
   ```bash
   touch _techniques/your-technique-name.md
   ```

2. **Add front matter** to the file:
   ```yaml
   ---
   layout: technique
   title: Your Technique Name
   description: Brief description of the technique
   ---
   ```

3. **Write your content** using Markdown syntax

4. **Update the main table** in `index.html` to include a link to your new technique

### Example Technique Page Structure

```markdown
---
layout: technique
title: Example Technique
description: Brief description of the technique
---

# Example Technique

## Summary

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

## Examples

- [Example 1: Real-world case study](https://example.com/case-study-1)
- [Example 2: Technical analysis](https://example.com/technical-analysis)
- [Example 3: Detection methods](https://example.com/detection-methods)
```

## Customizing the Site

### Modifying the Matrix

The main technique matrix is located in `index.html`. You can:
- Add new rows representing different attack scenarios
- Add new columns for additional attack phases
- Update technique names and descriptions
- Modify links to technique pages
- Reorganize techniques across different phases

### Styling Changes

The site styling is in `assets/css/style.css` and follows the Push Security design system. Key sections include:
- **Header styling**: `.site-header` (black background with orange accents)
- **Matrix styling**: `.techniques-table` (orange headers, white cells with orange borders)
- **Technique page styling**: `.technique` (clean, professional layout)
- **Button styling**: `.btn-primary` (orange buttons with hover effects)
- **Responsive design**: Media queries for mobile and tablet devices

### Configuration Options

Edit `_config.yml` to customize:
- Site title and description
- Base URL for deployment
- Jekyll settings
- Plugin configuration

## Matrix Structure

The main technique matrix is organized with the following columns representing different phases of phishing attacks:

- **Targeting**: Initial target selection and reconnaissance techniques
- **Link Delivery**: Methods used to deliver malicious links to targets
- **Link Camouflage**: Techniques to disguise or obfuscate malicious URLs
- **TI Evasion**: Threat Intelligence evasion methods
- **Anti-Analysis**: Techniques to prevent automated analysis and detection
- **Page Obfuscation**: Methods to hide or disguise malicious page content
- **Defeat MFA & CA**: Techniques to bypass Multi-Factor Authentication and Conditional Access
- **Account Takeover**: Final methods used to gain unauthorized access

Each cell in the matrix contains clickable links to detailed technique pages, allowing users to explore specific methods within each attack phase.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-technique`)
3. Add your technique or improvements
4. Commit your changes (`git commit -am 'Add new technique'`)
5. Push to the branch (`git push origin feature/new-technique`)
6. Create a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you encounter any issues or have questions:
1. Check the [GitHub Issues](https://github.com/jacques/phishing-techniques/issues)
2. Create a new issue with detailed information
3. Include steps to reproduce the problem

## Design System

This site uses the Push Security design system with:
- **Primary Color**: Black (`#000000`) for headers and footers
- **Accent Color**: Orange (`#FF6600`) for buttons, headers, and highlights
- **Typography**: Clean sans-serif fonts for optimal readability
- **Layout**: Minimalist design with clear visual hierarchy

## Security Note

This site is for educational and research purposes only. The information provided should be used to understand and defend against phishing attacks, not to conduct them. Always ensure you have proper authorization before testing security measures in any environment.