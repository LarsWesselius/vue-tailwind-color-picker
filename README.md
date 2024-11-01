# Made to work with latest Tailwind and Vue3.
## As of 28th of October, 2024




# Vue Tailwind Color Picker

Color picker for vue using Tailwind v2.

**Requires Tailwind**

## [Live demo](https://advplyr.github.io/vue-tailwind-color-picker/)

<img src="https://raw.githubusercontent.com/advplyr/vue-tailwind-color-picker/master/sample.png" />

## Installation

```bash
$ npm install vue-tailwind-color-picker
```

```bash
$ yarn add vue-tailwind-color-picker
```

## Installation Nuxt
Global add plugins 

plugins/vue-tailwind-color-picker.js

```
import Vue from 'vue'
import VueTailwindColorPicker from 'vue-tailwind-color-picker'
Vue.use(VueTailwindColorPicker)
```

add nuxt.config.js

```
plugins: [
    '~/plugins/vue-tailwind-color-picker',
  ],
```

## Installation Nuxt Typescript

Global add plugins 

plugins/vue-tailwind-color-picker.ts

```
import Vue from 'vue'
// @ts-ignore
import VueTailwindColorPicker from 'vue-tailwind-color-picker'
Vue.use(VueTailwindColorPicker)
```

add nuxt.config.ts

```
plugins: [
    '~/plugins/vue-tailwind-color-picker',
  ],
```

## Usage

```js
<template>
   <vue-tailwind-color-picker v-model="color" :swatches.sync="swatches" :hide-swatches="false" @change="changedColor" @addSwatch="swatchAdded" @deleteSwatch="swatchDeleted" />
</template>

<script>
import VueTailwindColorPicker from 'vue-tailwind-color-picker.vue'

export default {
  components: {
    VueTailwindColorPicker
  },
  data() {
    return {
      color: '#00FF00FF',
      swatches: [
        '#f94144',
        '#f3722c',
        '#f8961e',
        '#f9c74f',
        '#90be6d',
        '#43aa8b',
        '#577590',
        '#22223b',
        '#4a4e69',
        '#c9ada7'
      ]
    }
  },
  methods: {
    changedColor(color) {
      console.warn('Changed Color', color)
    },
    swatchAdded(color) {
      console.log('Swatch Added', color)
    },
    swatchDeleted(color) {
      console.log('Swatch Deleted', color)
    }
  }
}
</script>
```

## License
[MIT](https://choosealicense.com/licenses/mit/)
