# Ayling Family History Website

A simple, Jekyll-based family tree website hosted on GitHub Pages.

## Overview

This website is designed to document and share the Ayling family history. It uses Jekyll to generate a static website from markdown files and YAML data.

## Setup Instructions

### Local Development

1. Install Ruby and Jekyll (if not already installed):
   ```
   gem install jekyll bundler
   ```

2. Clone this repository:
   ```
   git clone https://github.com/aylingfamily/aylingfamily.github.io.git
   cd aylingfamily.github.io
   ```

3. Install dependencies:
   ```
   bundle install
   ```

4. Run the local development server:
   ```
   bundle exec jekyll serve
   ```

5. View the site at `http://localhost:4000`

### Deploying to GitHub Pages

1. Create a GitHub repository named `yourusername.github.io`
2. Push your code to the repository
3. Enable GitHub Pages in the repository settings
4. Your site will be available at `https://yourusername.github.io`

## How to Edit the Family Tree

### Adding a New Family Member

1. Add the person's information to `_data/family.yml` following the existing format
2. Create a new markdown file in the `_people` directory (e.g., `_people/jane_ayling.md`)
3. Add the person to the appropriate generation in the `generations` section of `family.yml`

### Person File Format

```markdown
---
layout: person
title: Person Name
person_id: person_id_from_family_yml
---

## Personal Life

Write about the person's life here.

## Career and Achievements

Write about career achievements here.

## Memories

Add quotes or memories here.
```

### Adding Photos

1. Add photos to the `assets/images` directory
2. Reference them in the `image` field of the person's entry in `family.yml`

## File Structure

- `_config.yml`: Jekyll configuration
- `_layouts/`: HTML templates for pages
- `_data/family.yml`: Family data in YAML format
- `_people/`: Individual markdown files for each person
- `assets/`: Images and CSS
- `index.md`: Homepage
- `tree.md`: Family tree visualization page

## Customization

- Edit `assets/css/style.css` to change the site's appearance
- Modify `_layouts` files to change page structure