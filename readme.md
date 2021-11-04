# Hugo SVG Font

## Usage

The `src` path is relative to the resources folder. The following example shows defaults

```HTML
{{ partial "svg-font" (dict "src" "icons/bootstrap/envelope" "em" 1 "block" false ) }}
```

As the example above uses defaults to you can use the following shortcut (pass the path as the partials context):

```HTML
{{ partial "svg-font" "icons/bootstrap/envelope" }}
```

## Optional

SVG width defaults to 1em (if the svg is 16px wide)

Set block to true if you are not using svg inline with text.

``` HTML
{{ partial "svg-font" (dict "src" "icons/bootstrap/envelope" "em" 2 "block" true )}}
```

## Installation

### Import module

```YAML
# config.yaml
module:
  imports:
  - path: github.com/future-wd/hugo-svg-font/v2
```

### Import CSS

You need to import required css from `/assets/scss/svg-font.scss'

```SCSS
// importing from index.html in /assets/scss/index.scss
@import "svg-font.scss";
```

Or instead run the following partial in the projects head to compile the scss (source map and non-compressed CSS provided for development use)

```HTML
{{- partial "svg-font/css" . }}
```
