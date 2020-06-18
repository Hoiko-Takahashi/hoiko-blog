---
title:  "【Centrarium】トップページに記事全文が表示される問題"
date: 2020-06-18
layout: post
categories: Diary
cover:  "/assets/tomatoes-5356_1920.jpg"
---
{% comment %}
cover:  "/assets/tomatoes-1561565_1920.jpg"
cover:  "/assets/salad-2487775_1920.jpg"
cover:  "/assets/tomatoes-5356_1920.jpg"
cover:  "/assets/tomatoes-1280859_1280.jpg"
cover:  "/assets/tomato-699731_1920"
cover:  "/assets/tomato-1205699_1920"
cover:  "/assets/tomatoes-320860_1920"
cover:  "/assets/tomatoes-1220774_1920"
cover:  "/assets/vegetable-crate-2392476_1920"
cover:  "/assets/vegetables-760860_1920"
cover:  "/assets/food-1932466_1920"
cover:  "/assets/lasagna-1900529_1920"
cover:  "/assets/olive-oil-1412361_1920"
{% endcomment %}


# はじめに
　GitHubPagesでブログをやっています。Jekyllのテーマを「Centrarium」にしたところ、当初はトップページに記事が表示されない問題が発生しました。これは、プラグインを書き換えることで解決しました（参考：[GitHubでのブログ構築。苦労したひとつのこと](https://hoiko-takahashi.github.io/hoiko-blog/diary/2020/06/17/My-Blog-is-started.html)）。

　これで無事、記事が表示されたのですが、次なる問題が発生します。

　**日本語記事の場合、概要ではなく、全文が表示されてしまいます。**かっこ悪いので、なんとかしましょう。

# 参考になったサイト
　英語ではない原語で、"truncatewords"がうまく動かないという問題について書かれています。

* [Make "truncatewords" and "truncate" work for non-English characters #166](https://github.com/Shopify/liquid/issues/166)  

# index.htmlを書き換える
　26行目あたりにある「 truncatewords: 50 」が犯人です。「文字列を指定語数（この場合50文字）以下になるように切り詰める」命令だそうで、これが英語以外ではうまく動作しません。そこで、「truncate」に置き換えます。何が違うのかわかりません。どうして200なのかもわかりません。ですが、これを書き換えたら、思った通りの表示になりました。

<script src="https://gist.github.com/Hoiko-Takahashi/9eefb8a5e2157b8c93f58ee709bb2364.js"></script>

{% comment %}
「[GitHub Gist](https://gist.github.com/)」
{% endcomment %}
