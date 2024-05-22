# microcms-field-extension-app-nextjs
https://blog.microcms.io/microcms-field-extension-sdk/

MicroCMSの拡張フィールド（iframe仕様）用のコンポーネント

## Getting Started

# アプリの作成
```sh
npx create-next-app microcms-iframe-app-color --example https://github.com/microcmsio/microcms-field-extension-sdk/tree/main/examples/nextjs
cd microcms-iframe-app-color
```

## microCMS側のアプリを指定（サービスIDを指定）
```
export NEXT_PUBLIC_MICROCMS_ORIGIN='https://〇〇〇.microcms.io'
```
## 実行
```
npm run dev
```

## Vercelなどにデプロイし、そのURLをMicroSMS側で指定する。
Environment Variables に「NEXT_PUBLIC_MICROCMS_ORIGIN」を設定してデプロイする。

MicroCMS側で拡張フィールドを作成し、VercelのURLを指定する。
- APIを作る
- APIスキーマからフィールドを追加する。その時に拡張フィールドを選択し、コンポーネントのURLを設定する。
- あとはデータを入稿すると追加したフィールドの情報がJSONデータに追加される。
※お知らせのサンプルAPIを作って、そこにcolorのフィールドを足した例
```
        {
            "id": "zpldgdqj1vs7",
            "createdAt": "2024-05-22T14:25:09.482Z",
            "updatedAt": "2024-05-22T14:25:09.482Z",
            "publishedAt": "2024-05-22T14:25:09.482Z",
            "revisedAt": "2024-05-22T14:25:09.482Z",
            "title": "さんぷる２",
            "content": "<p>ないよう２</p><p>かいぎょうしたら</p><p>こうなるよ。</p><p>あおいろです。</p>",
            "category": {
                "id": "bmvt1on06-yo",
                "createdAt": "2024-05-22T13:51:39.301Z",
                "updatedAt": "2024-05-22T13:51:39.301Z",
                "publishedAt": "2024-05-22T13:51:39.301Z",
                "revisedAt": "2024-05-22T13:51:39.301Z",
                "name": "テクノロジー"
            },
            "color": "#2f0cdf"
        },
```
