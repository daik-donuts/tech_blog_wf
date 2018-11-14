---
title: hexoの使い方 
date: 2018-11-13 19:52:14
tags: hexo
---

hexoのテストも兼ねて、簡単な使い方を認めておく。

## hexoとは
静的サイトジェネレータの一つ。Markdownで書き・ビルドするまでサポートする。

hexoが吐き出すのはHTML/CSSなど静的ファイルだけなので、環境に依存せず管理が楽チン。

専用のデプロイツールを使えば、簡単にブログが運営できる。

似た思想のものにhugoがあるがこちらはGolang用。


## 基本の使い方
参考url: https://tech.qookie.jp/posts/info-hexo-local/

### 記事を追加/削除する
記事を追加するときは、

`hexo new post your-post-name` 

`source/_posts/`以下にMDファイルが生成されるので、これを編集する。

削除したい時はMDファイルを削除するだけで良い。

### 下書きを追加する
同じく、

`hexo new draft your-draft-name`

で`source/_draft/`以下に生成されるMDファイルを編集する。

### プレビューする
記事を見るにはサーバを起動する必要がある。

`hexo s` または`hexo server`で起動できる。

### ビルドする
プレビュー画面は、hexoサーバがレンダリングしたものなので、他の環境では動かない。

Hexoのテーマ・npmライブラリ・Markdownからブログに必要なHTML/CSS/JSなど一式を生成するビルドコマンドこちら：

`hexo generate`

普通の静的サイトなので、どこのサーバーにアップしても表示できる。

Netlifyなどの一部のホスティングサービスはビルドプロセスの設定もできるので、githubのレポジトリにpushするだけでデプロイが完了するようにできる。

