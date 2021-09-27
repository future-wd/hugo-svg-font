# Hugo SVG Font

usage (don't add .svg to svg paths)

```
{{ partial "svg-font" (dict "svg" "icons/bootstrap/envelope")}}
```

optional

SVG width defaults to 1em (if the svg is 16px wide)

Set block to true if you are not using svg inline with text.

```
{{ partial "scripts/svg-font" (dict "svg" "icons/bootstrap/envelope" "em" 1 "block" true/false )}}
```