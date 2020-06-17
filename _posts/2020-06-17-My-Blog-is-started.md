---
title:  "GitHubでのブログ構築。苦労したひとつのこと"
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

　GitHubPagesでブログを開設をすることができました。苦労したことをメモしておきます。

# 参考にしたサイト
　Windows環境に、RubyとGit bashをインストールしました。参考にしたのは以下の記事です。
* [GitHub PagesにJekyllでブログを作成する](https://note.com/airis0/n/n191e89b83e1d)<br/>

　上記記事を参考にデフォルトテーマで構築したあと、テーマ変更をしました。その際に参考になったのは、以下の記事です。
* [Jekyll themeをCentrariumに変更する](https://haltaro.github.io/2018/02/11/theme-change)

# テーマを変更したら、トップに記事が出ない
　ローカル環境では問題なかったのですが、GitHubにPushしたところ、トップページに記事が表示されない問題が発生しました。テーマで使用しているプラグインとGitHubとの相性が悪いようです。
*  [Centrariumのjekyll-archives問題を回避する](https://haltaro.github.io/2018/06/15/jekyll-archives)<br/>
　まずは、“_config.yml”から、上記の記事とまったく同じ箇所、jekyll-archives関連をコメントアウトしました。それでも記事は表示されなかったので、

<script src="https://gist.github.com/Hoiko-Takahashi/b57e0376f4b69b68901cc2dafa6961ae.js"></script>

　のように、-jekyll-paginate-v2を-jekyll-pagenateに。さらに、pagenate（表示する記事数）の指定を加えました。これで、うまくいきましたー。やっほー。
 
 # どうやって記事にソース書くの？
  　「[GitHub Gist](https://gist.github.com/)」を使うといい感じです！　詳細は「[HTMLやCSSのソースコードをそのままページに貼り付ける方法](https://fukafuka295.jp/source-code-haritsuke/)」参照。

