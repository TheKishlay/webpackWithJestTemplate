---
layout: default
title: "Webpack Vanilla JS Template"
description: "A minimal, zero-config starter for vanilla JavaScript with Webpack, featuring separate development & production builds."
---

<!-- PROJECT BADGES -->
[![npm version](https://badge.fury.io/js/webpack.svg)](https://badge.fury.io/js/webpack)
[![license: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![build:dev](https://img.shields.io/badge/build-development-green.svg)](#)
[![build:prod](https://img.shields.io/badge/build-production-blue.svg)](#)

# 📦 Webpack Vanilla JS Template

A minimal, zero-configuration starter template for building **vanilla JavaScript** applications with **Webpack**, offering:

- 🔄 Separate **development** & **production** builds  
- ⚡️ Hot Module Replacement (HMR)  
- 📄 HTML template processing  
- 🎨 CSS bundling & extraction  
- 🔒 Asset minification & cache-busting  
- 🧪 Jest testing support
- 📦 ES6+ module support via Babel
---

## 📁 Repository Structure

```text
.
├── dist/                   # Production build output (auto-generated)
├── src/                    # Source files
│   ├── index.js            # Webpack entry point
│   ├── style.css           # Global styles
│   └── template.html       # HTML template for HtmlWebpackPlugin
├── webpack.dev.js          # Development webpack configuration
├── webpack.prod.js         # Production webpack configuration
├── package.json            # Project metadata & scripts
├── .gitignore              # Files & folders to ignore in Git
└── README.md               # This file
```

## 🚀 Quick Start

### 1. Clone the repo  
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Install dependencies

```bash
npm install
```

### 3. Development
```bash
npm run start
```

- Launches `webpack-dev-server` at [http://localhost:8080](http://localhost:8080)
- Enables **Hot Module Replacement (HMR)** and **inline source maps**

### 4. Production Build
```bash
npm run build
```

- Bundles and optimizes assets into `dist/`
- Minifies JS (Terser) & CSS (`css-minimizer-webpack-plugin`)
- Uses content-hashed filenames for cache-busting

---

## ⚙️ Configuration Details

### Entry Point
- `src/index.js` — imports styles and application logic.

### HTML Template
- `src/template.html` — base HTML processed by `html-webpack-plugin` to inject script and style tags.

### Stylesheet
- `src/style.css` — global CSS, extracted into a separate file in production by `mini-css-extract-plugin`.

### Webpack Configurations

| Config File        | Mode         | Key Features                                                      |
|--------------------|--------------|--------------------------------------------------------------------|
| `webpack.dev.js`   | development  | `devtool: 'inline-source-map'`, `webpack-dev-server`, HMR          |
| `webpack.prod.js`  | production   | CSS extraction, JS/CSS minification, content hashing, tree shaking |

## 📦 NPM Scripts

| Script | Command         | Description                             |
|--------|-----------------|-----------------------------------------|
| test   | `npm test`      | Run Jest tests once                     |
| watch  | `npm run watch` | Run Jest tests in watch mode            |
| start  | `npm run start` | Run dev server with live reload & HMR   |
| build  | `npm run build` | Create optimized production build in `dist/` |

---

## 📜 Dependencies & Plugins

### Core
- `webpack`
- `webpack-cli`
- `webpack-dev-server`
- `@babel/core` & `@babel/preset-env` - For ES6+ module support
- `jest` & `babel-jest` - For testing support

### HTML
- `html-webpack-plugin`

### CSS
- `css-loader`
- `style-loader`
- `mini-css-extract-plugin`

### Optimization
- `terser-webpack-plugin`
- `css-minimizer-webpack-plugin`

> See `package.json` for exact versions.

## 📦 Testing & Development Setup

### Jest Testing
This template includes Jest testing support. To run tests:

```bash
# Run all tests once
npm test

# Run tests in watch mode
npm run watch
```

### ES6+ Module Support
The template uses Babel to transpile ES6+ modules. Your JavaScript files can use modern JavaScript features including:

- ES6 modules (`import`/`export`)
- Arrow functions
- Template literals
- Destructuring
- Classes
- Async/await

---

## 🤝 Contributing

1. **Fork** this repository
2. **Create** your feature branch
   ```bash
git checkout -b feature/your-feature
```
   ```
3. **Commit** your changes
   ```bash
    git commit -m "feat: add your feature"
    ```
4. **Push** to your branch
    ```bash
    git push origin feature/your-feature
    ```
5. **Open** a **Pull** Request

After pushing your feature branch, open a Pull Request (PR) from your branch into the `main` branch of this repository.

Please make sure to:
- Write a clear title and description for your PR.
- Link any related issues if applicable.
- Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification for your commit messages (e.g., `feat: add new feature`, `fix: correct typo in README`).

Once your PR is reviewed and approved, it will be merged into the main project!

## 📝 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this project for personal or commercial purposes under the conditions of the [MIT license](LICENSE).

> See the [LICENSE](LICENSE) file for full license details.