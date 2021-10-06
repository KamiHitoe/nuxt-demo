
## overview

- Nuxt.js = Vue.js(v2) + vue-router + Vuex + SSR(node)
- moduleやpluginをinstallする度にnuxt.config.jsに追記する必要がある

## tags

- NuxtLink: like <a>
    - to: href attribute
- main: like <div>. <template>の子要素に用いる
- Nuxt: layouts/default.vueでpages/コンポーネントをレンダリング

## directory

- pages/: 自動でroutingしてくれる
- components/: 自動で<script>components</script>してくれる
- assets/: css, img, fontなどコンパイルされていないもの
- static/: vueで言うpublic/. コンパイルされず直接サーバのルートに配置される
- layouts/: vueで言うApp.vueに<header>, <nav>, <footer>を追加したのがdefault.vue
- store/: index.jsを作成することでVuexが有効化される
- nuxt.config.js: nuxtの設定ファイル. pluginとか<head>の設定とかできる


## property


## glossary

- context: API用に開発されたNuxtコンテンツへのアクセスオブジェクト
- helper: $nuxtを使ってサーバサイドの変数にアクセスする
- SSR: Nuxt SSRモードではサーバサイドレンダリングするのでnodeは必須
- SPA: nodeいらない. 静的ホスティングサービスから一度レンダリングするとあとは<NuxtLink>でブラウザ側で遷移するだけ
- ライフサイクル: plugin読み込み -> serverInit(Vuex, context) -> middleware -> created() -> fetch() -> mounted()

## .env

1. @nuxtjs/dotenvパッケージをinstall
2. nuxt.config.jsのbuildModulesに@nuxtjs/dotenvを追加
3. process.env.VARで参照可能


