+++
title = "範囲入力フォーム"
draft = false
tags = ["日報テンプレート", "入力フォーム", "編集者権限"]
weight = 180
# description = "チャプター"
+++

{{<imgproc icatch.png "範囲入力フォームを含んだ日報テンプレート" />}}

スライダー上のつまみを左右にドラッグすることで入力が可能なフォームです。見た目は[スライダ入力フォーム](/org/groupsetting/template/step/)と似ていますが、スライダーレール上につまみが2つあるのが本フォームの特徴です。
つまみが2つありこれらを左右にドラッグすることで、ある値の範囲入力ができるようになります。

スライダーの範囲は予め設定しておく必要があります。最小値がレールの左端、最大値がレールの右端になります。スライダ上のつまみが動く量は「刻み」として設定します。
最小〜最大の範囲を設定する性質上、予め入力の範囲がわかっているものに適しています。

スライダーはスワイプ操作でつまみが移動できるため、特にスマートフォンやタブレットなどのタッチパネル操作に対応した機器と相性が良いです。もちろん、PCでもマウスを使用して入力が可能です。

例えば「気温」「室温」「水温」のようにある程度入力範囲が限定されているデータと相性が良いフォームです。
一方で上限や下限が推測できないデータには不向きです。

## 範囲入力の初期設定

ポイントはスライダーレールの範囲を決める「最小値」「最大値」そしてつまみの移動量を決める「刻み」です。この3つの要素でスライダーレールの「密度」が決まります。
密度が高すぎるとつまみの操作がしにくくなり、操作性が低下してしまいます。密度が高くなりすぎないように注意してください。

|名称|説明|
|---|---|
|表示名|項目見出しエリアに表示される文字です|
|色|項目見出しエリアの背景色を設定できます。灰色・茶色・緑色・紺色・赤色から選択してください。初期値は灰色です|
|サイズ|表示名の文字サイズを最小・小・中・大の４段階から設定できます。初期値は「中」です。表示名が長すぎる場合は設定が無視されます|
|メモ|入力エリアの画面左上に赤文字で表示されます。日報・チェックシートの作成者が迷うことのないように補足文として活用できます|
|入力必須|これがONの場合、ファイルが添付されていない場合日報の提出ができなくなります|
|初期値|日報新規作成時に最初から文字を入力済みにできます。不要の場合は空欄にしておきます|
|幅|1〜12の幅を選択できます。推奨幅は4〜12です。最小値〜最大値の幅が広い場合はメモリが細かくなってしまうため、広い幅を指定すると操作しやすくなります|
|最小値|スライダーの左端の値を指定します。負数も扱えます|
|最大値|スライダーの右端の値を指定します。負数も扱えます|
|初期値（最小）|日報作成時にスライダーの最小つまみが配置される位置を指定します|
|初期値（最大）|日報作成時にスライダーの最大つまみが配置される位置を指定します|
|刻み|つまみの１メモリ単位を指定します。例えば2なら 2 , 4 , 6のように増えていきます。小数点も指定できます。初期値は1です|
|単位|数値の単位を指定します。例えば気温であれば「度」と入力します。単位は入力時の画面左上にヒントとして表示されます|

## 範囲入力フォームのテンプレートを作る

範囲入力フォームのみで構成されたサンプルのチェックシート用テンプレートを設計した画面です。
{{<imgproc template.png "範囲入力フォームのみで構成されたチェックシートテンプレートの例" />}}

左側の「気温」は問題有りませんが、あえて問題のあるアンチパターンを右側に配置しました。これがどのように悪い結果をもたらすのかについても併せて確認していきます。

### 範囲入力チェックシートの入力画面

範囲入力チェックシートの作成画面を表示します。
{{<imgproc input.png "範囲入力の画面イメージ。アンチパターンは密度が高すぎて目盛りが塗りつぶされている状態になっています。" />}}

下段左の「合格範囲」の範囲入力は密度が低いため操作しやすい一方で、アンチパターン（右上）は目盛りでスライダレールが塗りつぶされてしまっていることがわかります。
アンチパターンでは範囲が-100〜100の200と広い上に、刻みが0.2のためこの狭い範囲に1000パターンも詰め込まれている状態です。つまみを少し動かす操作は非常に難しくなり、狙った値で止めることが困難になります。
今回は極端な例を示しましたが、密度をある程度低く抑えることで入力の操作性が良くなります。多くても密度は100以下に抑えるようにしてください。

### 範囲入力の日報を受け取ったときにどのように見えるのか？

{{<imgproc post.png "スライダ入力フォームを含んだ日報を受信したときの例。スライダはそのまま表示されるが読み取り専用となるため動かすことはできない" />}}

スライダーがそのまま表示されますが、目盛りは省略されます。正確な値は各フォームの左上に記載されます。
スライダーレールが表示されることで入力された範囲が全体にたいして広いのか？狭いのか？といったことが視覚的に判別できます。

## データ活用編

範囲入力はスライダーレール上のつまみが2つあるため、内部的には次のような構造でデータを記録しています

```javascript
{
  min: 3,
  max: 10
}
```

minがスライダ上の左側のつまみを表し、maxがスライダ上の右側のつまみを表しています。このように最大・最小の2つの値を持つため、単純な集計ができません。
よって範囲入力のデータは主にCSVに出力した上で使用することになります。範囲入力フォームのデータ対応は以下の表のとおりです。

|[集計可否](/report/totalling/form/)|[CSV出力](/report/totalling/csv/)|[PDF出力](/report/read/pdf/)|[文字検索](/report/read/list/)|
|:---:|:---:|:---:|:---:|
|✗|○|○|○|


### 範囲入力の日報をCSVに出力する

範囲は「最小」と「最大」の２つのデータを持っているため、CSV出力時には１つの範囲入力に付き最小最大の２つの列が自動で生成されて分けて出力されます。
{{<imgproc csv.png "範囲入力フォームを含んだ日報をCSVに出力したときの例。最小の列と最大の列の2つに分けてCSVに出力されます" />}}
見やすいように項目ごとに色分けをしてみました。J列とK列、L列とM列、N列とO列、P列とQ列がそれぞれのペアになります。
分けて出力されるため加工や分析に適した計上です。

### PDF出力

なお、PDFに出力したときはこのように表現されます
{{<imgproc pdf.png "範囲入力フォームを含んだ日報をPDFに出力したときの画面イメージ" />}}

### サンプルデータ

このページで使用した実際のサンプルをダウンロードできます

{{<attachments style="orange" />}}
