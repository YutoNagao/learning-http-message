# HTTPでやりとりする仕組み

<!-- Markdown記法のヒント

コード記法（1行の中に埋めたい場合）

`code`

コードブロック記法（複数行）

```
print('a')
print('b')
```

-->

## 実習でやったこと (Y)

・Chrome開発者ツールの「Network」タブを使ってみる  
・学校のホームページのHTTPレスポンスを確認する  

## 自分で調べたこと

HTTP/1.1とHTTP/2の違いについて調べてみた  
　参考　<https://www.kagoya.jp/howto/webhomepage/http-2/>  

## HTTPメッセージ (kd.txt) のうち、最も重要だと思う部分を貼り付けてください

```
Date: Fri, 07 Jun 2019 00:39:08 GMT

Server: Apache

X-Cached: Fri, 07 Jun 2019 00:39:09 GMT

X-Pingback: https:/xmlrpc.php

Last-Modified: Fri, 07 Jun 2019 00:39:09 GMT

X-Accel-Expires: 0

Cache-Control: max-age=300

Expires: Fri, 07 Jun 2019 00:44:08 GMT

Vary: Accept-Encoding

Connection: close

Content-Type: text/html; charset=UTF-8
```

## それはなぜですか？

HTTPレスポンスのメッセージヘッダーの部分で、  
Webサーバーの情報が書かれているから。  

## わかったこと・気づいたこと

※Chromeの開発者ツールを使って  
・１つのページでたくさんのファイルが読み込まれていること  
・imgやCSSなど要素ごとに絞って検索が可能  
ということがわかった。  
また、読み込みにかかった時間らしきものが書かれていて、  
学校のサイトのような情報量が多いページだと２秒ほどかかっていたが、  
Googleなど情報量の少ないページだと７００ミリ秒くらいだった。  
