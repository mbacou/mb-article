# mb-article Quarto Format (DRAFT)

Custom HTML format for Quarto standalone documents and websites that provides a simplified document header (optional), as well as project branding and TOC on the left sidebar. Colors and typography are controlled via `_brand.yml`. The default Boostrap theme was modified slightly to improve vertical rythm.

## Installing

```bash
quarto use template mbacou/mb-article
```

This will install the extension and create an example `.qmd` file that you can use as a starting place for your article.

## Using

The format provides the following custom options (to be included in document front matter or in `_quarto.yml` per standard practices). This will display a minimum document header.

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
```

Content on the left sidebar uses standard `website` configuration in `_quarto.yml`, e.g.

```{yaml}
website:
  sidebar:
    background: transparent
    logo: logo.png
    style: floating
    search: false
    footer: Brabd baseline description will show below branded logo
  other-links: 
    - href: ./
      icon: arrow-up-square-fill
      text: Back to top
    - href: "#quarto-appendix"
      icon: arrow-down-square-fill
      text: Appendix  
```

## Example

Here is the source code for a minimal sample document [index.qmd](index.qmd).
