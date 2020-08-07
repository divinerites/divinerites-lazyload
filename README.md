# divinerites-lazyload

## About

- Use lazyloading in your project (images, iframes, ...)

## Usage

- Add a `params.global.lazyload` section in your `config.toml`
- Update `label` with the value your lazyload name
  - `lazy` for [vanillia-lazyload](https://github.com/verlok/vanilla-lazyload)
  - `lozad` for [lozad](https://github.com/ApoorvSaxena/lozad.js)

### Add a section in your `config.toml`

```toml
[params.global.lazyload]
   enable = true (only lazy at  the moment)
   local = true
   label = "lazy"  # lazy / lozad
```

### Call partials in your `<head>` and `<footer>`

```go-html-template
<head>
...
<!-- HEADER Manage images lazyloading -->
{{ partial "header_lazyload.html" . }}
...
</head>
```

```go-html-template
<footer>
...
<!-- FOOTER : For images with/without LazyLoading -->
{{ partial "footer_lazyload.html" . }}
...
</footer>
```

### iframe

For iframe with the **built-in lazyload** : just add `class="lazy"`

### Credits

- Original idea : https://discourse.gohugo.io/t/responsive-lazy-loaded-images/26041
  - vanilla lazyload : https://github.com/verlok/vanilla-lazyload
  - lozad : https://github.com/ApoorvSaxena/lozad.js (from meghna theme)
- Copyright © 2020 onwards, Didier Divinerites
