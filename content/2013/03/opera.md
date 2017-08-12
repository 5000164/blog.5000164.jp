+++
title = "Operaの右クリックで表示中のページのURLを取得したり別のブラウザで開いたり"
date = 2013-03-04T04:16:33+00:00
url = "2013-03-opera"
+++
{{< figure src="/images/2013/03/de_20130303_Opera.jpg" title="" >}}

&nbsp;

# Operaの右クリックをカスタマイズ

Operaの右クリックで表示されるメニューをちょっとカスタマイズするだけですごく使いやすくなりますよ

便利ですよ

というわけでOperaのmenu.iniに下記を追記します

&nbsp;

## 現在表示中のページのタイトルとURLを取得する

<pre class="brush: jscript; gutter: false; title: ; notranslate" title="">[Document Popup Menu]
～中略～
++++++++++++++++++--
Item, "Copy URL" = Go to page, "javascript:(function(){window.prompt('', document.title+'\n'+location.href);})();" & Delay, 100 & Cut & Cancel
</pre>

## 現在表示中のページをChromeで開く

<pre class="brush: jscript; gutter: false; title: ; notranslate" title="">[Document Popup Menu]
～中略～
++++++++++++++++++--
Item, "Open page in Google Chrome"=Execute program, "chrome","%u"
</pre>

## リンク先のページをChromeで開く

<pre class="brush: jscript; gutter: false; title: ; notranslate" title="">[Link Popup Menu]
～中略～
++++++++++++++++++--
Item, "Open link in Google Chrome"=Execute program, "chrome","%l"
</pre>

# 結論

ちょっとしたカスタマイズですごく幸せになれます