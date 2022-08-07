# 課題内容

Figma のデザインを参考に、Todo の作成を行う。

ディレクトリ構造は本番を想定して作る。

eslint、prettier に関しては導入必須で、設定方法は自由。

テストは余裕があれば書く。

その他のツールに関しては任意。なお、MUI や ChakraUI などの UI ライブラリの使用は禁止。

# 仕様

デザインは[こちら](https://www.figma.com/file/9mSTr7E2cg5xs7Qr0WzpML/Web%E3%83%95%E3%83%AD%E3%83%B3%E3%83%88-%E8%AA%B2%E9%A1%8C?node-id=0%3A1)

- 機能要件

  - デザインに合わせて Todo アプリの UI を構築する
  - Todo の取得 / 追加 / 削除を json-server と連携して実装する

- プロジェクトの立ち上げ方
  - `yarn install` で依存関係をインストール
  - `yarn dev` で開発サーバーを立ち上げる
  - `yarn json-server` でモックサーバーを立ち上げる

# TodoAPI に関しては以下

Todo エンドポイント -> http://localhost:5000/todos

型に関して

```
Todo = {
  id: number,
  title: string;
}
```

※id に関しては自動インクリメント

| メソッド | リクエストボディ        | URL         | レスポンス               |
| -------- | ----------------------- | ----------- | ------------------------ |
| Get      | なし                    | /todos      | Todo[]                   |
| Post     | body: { title: string } | /todos      | Todo                     |
| Delete   | なし                    | /todos/[id] | {} （※空のオブジェクト） |

# 技術に関して

React / Next.js を使用して作成してください。

CSS や API のライブラリに関しては自由にインストールしていただいて大丈夫です。

# 期限

１週間以内にご自身の GitHub にあげたものを提出してください。

# その他

もし仕様などに関する質問があれば、いつでも質問してください。
