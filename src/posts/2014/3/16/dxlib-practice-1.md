---
title: "DXライブラリできれいなフォントを表示する"
published: "2014-03-16 03:20:28 +0900"
updated: "2014-03-16 03:20:28 +0900"
---

![](../../../../images/2014/3/16/dxlib-practice-1-1.png)

# 早速見ていただきましょう

ソースコードはこちら。

[5000164/dxlib-practice-1](https://github.com/5000164/dxlib-practice-1)

# DXライブラリで1番最初に確認したのがフォントの表示

ゲームのようなものを作りたいなと考えていて、知人に教えてもらったDXライブラリを使うことにしました。

[ＤＸライブラリ置き場　ＨＯＭＥ](http://homepage2.nifty.com/natupaji/DxLib/index.html)

その際に、1番初めに確認したことがフォントの表示でした。

フォントの美しさはモチベーションに直結します。

# 結果はごらんの通り

美しいフォントを表示させることができました。

ちなみに比較対象として、デフォルト設定でのフォントを下部に表示しています。

# フォントをきれいに表示するには1行追加するだけ

```cpp
ChangeFontType(DX_FONTTYPE_ANTIALIASING_8X8);
```

この文を追加するだけです。

この文を追加することでフォントにアンチエイリアスをかけてくれます。

[ＤＸライブラリ置き場　リファレンスページ](http://homepage2.nifty.com/natupaji/DxLib/function/dxfunc_graph2.html#R17N24)

# よりうつくしい表示のために若干の影をつけています

アンチエイリアスをかけるだけで十分きれいに表示されます。

ですが、ここではよりフォントを際立たせるために、若干の影をつけています。

まずは背景に影を描画。

フォントを描画したあとにガウシアンフィルタをかけるのがポイント。

```cpp
// 影の表示開始位置
text_x = font_size + shadow_offset_x;
text_y = font_size + shadow_offset_y;

// 影のベースとなる文字列を描画
for (int row = 0; row &lt; 5; row++)
{
DrawString(text_x, (int)(text_y + ((font_size * line_height) * row)), text[row], shadow_color_dx);
}

// ガウスフィルターを施して影にする
GraphFilter(backscreen, DX_GRAPH_FILTER_GAUSS, 8, 50);
```

背景ができたら、普通にフォントを描画します。

```cpp
// テキスト表示開始位置
text_x = font_size;
text_y = font_size;

// 文字列の描画
for (int row = 0; row &lt; 5; row++)
{
DrawString(text_x, (int)(text_y + ((font_size * line_height) * row)), text[row], font_color_dx);
}
```

これで完成です。

# まとめ

もちろん処理の負荷が高くなるとのことですが、美しいフォントの表示が可能であると知れて満足です。
