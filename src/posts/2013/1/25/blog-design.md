---
title: "ブログのデザインを変更しました"
published: "2013-01-25 03:12:34 +0900"
updated: "2013-01-25 03:12:34 +0900"
---

ブログのデザインを変更しましたよ。

# 変更点

# ロゴ

今まではスクロールしてもロゴの位置が変わらないようにしてたのですが、今回はスクロールしたら一緒にスクロールするようにしました。

それに伴って目立って邪魔にならないように色を抑えてたものを、普通に見えるように変更。

マウスをホバーした時の画像は薄いロゴを流用したので修正する必要あり。

# 文字サイズ

本文の文字サイズを18pxから16pxへ変更。

最初は大きくていいなーと思ってたけど、見てるうちにあとほんの少し小さい方が読みやすいなと感じたから。

それに伴い行間もほんのり狭く。

# ループスクロール

そして最大の変更点はこれ。

ループスクロール（おれが今命名）です。

ずっとやってみたかったことをついにやってみた。

思ったよりも簡単に実装できてよかった。

ちゃんとデバッグしてないけど。

これは、本文を読み終わって「トップへ戻る」ボタンを配置するくらいなら勝手にトップに戻してしまえ、という思想に基づいてデザインしました。

ロゴを固定するのをやめたのも、このループスクロールで下にまたロゴが出てくるからです。

でも実際に実装してみると、区切りがわかりづらいですね。

区切られた部分になにか目印を置いて繰り返しを示す必要がありますね。

あとは、現状では上から下へのスクロールしか対応してないけど、これが上下どっちのスクロールでもいけるようになればいいなと思います。

# まとめ

全体的にサイトが見やすくなって大歓迎です。

特にずっとやってみたかったループスクロールが面白くて楽しいです。

あとは徐々に実用性を高めていきたいと思います。
