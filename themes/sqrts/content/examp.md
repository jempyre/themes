<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <p>
      For example, `layouts/shortcodes/myshortcode.html`
      will be called with either
      `{{< myshortcode />}}` or
      `{{% myshortcode /%}}`
      depending on the type of parameters you choose.
    </p>
    <p>Lookup Order
      <code>
        `/layouts/shortcodes/<SHORTCODE>.html`
        `/themes/<THEME>/layouts/shortcodes/<SHORTCODE>.html`
      </code>
      <code>
        `{{ with .Get "class"}} class="{{.}}"{{ end }}`
        `{{ or .Get "title" | .Get "alt" | if }} alt="{{ with .Get "alt"}}{{.}}{{else}}{{.Get "title"}}{{end}}"{{ end }}`
        `{{< innershortcode />}}`
        `$.Page.Params.shortcode_color`
        `$.Page.Site.Params`
        ```
        {{ if .IsNamedParams }}
        <img src="{{.Get "src" }}" alt="">
        {{ else }}
        <img src="{{.Get 0}}" alt="">
        {{ end }}
        ```
        `.Parent` <!-- for nested codes -->
        `
        `{{ now.Format "2006" }}`

      </code>
    </p>
  </body>
</html><!--

-->
