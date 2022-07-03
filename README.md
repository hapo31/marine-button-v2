# marine-button-v2

marine-button-v2 は以下のようなモジュールで monorepo で構成されている。

## marine-server

API サーバー。  
NestJS
コンテンツの管理とフロントエンドビルド時にボタン一覧情報を WebAPI として提供。  
CMS としての機能もある（予定）。

## pirate-frontend

フロントエンド。  
Next.js, React, Recoil
SSG でビルド時に API サーバーからボタン一覧情報を取得して生成する。

## treasure-schema

スキーマの管理。
Prisma.js
prisma.schema から prisma generate を用いて marine-server, pirate-frontend に DB の型情報とクライアントコードを提供する。
