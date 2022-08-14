<h1 align=center>Hugo SimpleDark</h1>

![screenshot](https://user-images.githubusercontent.com/77948036/182126160-5fbc1e4d-fb02-4ad8-aaab-bc0e75b6df80.png)

[Demo](https://minetaro12.github.io/hugo-simple-dark)

## 使い方

```
# サイトの作成
$ hugo new site -f yml new-site

$ cd new-site

# テーマの追加
$ git clone https://github.com/minetaro12/hugo-simple-dark themes/hugo-simple-dark

# テーマの追加(Submodule)
$ git submodule add -b master https://github.com/minetaro12/hugo-simple-dark themes/hugo-simple-dark

# サンプル設定ファイルのコピー
$ cp themes/hugo-simple-dark/example.config.yml config.yml

# テンプレートファイルのコピー
$ cp themes/hugo-simple-dark/archetypes/default.md archetypes/default.md

# 記事の作成
$ hugo new posts/hello.md
```

### アーカイブを表示したい場合

`content`ディレクトリ内に`archives.md`を作成し、下の内容を書き込む。

```
---
title: Archives
layout: archive
---
```

`example.com/archives`にアーカイブが表示されます。