---
title: "なぜ営業キャッシュフローでは減価償却費をプラスとして扱うのか？"
url: "/p/jyreg5t"
date: "2018-10-10"
tags: ["財務分析"]
---

大きな設備投資などを行うと、損益計算書 (P/L) では減価償却費として毎年少しずつ費用計上していくことになります。
一方、キャッシュフロー計算書では、減価償却費がプラスとして計上されているのを見て最初は疑問に思うかもしれません。

```
営業活動によるキャッシュ・フロー
--------------------------------
当期純利益                 1500
   減価償却費               300  ←なぜプラス？
   退職・年金費用         △200
   ...
```

この理由は、営業キャッシュフローのベースになっている「当期純利益」の内訳にあります。
当期純利益にはすでに減価償却費だけマイナスされた値になっており（損益計算書でマイナス計上されたものが反映されている）、この数値をそのまま営業キャッシュフローの値として使ってしまうと、実際には現金の流れがないのにキャッシュフローがマイナスになってしまいます。
そのため、減価償却費の分を足してやることで、その部分のキャッシュフローを±0にしています。

```
営業活動によるキャッシュ・フロー
--------------------------------
当期純利益                 1500  ←実は既に減価償却費の -300 が含まれている
   減価償却費               300  ←上記のマイナス分を打ち消して 0 にする
   退職・年金費用         △200
   ...
```

ひとことで言うと、当期純利益の内訳から減価償却費に当たる部分を取り除いているということです。
つまり、ただの計算上の調整ですね。

