---
title: Explainer videos
subtitle: Comprehensive guide to installing, utilizing, and customizing the Knowledge Base Jekyll theme available for purchase on ThemeForest.
date: 2023-05-26
lastmod: 2023-06-03
author: joshua
---

## Setup
### Installation and development

Install the Jekyll with [Bundler](http://bundler.io/):

```bash
bundle install
```

Install dependencies:
`npm install`

To start developing: 
`npm run dev`

To get out of developing mode you need to do **Ctrl+c** twice.

You can find more on [Deployment Methods](https://jekyllrb.com/docs/deployment-methods/) page on Jekyll website.

## Basic theme setup

### Site details
Add your site details in `_config.yml`:

```yaml
# Site title and description
title: My Site
description: Customer docs Jekyll theme.

# Site subpath, e.g. /blog
baseurl: ""

# Site base hostname & protocol, e.g. http://example.com
url: ""
```

### Update favicon
You can find the current favicons inside the `/uploads/` directory, just replace it with your new favicons.

### Update logo
The theme uses two logo files one larger for desktop and one smaller mark logo for mobile. If you don't intend to use mark logo, set the same logo file for both.

Add your logo image files to `/uploads/` directory, then specify the logo files in `_config.yml`:

```yaml
logo: /uploads/logo-main.svg
logo_mark: /uploads/logo-mark.svg
```

### Navbar navigation 
Set in the main navigation links in `_data/navbar.yml`:

```yaml
# Top level links
- text: Contact
  url: "/contact/"
- text: Dropdown
  dropdown: # Dropdown links
  - text: Getting started
    url: "/getting-started/"
    icon: rocket-launch
  - text: Code tutorials
    url: "/getting-started/"
    icon: academic-cap
```

### Footer
Set footer navigation links and content in `_data/footer.yml`:

```yaml
copyright: "&copy; 2023 Knowledge"
description: Jekyll documentation theme for organizations, startups, and personal projects.
menus:
- heading: Services
  links:
  - text: Applications
    url: "/somelink/"
  - text: Work
    url: "/somelink/"
```

Documentation sidebar menu is set in `_data/navigation_docs.yml`:
```yaml
- title: Introduction
  icon: square-3-stack-3d
  description: Sint ipsa praesentium dolor error cumque velit tenetur quaerat.
  docs:
  - getting-started
  - doc-22
  - doc-23

- title: Code tutorials
  icon: academic-cap
  description: Sint ipsa praesentium dolor error cumque velit tenetur quaerat.
  docs:
  - doc-7
  - doc-8
```

The icons are located in `_includes/icons/` folder, when specifying icons in block reference only the icon file name without the `.svg` extension.

### Analytics
Theme support Google analytics, enable by setting ID in `_config.yml`:
```yaml
google_analytics:  ANALYTICS_ID
```

## Content

### Authors
Set author in post front matter, reference author `username` from `_data/authors.yml`:
```yaml
author: joshua
```

Add authors in `_data/authors.yml`:
```yaml
joshua:
  name: Joshua Birdman
  image: /uploads/joshua.jpg
peter:
  name: Peter Goodman
  image: /uploads/peter.jpg
```

### Blocks

Theme uses blocks layout as source of content for pages. The blocks layout and contents are defined in page front matter. Set the page layout to `layout: blocks`. Available blocks: `cards, contact-form, contact-info, cta, faq, navigation`.

Example CTA block:
```yml
blocks:
- block: cta
  heading: Ready to get started?
  copy: Morbi eget neque vel turpis lacinia eget neque vel turpis lacinia lacinia eget neque.
  icon: thin-rocket
  button:
    text: Get started
    url: "#"
```

All block demos are included in the theme pages. New site blocks can be added in `_includes/blocks/` directory.

### Icons
Some blocks have options to display icons, the icons are located in `_includes/icons/` folder, when specifying icons in block reference only the icon file name without the `.svg` extension.

### Contact form
Contact form is setup and ready to use with [Netlify](https://www.netlify.com/) hosting.

### Documentation content
Documentation pages are located in `_docs/` directory. For general markdown syntax see [Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).


## Customization

### String translation
Set your language code in `_config.yml`:
```yml
lang: en
```
Theme strings can be translated in `_data/translation.yml`, copy the current English translation and paste it bellow the Eglish translation, then replace `en` with you language code that you set in `_config.yml` and translate the strings.

### Code highlighter style
The highlighter is set in `_config.yml`:
```yml
highlighter: rouge
```
Styles are located in `assets/css/main.css`

### Brand colors
Theme uses TailwindCSS default colors:
```txt
text-sky-500
text-sky-600
bg-sky-500
bg-sky-600
bg-sky-700
```

Search and replace the colors or modify sky colors in `tailwind.config.js`:
```js
theme: {
  extend: {
    colors: {
      sky: {
        500: '#0ea5e9',
        600: '#0284c7',
        700: '#1d4ed8',
      }
    }
  }
}
```

## Support
Customer support is provided through our Envato item support tab for up to six months from the purchase date and is provided Monday to Friday during the business week. We aim to answer all support requests daily, most are handled within 24h.

Please note items downloaded from Envato Elements are not supported so you will be unable to get assistance with technical questions, installation, third-party assets or direct guidance.

Before contacting support please:

- Read this documentation
- Describe your problem in detail
- Include links
- Attach screenshot