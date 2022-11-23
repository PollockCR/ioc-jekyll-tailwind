# Jekyll + CloudCannon + Tailwind + Docker Dev Container Boilerplate

## Dependencies

This boilerplate uses the following dependencies & plugins:

- Jekyll (~>4.3.1)
- TailwindCSS (^3.2.4)
- jekyll-postcss plugin

Detailed dependencies listed in the [Gemfile](./Gemfile) and [package.json](./package.json)
  
## Local project development

### Local dependencies

- Visual Studio Code
- Docker Desktop
- [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) Visual Studio Code extension
- [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) Visual Studio Code extnesion

### Local development

1. Open Docker Desktop

2. Open this folder in a Dev Container within VS Code

Run Jekyll:
```
$ bundle exec jekyll s
```
or `bundle exec jekyll s -l`, `bundle exec jekyll serve --livereload`


## Troubleshooting

### If running into the `Error: unterminated attribute selector for type` error:

Run `npm audit fix` to restore working order.

Often, cleaning the cache by deleting the `.jekyll-cache` folder will also allow to run the `build` or `serve` commands

### If running into the PostCSS error `Cannot load module`:

Delete both `node_modules` and `jekyll-cache` folders, run `npm i` and then start Jekyll server with `bundle exec jekyll s` 

### If running into the Jekyll error `SyntaxError: Unexpected end of JSON input` ... `Conversion error: Jekyll::Converters::PostCss encountered an error while converting 'css/main.css': unexpected token at ''` :

There is currently an [issue](https://github.com/mhanberg/jekyll-postcss/issues/16) where you need to use double quotes " instead of single quotes ' in your CSS