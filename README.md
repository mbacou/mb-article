# mb-article Quarto Format

Custom 3-column format for Quarto HTML documents and website projects. The format provides an optional document header and places **all project branding and table-of-content on the left sidebar**. Colors and typography are controlled via `_brand.yml`. The default Bootstrap theme was modified slightly to improve vertical rythm. As with the built-in Quarto document type, the 3-column page design is fully responsive.

## Installing

```bash
quarto use template mbacou/mb-article
```

This will install the extension and create an example `.qmd` file that you can use as a starting place for your article.

## Using

This format provides additional configuration options, as shown below (to be included in the document front matter or in a project-level `_quarto.yml` file per standard practices). This will display a minimum document header, as well as branding and footer in the left column (sidebar).

```{yaml}
format:
  mb-article-html:
      logo: logo.svg
      logo-href: ./
      footer: |
        <strong>Mel B. Labs</strong> -- a personal blog about statistics
        and spatial econometrics.      
      header:
        palette: true      // show Bootstrap semantic colors
        left:
          - text: Link 1
            icon: link
            href: ./
          - text: Link 2
            icon: link
            href: ./
          - text: Link 3
            icon: link
            href: ./         
        right: 
          - icon: github
            href: https://github.com/mbacou/mb-article
          - icon: telegram
            href: https://t.me/mbacou
          - icon: linkedin
            href: https://linkedin.com/in/mbacou
          - icon: youtube
            href: https://youtube.com/\@mbacou/playlists
```

## Example

Here is the source code for a minimal sample document [index.qmd](index.qmd).
