# Kotlin2Docset

## Kotlin Docset generator for Dash

### Requirements

- Python 3
- BeautifulSoup
- Pretty decent internet connection

### Usage

In order to start docset build process, run:

```bash
python3 kotlin2docset.py
```

This will start querying main [KotlinLang pages](https://kotlinlang.org/api/latest/jvm/stdlib/). The process itself
takes a lot of time, since all the URLs are queried one by one.

After webpages are downloaded, HTML files are parsed and mapped by assigned elements to proper docset categories (
methods, classes, etc). Then, a docset file is generated in the script's main directory.

### Changes after docset is generated

After docset generation, find `styles.css` file and append:

```css
/* header & nav */
header {
    display: none !important;
}

.docs-nav,
.docs-nav-new {
    display: none;
}

/* side */
.g-3 {
    display: none;
}

/* content */
.page-content {
    width: 100%;
}

.g-layout {
    width: 85%;
    padding: 40px;
}
```

## Adding By

- [Add an Icon](https://kapeli.com/docsets#addingicon)