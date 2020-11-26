# gh-md-to-moodle

A tool to convert markdown to a `html` in GitHub style markdown.

## Installation

```console
pip install git+https://github.com/theendlessriver13/gh-md-to-moodle.git@1.0.0
```

## Usage

- accessible via the command line with `gh-md-to-moodle`

  ```console
  $ gh-md-to-moodle --help
  usage: gh-md-to-moodle [-h] [-V] origin destination

  positional arguments:
  origin         markdown file to be converted
  destination    path to output directory

  optional arguments:
  -h, --help     show this help message and exit
  ```

- first positional argument is `origin` which should point at the markdown file
- second positional argument is `destination` which should point at the destination file
- copy the file contents into the moodle text editor of text pages
  - it will not render correctly in the preview due to the `js` functions

### How does it work?

- this tool uses the python package [gh-md-to-html](https://pypi.org/project/gh-md-to-html/) to convert the markdown to `html`
- after this some JavaScript is added
  - the JavaScript appends another stylesheet to the loaded page and adds some inline css. This allows the page to render in GitHub styled markdown.

## Not implemented yet

- images are not supported yet
