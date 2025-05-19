# Portfolio Site with Jekyll and Minimal Mistakes

A minimalistic portfolio site built with Jekyll and the Minimal Mistakes theme, designed to be hosted on GitHub Pages.

## Features

- Responsive design
- Project showcase
- About page
- Contact form
- Custom styling
- GitHub Pages ready

## Installation

### Prerequisites

- Ruby (version 2.5.0 or higher)
- RubyGems
- Bundler

### Setup

1. Clone this repository
   ```bash
   git clone https://github.com/username/portfolio-site.git
   cd portfolio-site
   ```

2. Install dependencies
   ```bash
   bundle install
   ```

3. Run the site locally
   ```bash
   bundle exec jekyll serve
   ```

4. View the site at `http://localhost:4000`

## Customization

### Site Configuration

Edit `_config.yml` to update site settings, personal information, and social media links.

### Content

- **Projects**: Add or modify project details in `_pages/projects.md`
- **About**: Update your information in `_pages/about.md`
- **Contact**: Customize the contact form in `_pages/contact.md` (remember to update the Formspree endpoint)

### Navigation

Edit `_data/navigation.yml` to update the main navigation menu.

### Styling

Custom styles are located in `assets/css/main.scss`. You can adjust the theme skin in `_config.yml`.

## Deployment to GitHub Pages

1. Create a new repository on GitHub named `username.github.io`
2. Update the `url` and `baseurl` in `_config.yml`:
   ```yaml
   url: "https://username.github.io"
   baseurl: ""  # or /portfolio if not using username.github.io
   ```
3. Push your code to the repository:
   ```bash
   git remote set-url origin https://github.com/username/username.github.io.git
   git push -u origin main
   ```
4. In your GitHub repository, go to Settings > Pages and ensure your site is being built from the main branch

## License

This project is open source and available under the [MIT License](LICENSE). 