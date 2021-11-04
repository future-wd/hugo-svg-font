# Hugo SVG Font

## Simple Partial Usage

The "source" path is relative to the resources folder.

```HTML
{{ partial "svg-font" "icons/bootstrap/envelope" }}
```

## Optional Arguments for Partial

To use the optional argument you must pass a dict as the partials context.

``` HTML
{{ partial "svg-font" (dict "src" "icons/bootstrap/envelope" "em" 2 "block" true "title" "Icon Title" "desc" "Icon Desc")}}
```

`src` points to the SVG file relative to the assets folder. The .svg suffix is optional.

`em` is for setting the width that the icon will be displayed at. The default is 1em which will display an svg at its native size.

`block` is set to true if you are not using svg inline with text. This enables `display:block`.

`title` adds a title tag which browsers pick up and display on hover. It also adds `aria-labelledby` to the SVG. (for assistive technology). The title is useful for desktop users, but does not add functionality for mobile users. (who aren't using assistive technology/screen readers)

`description` adds a description tag and adds `aria-describedby` to the SVG. (for assistive technology)

## Shortcode usage

{{< svg-font src="icons/bootstrap/envelope" em=2 block=true title="Icon Title" desc="Icon Desc" >}}

## Styling your icons

You need to wrap your partial or shortcode in a div or span and add CSS classes to change the size and color.

An example utilizing bootstrap 5's utility classes is as follows:

```HTML
<span class="fs-2 text-primary">{{ partial "svg-font" "icons/bootstrap/envelope" }}</span>
```

*fs-2 changes the font size for the svg and text-primary changes the line color to primary (blue by default).*

## Installation

### Import module

Ensure that you are importing v2 as v1 is depreciated and not maintained.

```YAML
# config.yaml
module:
  imports:
  - path: github.com/future-wd/hugo-svg-font/v2
```

### Import CSS

You need to import required css from `/assets/scss/svg-font.scss'

```SCSS
// /assets/scss/index.scss
@import "svg-font.scss";
```

Or instead run the following partial in the projects head to compile the scss (source map and non-compressed CSS provided for development use)

```HTML
{{- partial "svg-font/css" . }}
```
