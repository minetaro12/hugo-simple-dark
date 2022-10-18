<h1 align=center>Hugo SimpleDark</h1>

![screenshot](https://user-images.githubusercontent.com/77948036/182126160-5fbc1e4d-fb02-4ad8-aaab-bc0e75b6df80.png)

[Demo](https://minetaro12.github.io/hugo-simple-dark)

デモサイトのソースは[examplesite](https://github.com/minetaro12/hugo-simple-dark/tree/examplesite)ブランチにあります

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

### config.ymlの書き方

```yml
baseURL: https://example.org/
languageCode: ja-jp
title: My New Site
theme: hugo-simple-dark
copyright: "&copy; 2022 yourname" #フッター部分の文字列

menu:
  header:
    - name: Posts #メニューの名前
      weight: 1 #表示される順番
      url: /posts #推移先のURL

    - name: Tags
      weight: 2
      url: /tags

    - name: MyGithub
      weight: 3
      url: https://github.com/
      params:
        newtab: true #新しいタブで開くようにする

params:
  showsource: true #記事にソースへのリンクを表示するかどうか
  contenturl: https://github.com/yourname/site-repo/tree/master/content/ #ソースのcontentディレクトリのURL
  description: Hello #OGPの説明部分
  image: #OGP画像のパス(サイトのassetsディレクトリ内に画像を入れて、assetsディレクトリ基準のパスを書き込む)

markup:
  highlight:
    style: monokai #see https://xyproto.github.io/splash/docs/all.html
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