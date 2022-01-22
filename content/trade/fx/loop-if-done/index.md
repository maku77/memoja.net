---
title: "繰り返し IFD 注文の損失拡大表"
url: "/p/axfr8wi"
date: "2016-01-12"
tags: ["FX", "戦略"]
---

{{< image w="500" src="loop-if-done.png" title="外為オンラインの「iサイクル注文」より" >}}

例えば、ドル円を値幅 0.1 円ごとに買い注文を入れ（ナンピン）、0.1 円上がるごとに利確するといったことを繰り返すと、**レンジ相場であるかぎり利益を上げ続けることができます**。
外為オンラインのiサイクル注文や、マネースクウェア・ジャパンのトラリピなどがこの仕組みを提供しています。

魅力的な戦略に見えますし、しばらくの間は順調に利益を上げ続けることもありますが、端的に言うと**バリバリのナンピン戦略**です。
一方的に円高が進む局面になると、急激に損失が膨らんでいきます。
どんどんポジションサイズを増やしていくのですから当然です。

下記は、0.1 円ごとに 1000 通貨のナンピン買い注文を入れ続けた場合に、損失がどのように膨らんでいくかを示した表です。
ナンピン戦略を取り入れるときは、損失の急激な拡大に耐えられるようにレバレッジ調整するか、想定範囲外の価格変動があったときには新規ポジションを取らないようにするなど、資金管理を徹底しましょう。

| Price | Loss |
| ---- | ---- |
| 120.0 | 0 |
| 119.9 | -100 |
| 119.8 | -300 |
| 119.7 | -600 |
| 119.6 | -1000 |
| 119.5 | -1500 |
| 119.4 | -2100 |
| 119.3 | -2800 |
| 119.2 | -3600 |
| 119.1 | -4500 |
| 119.0 | -5500 |
| 118.9 | -6600 |
| 118.8 | -7800 |
| 118.7 | -9100 |
| 118.6 | -10500 |
| 118.5 | -12000 |
| 118.4 | -13600 |
| 118.3 | -15300 |
| 118.2 | -17100 |
| 118.1 | -19000 |
| 118.0 | -21000 |
| 117.9 | -23100 |
| 117.8 | -25300 |
| 117.7 | -27600 |
| 117.6 | -30000 |
| 117.5 | -32500 |
| 117.4 | -35100 |
| 117.3 | -37800 |
| 117.2 | -40600 |
| 117.1 | -43500 |
| 117.0 | -46500 |
| 116.9 | -49600 |
| 116.8 | -52800 |
| 116.7 | -56100 |
| 116.6 | -59500 |
| 116.5 | -63000 |
| 116.4 | -66600 |
| 116.3 | -70300 |
| 116.2 | -74100 |
| 116.1 | -78000 |
| 116.0 | -82000 |
| 115.9 | -86100 |
| 115.8 | -90300 |
| 115.7 | -94600 |
| 115.6 | -99000 |
| 115.5 | -103500 |
| 115.4 | -108100 |
| 115.3 | -112800 |
| 115.2 | -117600 |
| 115.1 | -122500 |
| 115.0 | -127500 |
| 114.9 | -132600 |
| 114.8 | -137800 |
| 114.7 | -143100 |
| 114.6 | -148500 |
| 114.5 | -154000 |
| 114.4 | -159600 |
| 114.3 | -165300 |
| 114.2 | -171100 |
| 114.1 | -177000 |
| 114.0 | -183000 |
| 113.9 | -189100 |
| 113.8 | -195300 |
| 113.7 | -201600 |
| 113.6 | -208000 |
| 113.5 | -214500 |
| 113.4 | -221100 |
| 113.3 | -227800 |
| 113.2 | -234600 |
| 113.1 | -241500 |
| 113.0 | -248500 |
| 112.9 | -255600 |
| 112.8 | -262800 |
| 112.7 | -270100 |
| 112.6 | -277500 |
| 112.5 | -285000 |
| 112.4 | -292600 |
| 112.3 | -300300 |
| 112.2 | -308100 |
| 112.1 | -316000 |
| 112.0 | -324000 |
| 111.9 | -332100 |
| 111.8 | -340300 |
| 111.7 | -348600 |
| 111.6 | -357000 |
| 111.5 | -365500 |
| 111.4 | -374100 |
| 111.3 | -382800 |
| 111.2 | -391600 |
| 111.1 | -400500 |
| 111.0 | -409500 |
| 110.9 | -418600 |
| 110.8 | -427800 |
| 110.7 | -437100 |
| 110.6 | -446500 |
| 110.5 | -456000 |
| 110.4 | -465600 |
| 110.3 | -475300 |
| 110.2 | -485100 |
| 110.1 | -495000 |
| 110.0 | -505000 |

最初は 1000 通貨のポジションだとしても、10 円下がるまでナンピン戦略を続けると、10 / 0.1 = 100 回のナンピンで、10 万通貨を持つことになります。
そこから 0.1 円下がると、-1 万円です。

もちろん、そこまで円高が進んでいく過程で、何回も利食いできているでしょうから、上記がそのまま損失額になるわけではありません。それでもやはり損大利小です。基本的にはレンジ相場を狙った戦略と捉えたほうがよさそうです。


おまけ (上記の表作成に使ったスクリプト）
----

{{< code lang="ruby" title="nanpin.rb" >}}
#!/usr/bin/env ruby

HIGH = 120  # 上限価格
LOW = 110   # 下限価格
STEP = 0.1  # 何円ごとにナンピンするか
POS_SIZE = 1000  # 何通貨ずつナンピンするか

factor = 0
loss = 0
HIGH.step(LOW, -STEP) do |price|
  printf "| %.1f | %d |\n", price, loss
  factor += POS_SIZE * STEP
  loss -= factor
end
{{< /code >}}
