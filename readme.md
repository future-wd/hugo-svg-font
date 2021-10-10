# Hugo SVG Font

usage (optionally .svg to svg paths)
path is relative to the resources folder. The following example shows defaults

```HTML
{{ partial "svg-font" (dict "svg" "icons/bootstrap/envelope" "em" 1 "block" false ) }}
```

As the example above uses defaults to you can use the following shortcut (pass the path as the partials context):

```HTML
{{ partial "svg-font" "icons/bootstrap/envelope" }}
```

optional

SVG width defaults to 1em (if the svg is 16px wide)

Set block to true if you are not using svg inline with text.

``` HTML
{{ partial "svg-font" (dict "svg" "icons/bootstrap/envelope" "em" 2 "block" true )}}
```
