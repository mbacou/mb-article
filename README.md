# mb-article Quarto Format (DRAFT)

Custom 3-column format for stand-alone Quarto HTML documents and website projects. The format provides an optional document header and places **all project branding and table-of-content on the left sidebar**. Colors and typography are controlled via `_brand.yml`. The default Bootstrap theme was modified slightly to improve vertical rythm. As with the built-in Quarto document type, the 3-column page design is fully responsive.

## Installing

```bash
quarto use template mbacou/mb-article
```

This will install the extension and create an example `.qmd` file that you can use as a starting place for your article.

## Using

The format provides the additional configuration options below (to be included in the document front matter or in a separate `_quarto.yml` per standard practices). This will display a minimum document header and brand on the left column..

```{yaml}
format:
  mb-article-html:
    logo: logo.png
    logo-href: ./    

    tools: 
      - icon: github
        href: ./tool-1
      - icon: telegram
        href: ./tool-2
      - icon: linkedin
        href: ./tool-3
    
    links:
      - text: Link 1
        icon: link
        href: ./link-1
      - text: Link 2
        icon: link
        href: ./link-2
      - text: Link 3
        icon: link
        href: ./link-3

    footer: |
      <strong>Mel B. Labs</strong> -- a personal blog about statistics
      and spatial econometrics.<br/>© 2026 
      <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en">
      CC BY-NC 4.0</a>        
```

## Example

Here is the source code for a minimal sample document [index.qmd](index.qmd).
