# Building and setting up mkdocs directory from scratch

* Install mkdocs tools  

  ```
  pip install mkdocs markdown-include mkdocs-alabaster mkdocs-bootstrap python-markdown-math mkdocs-material pymdown-extensions pygments
  ```

* Create new project

  ```
  python -m mkdocs new btp-manuals-md
  ```

* cd into the /docs directory (automatically created) in the new project you created.

  ```
  cd btp-manuals-md/docs
  ```

* Create directories required

  ```
  mkdir media css js modules
  mkdir media/icons media/logos
  ```

* Add any icons pngs or logo pngs to media/icons and  media/logos respectively.

* Make sure Workshop Information file preamble.md is located in docs directory

* Create a directory for each module. In addition, each module should contain an images directory. This will make both module and image directory:

  ```
  mkdir -p modules/btp-module-chip-seq/images
  mkdir -p modules/btp-module-ngs-cli/images
  mkdir -p modules/cancer-module-alignment/images
  ```

* Create a markdown file for each module in each module directory in /docs
  e.g. modules/btp-module-ngs-cli/commandline.md

* Any images for a module are located in the images directory in the module
  e.g. modules/btp-module-ngs-cli/images/x.png

* Edit default mkdocs.yml file with themes, extensions, styling and javascripts

* Edit pages in mkdocs.yml to control what is displayed.

* Edit docs/index.md to contain welcome info

* Add in any CSS files to docs/css folder

* Add in JS files to docs/js folder

* Deploy to *public* server

```
mkdocs gh-deploy --clean --message "Initial commit"
```
