# vue-select ![Current Release](https://img.shields.io/github/release/sagalbot/vue-select.svg?style=flat-square) ![Bundle Size](https://flat.badgen.net/bundlephobia/min/vue-select)  ![Monthly Downloads](https://img.shields.io/npm/dm/vue-select.svg?style=flat-square) ![Code Coverage](https://img.shields.io/coveralls/github/sagalbot/vue-select.svg?style=flat-square) ![Maintainability Score](https://img.shields.io/codeclimate/maintainability/sagalbot/vue-select.svg?style=flat-square) ![MIT License](https://img.shields.io/github/license/sagalbot/vue-select.svg?style=flat-square)

> **This is a fork of [vue-select](https://github.com/sagalbot/vue-select) with support for searching multiple keys in an object, customizable text when no results are found and a minimum input length before the list shows.**

> **Everything you wish the HTML `<select>` element could do, wrapped up into a lightweight, zero
dependency, extensible Vue component.**

- Tagging
- Filtering / Searching
- Vuex Support
- AJAX Support
- SSR Support
- ~20kb Total / ~5kb CSS / ~15kb JS
- Select Single/Multiple Options
- Customizable with slots and SCSS variables
- Tested with Bootstrap 3/4, Bulma, Foundation
- +95% Test Coverage
- Zero dependencies

## Documentation

Complete documentation and examples available at https://vue-select.org.

- **[API Documentation](https://vue-select.org)**
- **[Sandbox Demo](https://vue-select.org/sandbox.html)**
- **[CodePen Template](http://codepen.io/sagalbot/pen/NpwrQO)**
- **[GitHub Projects](https://github.com/sagalbot/vue-select/projects)**

## Install (Standard Repo, without this fork's functionality)

```bash
$ npm install vue-select
```

Register the component

```js
import Vue from 'vue'
import vSelect from 'vue-select'

Vue.component('v-select', vSelect)
```

You may now use the component in your markup

```html
<v-select v-model="selected" :options="['Vue.js','React']"></v-select>
```

You can also include vue-select directly in the browser. Check out the
[documentation for loading from CDN.](https://vue-select.org/guide/install.html#in-the-browser).

## Fork functions

The functions that are available in this fork are explained here.

Change the text when no options are available

```html
<v-select v-model="selected" :options="['Vue.js','React']" :noOptionsText="'Sorry, geen opties gevonden'"></v-select>
```

Use multiple keys to search from, with "a darn good search filter function" [credits to Peterbe.com](https://www.peterbe.com/plog/a-darn-good-search-filter-function-in-javascript).

```html
<v-select v-model="selected" :options="[{name: 'John Doe', address: '123 Main St', city: 'Anytown'}, {name: 'Jane Doe', address: '123 Appleseed', city: 'Cupertino'}, {name: 'Jan Janssen', address: 'Hoofdweg 1', city: 'Amsterdam'}]" :noOptionsText="'Sorry, geen opties gevonden'" label="name" :searchBy="['name', 'address', 'city']"></v-select>
```

Set minimum input length

```html
<v-select v-model="selected" :options="[{name: 'John Doe', address: '123 Main St', city: 'Anytown'}, {name: 'Jane Doe', address: '123 Appleseed', city: 'Cupertino'}, {name: 'Jan Janssen', address: 'Hoofdweg 1', city: 'Amsterdam'}]" :noOptionsText="'Sorry, geen opties gevonden'" label="name" :searchBy="['name', 'address', 'city']" :minInputLength="1"></v-select>
```

> __This fork is used internally and only with the searchBy key. If there are any issues, feel free to create an issue and/or fix the issue. But please, keep me informed!__

## License

[MIT](https://github.com/sagalbot/vue-select/blob/master/LICENSE.md)
