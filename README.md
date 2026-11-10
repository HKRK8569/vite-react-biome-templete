# vite-react-biome-templete

## セットアップ

Node.js 22.23.4 と pnpm 12.18.0 を使用します。Volta では Node.js のバージョンを固定しています。

pnpm が未導入の場合は、次のコマンドでインストールします。

```sh
npm install --global pnpm@12.18.0
```

```sh
pnpm install --frozen-lockfile
```

Volta 経由で `node: not found` が出る場合は、`volta run --node 22.23.4 pnpm install --frozen-lockfile`
のように実行してください。起動や確認コマンドも同じ形式で実行できます。

依存パッケージは、各バージョンの公開から3日（4,320分）経過したものだけを許可します。
公開日時を取得できない場合もインストールを拒否します。設定は `pnpm-workspace.yaml` にあります。

## 起動方法

```
pnpm dev
```

## 確認コマンド

```sh
pnpm exec tsc -b
pnpm test
pnpm build
pnpm build-storybook
```

## スタイル

Tailwind CSS を使用しています。`src/index.css` で読み込み、コンポーネントの
`className` にユーティリティクラスを指定します。Storybook でも同じ CSS を読み込みます。
