---
title: "EasyLanguage: 独自インジケーターの線を元の銘柄のチャートに重ねて表示する"
linkTitle: "独自インジケーターの線を元の銘柄のチャートに重ねて表示する"
url: "/p/8v8hs3c"
date: "2020-05-02"
tags: ["EasyLanguage"]
---

トレステで作成した独自のインジケーターをチャートに適用すると、デフォルトではサブチャート（別のウィンドウ）に描画されるようになっています。
デフォルトで最初の銘柄のウィンドウ領域に描画されるようにするには下記のように設定します。

1. トレードステーション開発環境の EasyLanguage エディタ領域で右クリック
2. `プロパティ` を選択
3. `スケーリング` タブの `スケール位置` で __`元データに軸を合わせる`__ を選択
4. `F3` キーで再コンパイル

{{< image border="true" src="img-001.png" >}}

