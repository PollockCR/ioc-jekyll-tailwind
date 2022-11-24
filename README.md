# Jekyll + CloudCannon + Tailwind + Docker Dev Container Boilerplate

## Dependencies

This boilerplate uses the following dependencies & plugins:

- Jekyll (~>4.3.1)
- TailwindCSS (^3.2.4)

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

3. In the terminal, run
    ```
    $ bundle install
    ```

4. Run Jekyll & Tailwind CLI concurrently:
    ```
    $ npm run dev
    ```

### Troubleshooting

#### **Jekyll changes not detected or displayed**
Run Jekyll & Tailwind CLI concurrently with polling:
```
$ npm run dev:poll
```
#### **Debug a Jekyll error**
Run the debug command
```
$ npm run dev:trace
```