---
title: "Mistel Barocco と Karabiner-Elements で コマンドキーを単体で押したときに、英数・かなキーを送信する の設定を使っている時に Todoist のタスク複数選択が動かない現象の回避方法"
published: "2018-12-05 21:35:40 +1100"
updated: "2020-02-04 16:12:55 +0100"
---

# 結論

- Command キーを押したまま Option キーを一回押して離す

# 発生した現象

- Command キーを押しながら Todoist のタスクをクリックすると編集になってしまう
    - 期待している挙動としては、Command キーを押しながらクリックすることでタスクを複数選択できること
        - 今まではできていたような気がするのだが最近できなくなったような気がする
            - Mojave への OS アップデート？
        - 外付けのトラックパッド、トラックボールだと複数選択できないのだが、Mac 本体のトラックパッドだと複数選択することができる

# 回避方法を見つけた経緯

- Mistel Barocco の設定が悪いのかと思って Mistel Barocco の設定をリセットして最初から設定し直す
- それでもうまく動かなかった
- Karabiner-Elements を終了してみる
- うまく動いた
- Karabiner-EventViewer でイベントを確認してみる
- いろいろ連打して動作確認をしていたら左 Command を入力した時に lang2 となる時と left_gui となる時があることに気づく
- Karabiner-Elements を終了すると left_gui だけになる
- Karabiner-Elements が起動している状態でも left_gui になる条件を探す
- 一度 Command キーを押した後に他のキーを押すと left_gui として認識される
    - たぶん コマンドキーを単体で押したときに、英数・かなキーを送信する の設定で英数キーが送信されているのかも知れない
    - 他のキーを押すことで英数キーを送信しなくなって Command キーとして送信されるのかも知れない

# 2020.2.4 追記

- 設定を変えることで対応できたかも知れない
    - [Karabiner-elementsでFor Japanese(日本語環境向けの設定)を使うとCommandキー組み合わせのショートカットが効かなくなる問題解決した - ひと夏の技術](https://tech-1natsu.hatenablog.com/entry/2018/10/21/160216)
