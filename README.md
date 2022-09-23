# pon-developer-guide-vuejs

## Introduction
Ahoy there fellow Developer 👋 This repository is a good starting point for accelerating your ability to contribute towards our VueJS projects, yay! Scouts rules apply, so please keep this page up to date for your colleagues (or future self).

### Composition API vs. Options API
All components should be created using the composition API pattern and should be created using the `<script setup>` method.

Have a read about it on the [VueJS introduction page](https://vuejs.org/guide/introduction.html#api-styles) that will give you a good idea on te differences

### General guidelines
We develop our components using v3.

We're not pretending to know more than the creators of VueJS and luckily for us they have [extended documentation](https://vuejs.org/guide/introduction.html) on how to use the library and provide the best practices.
We try to keep our standards on VueJS aligned.

All components should follow the Style guide provided by VueJS. Note: the guide is written for v2.x, but still applies for everything except the examples that utilize the Options API.

Useful links:
* [Docs](https://vuejs.org/guide/introduction.html)
* [Style guide](https://v2.vuejs.org/v2/style-guide/) ()

### Recommended plugins
| Type               | Name                     | Link                                              |
|--------------------|--------------------------|---------------------------------------------------|
| State management   | Pinia                    | [link](https://pinia.vuejs.org/)                  |
| Component library  | Ponbike Vue components   | [link](https://github.com/ponbike/vue-components) |

### Linting

#### Eslint
Eslint should extend from `plugin:vue/vue3-recommended`

Links:
* [Eslint](https://eslint.org/)
* [eslint-plugin-vue](https://github.com/vuejs/eslint-plugin-vue)
* [Eslint rules for VueJS](https://eslint.vuejs.org/rules/)

#### Stylelint
Stylelint should extend from `stylelint-config-standard-scss`

Links:
* [Stylelint](https://stylelint.io/)
* [stylelint-config-standard-scss](https://www.npmjs.com/package/stylelint-config-standard-scss)

#### Install dependencies
`npm install eslint-plugin-vue vite-plugin-stylelint vite-plugin-eslint stylelint-config-standard-scss -D`

#### Edit configuration file
To set up automatic linting on hot reloading edit the `vite.config.js` file to use the plugins for `Eslint` and `Stylelint`

`vite-config.js`
```js
import { defineConfig } from 'vite'
import StylelintPlugin from 'vite-plugin-stylelint'
import EslintPlugin from 'vite-plugin-eslint'
import Vue from '@vitejs/plugin-vue'

export default defineConfig(({ mode }) => {
  return {
    plugins: [
      Vue(),
      StylelintPlugin(),
      EslintPlugin()
    ]
  }
}
```
