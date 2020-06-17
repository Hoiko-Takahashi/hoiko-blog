---
title:  "GitHubでブログをはじめるのに、苦労したこと"
date: 2020-06-17
layout: post
categories: Diary
cover:  "/assets/drop-of-water.jpg"
---
{% comment %}
cover:  "/assets/drop-of-water.jpg"
cover:  "/assets/sunflower.jpg"
cover:  "/assets/tulips.jpg"
cover:  "/assets/water.jpg"
cover:  "/assets/instacode.png"
{% endcomment %}

　GitHubでのブログ環境を構築することができました。苦労したところなどを書き留めておきましょう。

# 参考にしたサイト
　Jekyllで環境構築をして、GitHubにPushするまで、参考にした記事です。
・ [GitHub PagesにJekyllでブログを作成する](https://note.com/airis0/n/n191e89b83e1d)
　テーマ変更の際に、参考にしました。
・ [Jekyll themeをCentrariumに変更する](https://haltaro.github.io/2018/02/11/theme-change)

# テーマを変更したら、トップに記事が出ない
　テーマで使っているプラグインとGitHubとの相性が悪いようです。
・ [Centrariumのjekyll-archives問題を回避する](https://haltaro.github.io/2018/06/15/jekyll-archives)
　上記の方法で、_config.ymlから、jekyll-archives関連をコメントアウトした他、

#  - jekyll-paginate-v2
  - jekyll-paginate
paginate: 5

　と、-jekyll-paginate-v2を-jekyll-pagenateに。さらに、pagenate（表示する記事数）の指定を加えました。

