# Features

Nuxt Stack is composed of two parts:

- Nuxt [module](/module/) that installs and configures a collection of [modules and plugins](/module/plugins.html)
- Suite of [commands](/commands/) added to Nuxt's CLI for testing, linting, formatting etc.

## Nuxt Stack Module

- Prepends `normalize.css` to Nuxt's `css` array
- Installs `node-sass` and `sass-loader`
- Integrates `@nuxtjs/style-resources`
- Adds a `styles` alias for `css` in Nuxt's config
- Specify common meta data such as name, description and lang in one place and have it automatically cloned to head attributes, meta tags and the PWA manifest
- Easily add `preconnect` links for improved resource fetching performance
- Optimises Nuxt's `generate` config for Netlify with fallback enabled
- Configures Nuxt's server host and port to work across the network so you can view your app on another device during development
- ESLint integration with Webpack for linting and fixing your code automatically during development

The `nuxt-stack` module also installs and configures the following modules and plugins:

| Module                                     | Description                                                         |
| :----------------------------------------- | :------------------------------------------------------------------ |
| [`@nuxtjs/axios`][nuxt-axios]              | Nuxt `axios` module for making promise based HTTP requests          |
| [`@nuxtjs/dotenv`][nuxt-dotenv]            | Loads `.env` file and merges the key pairs with Nuxt's `env` object |
| [`@nuxtjs/pwa`][nuxt-pwa]                  | Collection of modules for developing PWAs                           |
| [`@nuxtjs/sitemap`][nuxt-sitemap]          | Automatically generate or serve a dynamic sitemap                   |
| [`nuxt-svg-loader`][nuxt-svg-loader]       | Import SVGs as Vue components                                       |
| [`webfontloader`][webfontloader]           | Load custom webfonts from services like Google and Typekit          |
| [`vue-analytics`][vue-analytics]           | Google Analytics integration for Vue and Nuxt                       |
| [`lazysizes`][lazysizes]                   | Lazily load images and videos only when they become visible         |
| [`vue-pwa-installer`][vue-pwa-installer]   | Interface for installing a PWA to the home screen                   |
| [`vue-lazy-hydration`][vue-lazy-hydration] | Lazily hydrate Vue components using a variety of strategies         |
| [`vue-tabbing`][vue-tabbing]               | Reactive flag triggered by keyboard navigation using the tab key    |
| [`vue-static-data`][vue-static-data]       | Declare static (non-reactive) data within Vue components            |

## Nuxt Stack Commands

- Generate project templates with `nuxt init`
  - Pick from two templates: "basic" or "fancy"
  - Only essential files and configuration are generated
  - Options for specifying the source, build and statically generated site folders
  - Score 100/100 in a Google Lighthouse audit from the outset
  - Inject useful development `scripts` and hooks for `husky` and `lint-staged`
  - Generate VSCode settings for resolving Nuxt path aliases and formatting code on save
- Write and run tests for Jest with zero configuration using `nuxt test`
  - Import Vue Single File Components (SFCs) into test files
  - Leverage `@vue/test-utils` suite of utilities for asserting your components
  - Use Jest's snapshot functions to render your Vue SFCs to formatted strings
  - Nuxt path aliases are automatically resolved
  - Only run _related_ tests when committing files to version control
- Lint your source files using `nuxt lint`
  - Configures ESLint file extensions to match `js,jsx,ts,tsx,vue`
- Format your code with Prettier using `nuxt format`
  - Optionally format and then lint with `nuxt format --lint`
- Delete all generated files and folders with `nuxt clean`
  - Removes `.nuxt`, `dist` and `coverage` folders
  - Optionally delete `node_modules` and lock files
- Serve statically generated sites with `nuxt serve`
  - Uses `serve` under the hood but infers the folder to serve from `nuxt.config.js`
- Generate a Webpack Bundle Analyser report with `nuxt stats`

[nuxt-axios]: https://axios.nuxtjs.org
[nuxt-dotenv]: https://www.npmjs.com/package/@nuxtjs/dotenv
[nuxt-pwa]: https://pwa.nuxtjs.org
[nuxt-sitemap]: https://www.npmjs.com/package/@nuxtjs/sitemap
[nuxt-svg-loader]: https://www.npmjs.com/package/nuxt-svg-loader
[webfontloader]: https://www.npmjs.com/package/webfontloader
[vue-analytics]: https://www.npmjs.com/package/vue-analytics
[lazysizes]: https://www.npmjs.com/package/lazysizes
[vue-pwa-installer]: https://www.npmjs.com/package/vue-pwa-installer
[vue-lazy-hydration]: https://www.npmjs.com/package/vue-lazy-hydration
[vue-tabbing]: https://www.npmjs.com/package/vue-tabbing
[vue-static-data]: https://www.npmjs.com/package/vue-static-data
