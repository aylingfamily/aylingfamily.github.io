# Ayling Family History Website

This repository contains the source code for the Ayling Family History website, which documents the history of the Ayling family's journey from England to Canada and their connection to Devil Lake.

## Overview

The site is built using Jekyll, a static site generator that transforms markdown content into a fully-functional website. The content focuses on:

- The ancestry and descendants of Henry Ayling and Ellen Eliza Ayres
- The family's immigration from England to Canada in 1906
- The Devil Lake property and cottage, which has been in the family since 1916
- Family photos, documents, and memorabilia

## Local Development

To run this site locally for development:

1. Install Jekyll and its dependencies (you'll need Ruby):
   ```
   gem install jekyll bundler
   ```

2. Clone the repository:
   ```
   git clone https://github.com/aylingfamily/aylingfamily.github.io.git
   cd aylingfamily.github.io
   ```

3. Install the site dependencies:
   ```
   bundle install
   ```

4. Start the local development server:
   ```
   bundle exec jekyll serve
   ```

5. View the site at [http://localhost:4000](http://localhost:4000)

## Site Structure

- `_config.yml` - Jekyll configuration file
- `_layouts/` - Contains the HTML templates for the pages
- `_includes/` - Contains reusable HTML components
- `assets/` - Contains CSS, JavaScript, and images
- `*.md` - Markdown content files for each page

## Adding Content

### Photos

To add photos to the site:

1. Place image files in the `assets/images/` directory
2. Reference them in markdown files using:
   ```
   ![Image description](/assets/images/filename.jpg)
   *Caption text here*
   ```

### Editing Content

All content is written in Markdown format. To edit a page:

1. Find the corresponding `.md` file
2. Edit the file using Markdown syntax
3. Commit and push your changes

## Deployment

This site is hosted on GitHub Pages and automatically deploys when changes are pushed to the main branch. No additional build steps are required.

## Contributing

If you have family history, photos, or documents to contribute:

1. Submit them via email to the site maintainers
2. Or, if you're familiar with GitHub, create a pull request with your additions

## License

This content is family property and not licensed for public use without permission.

## Contact

For questions or contributions, please contact:
- Jim Ayling - jrayling@example.com
- Lynn Ayling Hayes - lynnhayes@example.com