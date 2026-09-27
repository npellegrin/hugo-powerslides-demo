# Hugo PowerSlides Demo

A demonstration site for the [`hugo-powerslides`](https://github.com/npellegrin/hugo-powerslides) Hugo theme.

## Requirements

- Hugo Extended
- Go
- Git

Check your installation:

```bash
hugo version
go version
```

## Local theme development

During development, the demo uses the local theme repository through a Go `replace` directive.

```go
module github.com/npellegrin/hugo-powerslides-demo

go 1.22

replace github.com/npellegrin/hugo-powerslides => ../hugo-powerslides
```

The relative path must point to the local theme directory.

### Import the theme

In `hugo.toml`:

```toml
[module]
  [[module.imports]]
    path = "github.com/npellegrin/hugo-powerslides"
```

### Start the development server

```bash
hugo mod tidy
hugo server
```

When using local file with `replace` directive, changes made in the local `hugo-powerslides` repository are automatically used by the demo.
