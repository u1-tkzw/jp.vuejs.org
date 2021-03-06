---
title: インストール
type: guide
order: 0
vue_version: 1.0.13
dev_size: "244.48"
min_size: "69.37"
gz_size: "23.85"
---

> **互換性に関する注意:** Vue.js は IE8 以下をサポートしていません。

## スタンドアロン

ダウンロードし script タグで読み込んでください。`Vue` はグローバル変数として登録されます。

<div id="downloads">
<a class="button" href="/js/vue.js" download>開発バージョン</a><span class="light info">警告出力とデバッグモードあり</span>

<a class="button" href="/js/vue.min.js" download>プロダクションバージョン</a><span class="light info">警告出力なし、{{gz_size}}kb min+gzip</span>
</div>

### CDN

 [jsdelivr](//cdn.jsdelivr.net/vue/{{vue_version}}/vue.min.js) または [cdnjs](//cdnjs.cloudflare.com/ajax/libs/vue/{{vue_version}}/vue.min.js) を利用可能です。 (同期に少し時間がかかるので、最新版ではないかもしれません)。

### CSP 準拠ビルド

Google Chrome アプリのようなある環境では、Content Security Policy (CSP) を強制し、そして式の評価するために `new Function()` の使用を許可しません。これらのケースの場合、[CSP 準拠ビルド](https://github.com/vuejs/vue/tree/csp/dist) を代わりに使用できます。

## NPM

NPM は Vue.js で大規模アプリケーションを構築するときのインストール方法を推奨します。[Webpack](http://webpack.github.io/) または [Browserify](http://browserify.org/) のような CommonJS モジュールバンドラでうまくペアにします。Vue.js は[単一ファイルコンポーネント](application.html#Single_File_Components)による著作のための、付随するツールも提供しています。

``` bash
# 最新の安定版
$ npm install vue
# 最新の安定版 + CSP 準拠
$ npm install vue@csp
```

## CLI

Vue.js は意欲的なシングルページアプリケーションをすぐに足場固めするの対して、[オフィシャル CLI](https://github.com/vuejs/vue-cli) を提供します。それはモダンなフロントエンドのフレームワークのワークフローに対して、内蔵されたバッテリーの構築を提供します。ホットリローディング、リントの保存、そして本番可能なビルドを実行して準備するのは、わずか数分です。

``` bash
# インストール vue-cli
$ npm install -g vue-cli
# "webpack" ボイラープレートを使用した新しいプロジェクトを作成する
$ vue init webpack my-project
# 依存関係をインストールしてgo!
$ cd my-project
$ npm install
$ npm run dev
```

## 開発版のビルド

**重要**: NPM に配信された CommonJS バンドル (`vue.commonjs.js`) は配信元のコードで制御されていません。したがって、Github 上の最新のソースコードから Vue を使用するには、あなた自身それをビルドしなければなりません！

``` bash
git clone https://github.com/vuejs/vue.git node_modules/vue
cd node_modules/vue
npm install
npm run build
```

## Bower

``` bash
# 最新の安定版
$ bower install vue
```

## AMD モジュールローダ
ダウンロードされたスタンドアロン版 Vue.js と Bower 経由でインストールされた Vue.js は UMD でラップされています。そのため、 AMD モジュールとして直接利用することができます。

