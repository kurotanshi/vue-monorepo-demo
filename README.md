# Project structure of a Vue.js monorepo project demo

This project has a monorepo structure with a packages directory that contains multiple applications. Each application has its own README.md file, index.html, and index.js file, as well as its own dependencies under the node_modules directory. The applications also share common components and utilities.

Each application has its own package.json file and a public directory containing a favicon.ico file. The src directory contains the source code of the application, including assets, components, main JavaScript file, and stores. The vite.config.js file is the configuration file for the Vite build system.

The dist directory contains the built files of the application, including HTML, JavaScript, CSS, and favicon.ico files.

## Project Setup

```sh
pnpm install
```

### Compile and Hot-Reload for Development

```sh
pnpm dev:app-1
```

```sh
pnpm dev:app-2
```

```sh
pnpm dev:app-3
```

### Compile and Minify for Production

```sh
pnpm build:app-1
```

```sh
pnpm build:app-2
```

```sh
pnpm build:app-3
```
