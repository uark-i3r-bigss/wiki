# BIGSS Wiki

The BIGSS Wiki (based on Hugo) is now hosted on Github Pages.  
https://jhu-bigss.github.io/wiki/

## How to contribute

You can add new pages, edit existing pages directly from the Gitlab interface. Or you can clone the repository, make your changes, and submit a merge request.

## How to build locally

Clone the repository with the `--recurse-submodules`:

```
git clone --recurse-submodules https://github.com/jhu-bigss/wiki.git
```

You can build the wiki locally to preview your changes. You will need to install [Hugo](https://gohugo.io/) (Recommend installing `hugo` via Snap Package Manager), and then run the following command from the root of the repository:

```bash
hugo server
```

This will start a local web server on port 1313. You can then access the wiki page at http://localhost:1313/wiki/