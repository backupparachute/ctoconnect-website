# CTO Connect Website

A modern, responsive website for CTO Connect - Your On-Call Fractional CTO service. Built with Jekyll and Bootstrap 5.

## About CTO Connect

CTO Connect provides direct access to Kyle Miller's 25+ years of experience delivering software for Fortune 500s, hedge funds, government agencies, and fast moving startups. For just $99/month, you get unlimited email requests and weekly group calls to help your team get unstuck and stay on track.

## Features

- **Responsive Design**: Built with Bootstrap 5 for mobile-first design
- **Modern UI**: Clean, professional design with smooth animations
- **SEO Optimized**: Built-in SEO tags and meta descriptions
- **Fast Loading**: Optimized for performance
- **Contact Form**: Ready-to-use contact form
- **GitHub Pages Ready**: Configured for easy deployment

## Technology Stack

- **Jekyll**: Static site generator
- **Bootstrap 5**: CSS framework
- **Font Awesome**: Icons
- **Google Fonts**: Typography (Inter font family)
- **Jekyll SEO Tag**: SEO optimization
- **Jekyll Sitemap**: Automatic sitemap generation
- **GitHub Pages**: Hosting platform

## Local Development

### Prerequisites

- Ruby (2.7 or higher)
- RubyGems
- Bundler

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ctoconnect-website.git
   cd ctoconnect-website
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Start the development server:
   ```bash
   bundle exec jekyll serve
   ```

4. Open your browser and navigate to `http://localhost:4000`

### Building for Production

```bash
bundle exec jekyll build
```

The built site will be in the `_site` directory.

## Deployment

### GitHub Pages

1. Push your code to a GitHub repository
2. Go to Settings > Pages
3. Select "Deploy from a branch"
4. Choose the `main` branch and `/ (root)` folder
5. Click "Save"

The site will be available at `https://yourusername.github.io/repository-name`

### Custom Domain

To use a custom domain (like ctoconnect.io):

1. Add your domain to the `CNAME` file in the root directory
2. Configure your DNS settings to point to GitHub Pages
3. Update the `url` in `_config.yml` to match your domain

## Project Structure

```
ctoconnect-website/
├── _config.yml          # Jekyll configuration
├── _layouts/            # Layout templates
│   └── default.html     # Main layout
├── assets/              # Static assets
│   └── images/          # Images
│       └── cto-dots-logo.png
├── index.html           # Homepage
├── about.html           # About page
├── 404.html             # Custom error page
├── CNAME                # Custom domain configuration
├── robots.txt           # SEO file
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Customization

### Colors

The site uses Bootstrap 5's default color scheme with custom CSS variables defined in the layout file. You can modify the colors by editing the `:root` variables in `_layouts/default.html`.

### Content

- **Homepage**: Edit `index.html` to modify the main content
- **About Page**: Edit `about.html` for the about page content
- **Site Configuration**: Update `_config.yml` for site-wide settings

### Logo

Replace `assets/images/cto-dots-logo.png` with your own logo. The site is configured to use this logo in the navigation and various sections.

## SEO

The site includes:

- Meta descriptions for each page
- Open Graph tags for social media sharing
- Structured data markup
- Semantic HTML structure
- Fast loading times

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions about this website or CTO Connect services, contact:

- Email: kyle@ctoconnect.io
- Website: https://ctoconnect.io

---

Built with ❤️ using Jekyll and Bootstrap 5