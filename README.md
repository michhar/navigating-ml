## Welcome to Navigating ML

For the rendered site, go [here](https://michhar.github.io/navigating-ml).

For the site Readme, go [here](https://github.com/michhar/navigating-ml/edit/master/README.md).

### Building the site

To test locally:

1. Get mkdocs: `pip install mkdocs`
2. Get the Material theme: `pip install mkdocs-material`
3. In main folder run: `mkdocs serve`

Updating:

4. Modify any md's, add new ones, update mkdocs.yml if you do.
5. Test locally again with: `mkdocs serve`

Build and deploy:

6. Build: `mkdocs build --clean` which creates the `site` directory.
7. Copy files from `site` to `docs`.
8. Check into GitHub and voila.

