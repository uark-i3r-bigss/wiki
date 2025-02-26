# BIGSS Wiki

The BIGSS Wiki is based on Hugo, and is hosted on Gitlab Pages.  
https://bigss.lcsr.wse.jhu.edu/wiki/

## How to contribute

You can add new pages, edit existing pages directly from the Gitlab interface. Or you can clone the repository, make your changes, and submit a merge request.

## How to build locally

Clone the repository with the `--recurse-submodules`:

```
git clone --recurse-submodules https://gitlab.lcsr.jhu.edu/bigss/bigss-wiki.git
```

You can build the wiki locally to preview your changes. You will need to install [Hugo](https://gohugo.io/) (Recommend installing `hugo` via Snap Package Manager), and then run the following command from the root of the repository:

```bash
hugo server
```

This will start a local web server on port 1313. You can then access the wiki page at http://localhost:1313/wiki/