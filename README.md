# vuejs-install-instructions
Vuejsのインストール手順

## 環境

1. `node-js`のバージョン

    ```sh
    node -v
    ```
    - 結果
    ```sh
    v20.5.1
    ```

1. `npm`のバージョン

    ```sh
    npm -v
    ```
    - 結果
    ```sh
    9.8.0
    ```

1. `npx`のバージョン

    - `nodejs`と一緒にインストールされる模様

    ```sh
    npx -v
    ```
    - 結果
    ```sh
    9.8.0
    ```

## Vuejsのインストール（`@vue/cli`を使用）→ 依存モジュールが廃止になっていた等の理由で「非推奨」になっていた。実施を諦めた

### 参考資料

- 書籍「これからはじめるVue.js 3実践入門」の307ページ以降を参考にした

### 問題発生！！

- [公式サイト](https://cli.vuejs.org/guide/)より、

    ```
   ⚠️ Vue CLI はメンテナンス モードです。

    新しいプロジェクトの場合、Vitecreate-vueベースのプロジェクトをスキャフォールディングするために使用することが推奨されるようになりました。最新の推奨事項については、「Vue 3 ツール ガイド」も参照してください。 
    ```

- このため、`@vue/cli`のインストールは中止

<de>
1. `@vue/cli`をグローバルでインストール

    ```sh
    sudo npm i -g @vue/cli
    ```
    - 以下のエラーが発生した
    ```sh
    [sudo] kazuhiro のパスワード:
    npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
    npm WARN deprecated source-map-url@0.4.1: See https://github.com/lydell/source-map-url#deprecated
    npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
    npm WARN deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
    npm WARN deprecated @babel/plugin-proposal-optional-chaining@7.21.0: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-optional-chaining instead.
    npm WARN deprecated @babel/plugin-proposal-class-properties@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-class-properties instead.
    npm WARN deprecated @babel/plugin-proposal-nullish-coalescing-operator@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-nullish-coalescing-operator instead.
    npm WARN deprecated apollo-server-plugin-base@3.7.2: The `apollo-server-plugin-base` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-server-errors@3.3.1: The `apollo-server-errors` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-datasource@3.3.2: The `apollo-datasource` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-server-env@4.2.1: The `apollo-server-env` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/utils.fetcher` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-server-types@3.8.0: The `apollo-server-types` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-reporting-protobuf@3.4.0: The `apollo-reporting-protobuf` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/usage-reporting-protobuf` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-server-express@3.12.1: The `apollo-server-express` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated shortid@2.2.16: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
    npm WARN deprecated subscriptions-transport-ws@0.11.0: The `subscriptions-transport-ws` package is no longer maintained. We recommend you use `graphql-ws` instead. For help migrating Apollo software to `graphql-ws`, see https://www.apollographql.com/docs/apollo-server/data/subscriptions/#switching-from-subscriptions-transport-ws    For general help using `graphql-ws`, see https://github.com/enisdenjo/graphql-ws/blob/master/README.md
    npm WARN deprecated apollo-server-core@3.12.1: The `apollo-server-core` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.

    added 877 packages in 1m

    70 packages are looking for funding
    run `npm fund` for details
    ```

- ChatGPTの回答は以下

    ```
    このエラーメッセージは、npmパッケージの一部が非推奨とされていることを示しています。これは通常、古いバージョンのパッケージが使用されているか、新しいバージョンの代替パッケージが提供されているためです。

    エラーメッセージの中にいくつかのパッケージが非推奨とされている旨の警告が表示されています。具体的には、@babel/plugin-proposal-optional-chaining、@babel/plugin-proposal-class-properties、@babel/plugin-proposal-nullish-coalescing-operator などが含まれています。

    対策として、これらの非推奨のパッケージを新しいバージョンまたは代替パッケージに置き換えることが考えられます。以下は対策の手順です：
    ```

    1. 警告が表示されたパッケージを特定し、それらのパッケージをプロジェクトからアンインストールします。たとえば、@babel/plugin-proposal-optional-chaining のように一つずつ行います。

        ```sh
        npm uninstall @babel/plugin-proposal-optional-chaining
        npm uninstall @babel/plugin-proposal-class-properties
        npm uninstall @babel/plugin-proposal-nullish-coalescing-operator
        # 他の警告が表示されたパッケージも同様にアンインストール
        ```

    1. 代替パッケージまたは新しいバージョンのパッケージをインストールします。代替パッケージは、警告メッセージ中に提供されたリンク先のドキュメントで確認できます。たとえば、@babel/plugin-transform-optional-chaining は代替パッケージの一つです。これをインストールします。

        ```sh
        npm install @babel/plugin-transform-optional-chaining
        # 他の代替パッケージも同様にインストール
        ```

    ```
    必要な修正が完了したら、npm i -g @vue/cli コマンドを再実行してVue CLIをインストールします。
    これにより、非推奨のパッケージが新しいバージョンや代替パッケージに置き換えられ、エラーが解消されるはずです。
    ````

- ChtGPTの回答に従い対応してみる

- アンインストールコマンド

    ```sh
    npm uninstall @babel/plugin-proposal-optional-chaining \
        npm uninstall @babel/plugin-proposal-class-properties \
    npm uninstall @babel/plugin-proposal-nullish-coalescing-operator \
    npm uninstall apollo-server-plugin-base \
    npm uninstall apollo-server-errors \
    npm uninstall apollo-datasource \
    npm uninstall apollo-server-env \
    npm uninstall apollo-server-types \
    npm uninstall apollo-reporting-protobuf \
    npm uninstall apollo-server-express \
    npm uninstall shortid \
    npm uninstall subscriptions-transport-ws \
    npm uninstall apollo-server-core
    ```

    ```sh
    npm install @babel/plugin-transform-optional-chaining \
    npm install @babel/plugin-transform-class-properties \
    npm install @babel/plugin-transform-nullish-coalescing-operator \
    npm install @apollo/server \
    npm install @apollo/usage-reporting-protobuf \
    npm install graphql-ws
    ```
    - 結果
        ```sh

        added 1 package, and audited 471 packages in 5s

        45 packages are looking for funding
        run `npm fund` for details

        found 0 vulnerabilities
        ```

1. `@vue/cli`を再度、グローバルでインストール

    ```sh
    sudo npm i -g @vue/cli
    npm WARN deprecated @babel/plugin-proposal-class-properties@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-class-properties instead.
    npm WARN deprecated @babel/plugin-proposal-nullish-coalescing-operator@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-nullish-coalescing-operator instead.
    npm WARN deprecated source-map-url@0.4.1: See https://github.com/lydell/source-map-url#deprecated
    npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
    npm WARN deprecated @babel/plugin-proposal-optional-chaining@7.21.0: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-optional-chaining instead.
    npm WARN deprecated apollo-datasource@3.3.2: The `apollo-datasource` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
    npm WARN deprecated apollo-server-plugin-base@3.7.2: The `apollo-server-plugin-base` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
    npm WARN deprecated apollo-server-types@3.8.0: The `apollo-server-types` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-server-errors@3.3.1: The `apollo-server-errors` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-server-express@3.12.1: The `apollo-server-express` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated shortid@2.2.16: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
    npm WARN deprecated apollo-server-env@4.2.1: The `apollo-server-env` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/utils.fetcher` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated apollo-reporting-protobuf@3.4.0: The `apollo-reporting-protobuf` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/usage-reporting-protobuf` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    npm WARN deprecated subscriptions-transport-ws@0.11.0: The `subscriptions-transport-ws` package is no longer maintained. We recommend you use `graphql-ws` instead. For help migrating Apollo software to `graphql-ws`, see https://www.apollographql.com/docs/apollo-server/data/subscriptions/#switching-from-subscriptions-transport-ws    For general help using `graphql-ws`, see https://github.com/enisdenjo/graphql-ws/blob/master/README.md
    npm WARN deprecated apollo-server-core@3.12.1: The `apollo-server-core` package is part of Apollo Server v2 and v3, which are now deprecated (end-of-life October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
    ```

- 以下への対尾

    ```
    npm WARN deprecated @babel/plugin-proposal-class-properties@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-class-properties instead.
    ```

    ```
    npm WARN deprecated @babel/plugin-proposal-nullish-coalescing-operator@7.18.6: This proposal has been merged to the ECMAScript standard and thus this plugin is no longer maintained. Please use @babel/plugin-transform-nullish-coalescing-operator instead.
    ```

    ```sh
    npm uninstall @babel/plugin-proposal-class-properties \
    @babel/plugin-proposal-nullish-coalescing-operator
    ```
 
    ```sh
    npm install @babel/plugin-transform-class-properties
    @babel/plugin-transform-nullish-coalescing-operator
    ```
    - 結果
    ```sh


removed 271 packages, and audited 200 packages in 2s

17 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
        ```

</del>

- `@vue/cli`のインストールの後始末

    ```sh
    npm uninstall @babel/plugin-transform-optional-chaining \
    npm uninstall @babel/plugin-transform-class-properties \
    npm uninstall @babel/plugin-transform-nullish-coalescing-operator \
    npm uninstall @apollo/server \
    npm uninstall @apollo/usage-reporting-protobuf \
    npm uninstall graphql-ws
    ```

    - 結果
    ```
    
    removed 199 packages, and audited 2 packages in 1s

    found 0 vulnerabilities
    ```

    ```sh
    npm uninstall @babel/plugin-transform-class-properties
    ```

    ```sh

    up to date, audited 2 packages in 673ms

    found 0 vulnerabilities
    ```

    ```sh
    sudo npm un `@vue/cli -g
    [sudo] kazuhiro のパスワード:

    removed 877 packages in 3s
    ```

    ```sh
    npm ls -g
    /usr/local/lib
    └── @nestjs/cli@10.1.18
    ```

## Vuejsのインストール（`vite`を使用。パッケージマネージャは`npm`のみ使用。`yarn`は使用しない）

### 参考資料

- 書籍「これからはじめるVue.js 3実践入門」の307ページ以降を参考にした


### 構築手順

1. プロジェクトのフォルダを作成するフォルダに移動

    ```sh
    cd ~
    ```

1. Vue.jsのプロジェクトを作成(`vite`はインストールは必要なし、`npm`に同梱されている模様)

    ```sh
    npm init vite@latest
    ```

    ```sh
    Need to install the following packages:
    create-vite@4.4.1
    Ok to proceed? (y) y
    ✔ Project name: … vuejs-sample-01
    ✔ Select a framework: › Vue
    ✔ Select a variant: › TypeScript

    Scaffolding project in /home/kazuhiro/vuejs-sample-01/vuejs-sample-01...

    Done. Now run:

    cd vuejs-sample-01
    npm install
    npm run dev
    ```

1. プロジェクトのフォルダに移動

    ```sh
    cd vuejs-sample-01
    ```

1. 依存おジュールをインストール 

    ```sh
    npm install
    ```
    - 結果
    ```sh
    added 42 packages, and audited 43 packages in 17s

    4 packages are looking for funding
    run `npm fund` for details

    found 0 vulnerabilities
    ```

1. 作成されたフォルダを確認

    ```sh
    合計 72
    drwxrwxr-x   6 kazuhiro kazuhiro  4096 10月 21 21:49 .
    drwx------. 31 kazuhiro kazuhiro  4096 10月 21 21:45 ..
    -rw-rw-r--   1 kazuhiro kazuhiro   253 10月 21 21:45 .gitignore
    drwxrwxr-x   2 kazuhiro kazuhiro    29 10月 21 21:45 .vscode
    -rw-rw-r--   1 kazuhiro kazuhiro  1527 10月 21 21:45 README.md
    -rw-rw-r--   1 kazuhiro kazuhiro   362 10月 21 21:45 index.html
    drwxrwxr-x  32 kazuhiro kazuhiro  4096 10月 21 21:49 node_modules
    -rw-rw-r--   1 kazuhiro kazuhiro 30027 10月 21 21:49 package-lock.json
    -rw-rw-r--   1 kazuhiro kazuhiro   383 10月 21 21:45 package.json
    drwxrwxr-x   2 kazuhiro kazuhiro    22 10月 21 21:45 public
    drwxrwxr-x   4 kazuhiro kazuhiro   106 10月 21 21:45 src
    -rw-rw-r--   1 kazuhiro kazuhiro   661 10月 21 21:45 tsconfig.json
    -rw-rw-r--   1 kazuhiro kazuhiro   213 10月 21 21:45 tsconfig.node.json
    -rw-rw-r--   1 kazuhiro kazuhiro   157 10月 21 21:45 vite.config.ts
    ```

1. `package.json`の内容を確認

    ```sh
    cat package.json
    {
    "name": "vuejs-sample-01",
    "private": true,
    "version": "0.0.0",
    "type": "module",
    "scripts": {
        "dev": "vite",
        "build": "vue-tsc && vite build",
        "preview": "vite preview"
    },
    "dependencies": {
        "vue": "^3.3.4"
    },
    "devDependencies": {
        "@vitejs/plugin-vue": "^4.2.3",
        "typescript": "^5.0.2",
        "vite": "^4.4.5",
        "vue-tsc": "^1.8.5"
    }
    }
    ```

1.  `vite.config.ts`の内容を確認

    - [このサイト](https://kokichiblog.com/it/1103/)によると、Viteで構築したVue.jsは「listenポートが`5173`となっています。」とのこと
    - また、ポート番号は、`vite.config.ts`の変更で対応できるとのこと（あとで試す）

    ```sh
    cat vite.config.ts 
    import { defineConfig } from 'vite'
    import vue from '@vitejs/plugin-vue'

    // https://vitejs.dev/config/
    export default defineConfig({
    plugins: [vue()],
    })
    ```

1. アプリをビルドする

    ```sh
    cd ~/vuejs-sample-01
    ```

    ```sh
    npm run build
    ```

    - 結果
    ```sh

    > vuejs-sample-01@0.0.0 build
    > vue-tsc && vite build

    vite v4.5.0 building for production...
    ✓ 18 modules transformed.
    dist/index.html                  0.45 kB │ gzip:  0.29 kB
    dist/assets/vue-5532db34.svg     0.50 kB │ gzip:  0.31 kB
    dist/assets/index-c322ae43.css   1.30 kB │ gzip:  0.67 kB
    dist/assets/index-efed76db.js   51.75 kB │ gzip: 20.99 kB
    ✓ built in 1.41s
    ```

1. プロジェクトのフォルダの内容を確認する

    - `dist`フォルダが追加になっている

    ```sh
    ll -a
    合計 72
    drwxrwxr-x   7 kazuhiro kazuhiro  4096 10月 21 22:58 .
    drwx------. 31 kazuhiro kazuhiro  4096 10月 21 21:45 ..
    -rw-rw-r--   1 kazuhiro kazuhiro   253 10月 21 21:45 .gitignore
    drwxrwxr-x   2 kazuhiro kazuhiro    29 10月 21 21:45 .vscode
    -rw-rw-r--   1 kazuhiro kazuhiro  1527 10月 21 21:45 README.md
    drwxrwxr-x   3 kazuhiro kazuhiro    54 10月 21 22:58 dist
    -rw-rw-r--   1 kazuhiro kazuhiro   362 10月 21 21:45 index.html
    drwxrwxr-x  32 kazuhiro kazuhiro  4096 10月 21 21:49 node_modules
    -rw-rw-r--   1 kazuhiro kazuhiro 30027 10月 21 21:49 package-lock.json
    -rw-rw-r--   1 kazuhiro kazuhiro   383 10月 21 21:45 package.json
    drwxrwxr-x   2 kazuhiro kazuhiro    22 10月 21 21:45 public
    drwxrwxr-x   4 kazuhiro kazuhiro   106 10月 21 21:45 src
    -rw-rw-r--   1 kazuhiro kazuhiro   661 10月 21 21:45 tsconfig.json
    -rw-rw-r--   1 kazuhiro kazuhiro   213 10月 21 21:45 tsconfig.node.json
    -rw-rw-r--   1 kazuhiro kazuhiro   157 10月 21 21:45 vite.config.ts
    ```

- `dist`フォルダの内容を確認

    ```sh
    合計 12
    drwxrwxr-x 3 kazuhiro kazuhiro   54 10月 21 22:58 .
    drwxrwxr-x 7 kazuhiro kazuhiro 4096 10月 21 22:58 ..
    drwxrwxr-x 2 kazuhiro kazuhiro   81 10月 21 22:58 assets
    -rw-rw-r-- 1 kazuhiro kazuhiro  454 10月 21 22:58 index.html
    -rw-rw-r-- 1 kazuhiro kazuhiro 1497 10月 21 22:58 vite.svg
    ```

- アプリを起動する

    ```sh
    npm run  dev 
    ```
    - 結果

    ```sh
      VITE v4.5.0  ready in 472 ms

    ➜  Local:   http://localhost:5173/
    ➜  Network: use --host to expose
    ➜  press h to show help
    ```

- 別ターミナルで`cural`でアクセス → 疎通確認成功！！


    ```sh
    curl http://localhost:5173
    ```

    - 結果
    ```sh
    <!doctype html>
    <html lang="en">
    <head>
        <script type="module" src="/@vite/client"></script>

        <meta charset="UTF-8" />
        <link rel="icon" type="image/svg+xml" href="/vite.svg" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Vite + Vue + TS</title>
    </head>
    <body>
        <div id="app"></div>
        <script type="module" src="/src/main.ts"></script>
    </body>
    </html>
    ```

- ただし、IPアドレスを指定して`curl`を実行するとエラーとなる。
- このことから、viteのWebサーバは公開用に使うことを考えていないことが理解できる。

