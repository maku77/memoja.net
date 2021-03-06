---
title: "EasyLanguage: レーダースクリーンのセルのフォーマットを変更する（中央寄せ、小数点以下の表示など）"
linkTitle: "レーダースクリーンのセルのフォーマットを変更する（中央寄せ、小数点以下の表示など）"
url: "/p/g9r8n3h"
date: "2020-05-03"
tags: ["EasyLanguage"]
---

セル内のテキストを左寄せ／中央寄せ／右寄せ
----

{{< image border="true" src="img-001.png" >}}

レーダースクリーン用のストラテジを作って、セル内にテキストを表示すると、デフォルトではすべて右寄せになったりして見映えがよくありません。
セル内のテキストを中央寄せなどで表示したいときは、次のように設定します。

{{< image border="true" src="img-002.png" >}}

1. TradeStation 開発環境のエディタ領域で右クリック → __`プロパティ`__ を選択
2. `グリッドのスタイル` のタブの __`整列する`__ の項目で「中央寄せ」を選択
3. `F3` キーで再コンパイル

これで、レーダースクリーンにストラテジーを追加したときに、最初からセル内のテキストが中央寄せで表示されるようになります。
インジケータープロパティのダイアログで、プロット項目が出てこない場合は、一度 `F3` キーでコンパイルしてから開き直すと表示されます。

### （おまけ）上記の表示をするために使った EL コード

{{< code title="!テストインジケーター" >}}
once begin
    for Value1 = 1 to 3 begin
        SetPlotColor(Value1, White);
        SetPlotBgColor(Value1, DarkBlue);
    end;
end;

once (LastBarOnChart) begin
    Plot1("左", "指標1");
    Plot2("中", "指標2");
    Plot3("右", "指標3");
end;
{{< /code >}}


セル内の数値の表示フォーマットを設定する
----

{{< image border="true" src="img-003.png" >}}

レーダースクリーンのセル内に表示する数値のフォーマットも、同様にインジケータープロパティから設定することができます。
上記の例では、`指標1` から `指標4` まで全て同じ、`123.45` という値をプロットしているのですが、数値の表示フォーマット設定で、小数点以下を何桁まで表示するかを変更しています。

* `指標1` ... 小数点以下 3 桁まで表示（上の図では、0 パディング）
* `指標2` ... 小数点以下 2 桁まで表示
* `指標3` ... 小数点以下 1 桁まで表示（上の図では、四捨五入で切り上げ）
* `指標4` ... 小数点以下 0 桁まで表示（上の図では、四捨五入で切り捨て）

下の図は設定の例です。

{{< image border="true" src="img-004.png" >}}

カテゴリー項目で __`数値`__ を選択すると、小数点以下の表示桁数や、マイナス値をどのように表示するかなどを設定することができます。
もちろん、このフォーマット指定が有効になるのは、下記のようにプロット時に数値を指定したときのみです（文字列をプロットすると、これらの設定は無視されます）。

{{< code >}}
Plot1(123.45, "指標1");
{{< /code >}}


### （おまけ）上記の表示をするために使った EL コード

{{< code title="!テストインジケーター" >}}
once begin
    for Value1 = 1 to 4 begin
        SetPlotColor(Value1, White);
        SetPlotBgColor(Value1, DarkBlue);
    end;
end;

once (LastBarOnChart) begin
    Plot1(123.45, "指標1");
    Plot2(123.45, "指標2");
    Plot3(123.45, "指標3");
    Plot4(123.45, "指標4");
end;
{{< /code >}}

