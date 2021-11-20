# Nuxt.js

## overview

- Nuxt.js = Vue.js(v2) + vue-router + Vuex + SSR(node)
- you need to append module and plugin to `nuxt.config.js` every installation

## tags

- NuxtLink: like <a />
    - to: href attribute
- main: like <div />. use as child element of <template />
- Nuxt: render components in pages/ by layouts/default.vue

## directory

- pages/: route automatically
- components/: be run files automatically
- assets/: css, img, font which has been compiled
- static/: like public/. this files are never compiled and located as raw
- layouts/: default.vue = App.vue + <header /> + <nav /> + <footer>
- store/: activate Vuex in index.js
- nuxt.config.js: config file in nuxt app. you can config plugin, <head />


## property


## glossary

- context: access object to Nuxt contents developed for API
- helper: access to variable in server side via $nuxt
- SSR: server side rendering by using node in Nuxt SSR mode
- SPA: this doesn't require node. browser render <NuxtLink /> only once, after static hosting server render files
- lifecycle: load plugin -> serverInit(Vuex, context) -> middleware -> created() -> fetch() -> mounted()

## .env

1. install @nuxtjs/dotenv package
2. add @nuxtjs/dotenv to buildModules in nuxt.config.js
3. you can refer to process.env.VAR