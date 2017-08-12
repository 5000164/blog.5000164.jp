+++
title = "最初から完璧を求めない - 「TDDBC in Tokyo 2014-11」に参加しました"
date = 2014-11-22T23:08:52+09:00
url = "2014-11-tddbc"
+++

「TDDBC in Tokyo 2014-11」に参加しました
====
イベントの詳細はこちら。  
[TDDBC in Tokyo 2014-11 - TDDBC | Doorkeeper](http://tddbc.doorkeeper.jp/events/17353)  
  
課題はこちら。  
[TDD演習課題 - TODOリストアプリ](https://gist.github.com/kyonmm/6102436)  
  
私の組の実装はこちら。  
[5000164/tddbc-tokyo_2014-11](https://github.com/5000164/tddbc-tokyo_2014-11)

理解しやすいテストを書く
====
基調講演は xUnit Test Patterns の著者である Gerard Meszaros さんの「Refactoring a Test」だった。  
単体テストはわかりやすく書く。  
悪いコードが示されて、ここはこうする、次はこうする、と話してくれた。  
1 つのテストコードは 5 行に抑える、7 行を超えると理解しづらくなる。  
カスタムアサーションというものを知った。  
すっきり書けるようになっててよかった。  

なにをテストしたいのか？
====
このテストケースではなにをテストしたいのかを明確にする。  
重要でないセットアップは 1 つのメソッドにまとめてしまう。  
こうすることで、どこにフォーカスしたいテストなのかがわかりやすくなる。

やっぱ英語はできないとだめだ
====
リアルタイムのヒアリングだとほとんど理解できなかった。  
単体テストの部分は、なんとなく知っている部分があったのでほんのりわかったが、機能テストとかの話になったら理解できなくなった。  
英語ができないってだけでアクセスできる情報が制限されるのってやっぱり残念だ。

TDD はやっぱりおもしろい気がする
====
あの感じ好きだ。  
設計とかをもっと考えられるようになりたい。

テストの粒度というか責務というかがわからない
====
というか全体的によくわかってない。  
これをまずは立ち読みしてみる。  
<div style="text-align: center;"><iframe src="http://rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=5000164-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=ss_til&asins=4798124583" style="width:120px;height:240px;" scrolling="no" marginwidth="0" marginheight="0" frameborder="0"></iframe></div>

やれるところからやる
====
いきなりはできない。  
最初から完璧な TDD を回すことはできない。  
経験が必要。  
やれないからやらないではいつまでもできない。  
やれるところからやる。  
実装するときに、TDD できそうか考える。  
やれそうならやる。  
やれないならなぜやれないのか考える。  
スキルが足りないのか、定義や分析が不十分なのか。  
再帰的に問題を洗い出す。  

TDD のできる領域とできない領域がある
====
TDD に調査分析はできない。  
テストファーストだけでは TDD ではない。  
テストでデザインするのが TDD。  
設計を考える。

テストは品質を担保する
====
相手が品質に納得できる必要がある。  
Hello, world! にテストはいらない。  
単体テストでやったことを機能テストでもやるか。  
やった方が品質は担保されるが工数がかかる。  
相手が納得できるところを探す。

他人に甘えていた
====
今までは、こういうのやりませんか？って呼びかけるだけだった。  
でもそれじゃだめだ。  
自分で勉強して、できるようになって、おれができるのでやりましょう、ってやるべきだった。  
環境に依存していちゃだめだ。  
やれるところからやる。  
自分のスキルがあって、その領域から一歩踏み出して経験して、どんどん領域を広げていくしかない。

勉強する
====
<div style="text-align: center;"><iframe src="//www.slideshare.net/slideshow/embed_code/41785717" width="425" height="355" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe></div> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/KyonMm/ss-41785717" title="テストファースト、自動テストを導入するという事について（@社内勉強会）" target="_blank">テストファースト、自動テストを導入するという事について（@社内勉強会）</a> </strong> from <strong><a href="//www.slideshare.net/KyonMm" target="_blank">Kyon Mm</a></strong> </div>
[「いまさら聞けないTDD/BDD超入門」最新記事一覧 - ITmedia Keywords](http://www.atmarkit.co.jp/ait/kw/tdd_bdd.html)  
[Mikado-Method - Google 検索](https://www.google.co.jp/search?q=Mikado-Method)