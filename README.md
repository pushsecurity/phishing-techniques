# Phishing Techniques Database

A comprehensive Jekyll static site documenting various phishing techniques, their analysis, and countermeasures. This site is designed to be hosted on GitHub Pages and provides an interactive table-based interface for exploring different phishing methods.

## Features

- **Interactive Table Interface**: Main page features a large table with clickable cells linking to technique pages
- **Individual Technique Pages**: Detailed markdown pages for each phishing technique at `/techniques/{technique-name}`
- **Responsive Design**: Modern, mobile-friendly design that works on all devices
- **GitHub Pages Ready**: Configured for easy deployment on GitHub Pages
- **SEO Optimized**: Built with Jekyll SEO tag for better search engine visibility

## Site Structure

```
phishing-techniques/
├── _config.yml              # Jekyll configuration
├── _layouts/                # Layout templates
│   ├── default.html         # Main layout
│   └── technique.html       # Technique page layout
├── _techniques/             # Technique markdown files
│   ├── spear-phishing.md
│   ├── whaling.md
│   └── ... (more techniques)
├── assets/
│   └── css/
│       └── style.css        # Site styling
├── index.html               # Main page with table
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

## Overview
Brief introduction to the technique...

## How It Works
Detailed explanation of the attack method...

## Real-World Examples
Examples of actual attacks...

## Detection and Prevention
How to detect and prevent this technique...

## Conclusion
Summary and key takeaways...
```

## Customizing the Site

### Modifying the Table

The main table is located in `index.html`. You can:
- Add new rows and columns
- Change the categories
- Modify the difficulty/effectiveness ratings
- Update links to technique pages

### Styling Changes

The site styling is in `assets/css/style.css`. Key sections include:
- **Header styling**: `.site-header`
- **Table styling**: `.techniques-table`
- **Technique page styling**: `.technique`
- **Responsive design**: Media queries at the bottom

### Configuration Options

Edit `_config.yml` to customize:
- Site title and description
- Base URL for deployment
- Jekyll settings
- Plugin configuration

## Table Structure

The main table is organized with the following columns:
- **Category**: Groups techniques by type (Email Phishing, Web Phishing, etc.)
- **Technique Type**: Specific technique names with links to detailed pages
- **Difficulty**: Implementation difficulty (Low, Medium, High, Very High)
- **Effectiveness**: Success rate of the technique
- **Detection**: How easily the technique can be detected

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
1. Check the [GitHub Issues](https://github.com/yourusername/phishing-techniques/issues)
2. Create a new issue with detailed information
3. Include steps to reproduce the problem

## Security Note

This site is for educational and research purposes only. The information provided should be used to understand and defend against phishing attacks, not to conduct them. Always ensure you have proper authorization before testing security measures in any environment.