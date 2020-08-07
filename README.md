# divinerites-lazyload

## About

- Use lazyloading if set in your project.

## Usage

### Using our buit-in lazyload librairy

- Add header and footer
- Config.toml option : `label = "lazy"`

```toml
# Include this in your config.toml

# Gestion lazyload
[params.global.lazyload]
   enable = true
   local = true
   label = "lazy"
```

File : in your `header` section

```go-html-template
<!-- HEADER Gestion du lazyloading des images -->
{{ partial "header_lazyload.html" . }}
```

File : in your `footer` section

```go-html-template
<!-- FOOTER : Pour Images avec/sans LazyLoading -->
{{ partial "footer_lazyload.html" . }}
```

### Using an other lazyload librairy

```toml
# Include this in your config.toml

# Gestion lazyload
[params.global.lazyload]
   enable = false
   label = "lozad"  #for eample used in meghna theme
```

### HTML template Usage

```go-html-template

```

### iframe

For iframe with the **built-in lazyload** : just add `class="lazy"`

### Credits

- Original idea : https://discourse.gohugo.io/t/responsive-lazy-loaded-images/26041
- lazyload : https://github.com/verlok/vanilla-lazyload
- Copyright © 2020 onwards, Didier Divinerites
