+++
title = "レート入力フォーム"
draft = false
tags = ["日報テンプレート", "入力フォーム", "編集者権限", "集計機能"]
weight = 320
description = "アプリストア等でおなじみの星アイコンを使った入力フォームを日報やチェックシートに追加できます。タップ操作で簡単に入力でき、見た目もシンプルでわかりやすいフォームで特にチェックシートと相性が良いです"
+++

{{<imgproc icatch.png "レート入力フォームを含んだ日報テンプレート" />}}


レート入力は多くの方が慣れ親しんでいる入力方式です。ネットショップの商品レビューやアプリストア上のレビューとしてもおなじみですね。
１クリックで入力ができるシンプルな操作性と、視覚的にも直感的でわかりやすいとても便利な入力フォームです。
一般的なアプリストアなどのレビューは５段階ですがNipoPlusでは設定を変更することでレートの数を変更できます。上限は決められていませんが多すぎると画面レンダリングに時間がかかる上に視認性が大幅に低下します。そのため多くても10程度に抑えるようにしてください。入力されたデータは**数値**として記録されるため、集計にも対応しています。
例えば100など極端に多い値は入力することはできません。  
より大きな数値を入力したい場合は[スライド入力フォーム](/org/groupsetting/template/step/)か、あるいは[数値入力フォーム](/org/groupsetting/template/math/)の利用を検討してください。
（ただし集計方式が異なります）

{{<alice pos="right" icon="please">}}
星が100個も並んでいたら爽快だけど使いにくいよね。例えば星が10個並ぶだけで「★★★★★★★★☆☆」このようになるのです。100個はさすがに厳しいでしょう？
{{</alice>}}

## レート入力の設定

|名称|説明|
|---|---|
|表示名|項目見出しエリアに表示される文字です|
|色|項目見出しエリアの背景色を設定できます。灰色・茶色・緑色・紺色・赤色から選択してください。初期値は灰色です|
|サイズ|表示名の文字サイズを最小・小・中・大の４段階から設定できます。初期値は「中」です。表示名が長すぎる場合は設定が無視されます|
|メモ|入力エリアの画面左上に赤文字で表示されます。日報・チェックシートの作成者が迷うことのないように補足文として活用できます|
|入力必須|これがONの場合、レートが0だと日報・チェックシートの提出ができません（レートは２回同じレートをクリックすると0にできます)|
|幅|1〜12の幅を選択できます。レートの最大数に応じて適切な幅を選んでください。推奨幅は4〜12です|
|最大値|レートの最大数を設定します。推奨は5〜10です。(大きすぎる値は操作性、処理速度の観点から推奨されません)|
|アイコンの種類|星・ハート・いいね・ペット・ペンの５種類から選択できます。初期値は「星」です。見た目が変わりますが機能としては一緒です|
|アイコンの大きさ|小さめ・大きめ・最大の３種類から選択できます。初期値は「小さめ」です。|

## レート入力のテンプレートを作成

レート入力だけで構成されたチェックシートテンプレートを作成しました。アイコンの種類やアイコンの数もそれぞれ変更しています。
レート入力パーツは全部で4つ使用しています。アンチパターンとして極端に星が多いものも１つ用意してみました。実際にどのように見えるのか？確認してみましょう

{{<imgproc template.png "レート入力だけで構成されたチェックシートテンプレートを作成しました。このテンプレートをもとに入力時、出力時の画面イメージについて解説します" />}}

### レートのチェックシートを入力する

先程のテンプレートを使って実際にチェックシート作成画面を開いてみました。

{{<imgproc input.png "レートのチェックシートを実際にスマートフォン・タブレットから入力する画面のイメージです。見え方は異なりますが項目等は一緒です" />}}

アイコンの大きさがそれぞれ違うのは設定でそのようにしたためです。アイコンの種類もそれぞれ異なるものがセットされていることがわかりますね。
下段の極端に多い値は星が100個あります。これはアンチパターンとしてあえて例示しましたが実際に入力する際は使い勝手が悪いため、実運用上は多くても10個程度に抑えてください。
上記画面では少し見にくいですが、各フォームの左上には選択されたレートの値が表示されます。

{{<alice pos="right" icon="here">}}
例えば下段の値は59であることが読み取れますね
{{</alice>}}

### レートの日報を受け取ったときにどのように見えるのか？

レートの含まれる日報やチェックシートは作成時とほぼ同じ見た目のまま表示されます。
アイコンの他、左上には実際の値も併記されます。数値がずらずらと並ぶより、視覚的に見えるほうが読み手の精神的負担も軽減されます。

{{<imgproc post.png "レート入力フォームを含んだチェックシートの受信画面" />}}

一見入力できそうな見た目をしていますが、提出されたデータは読み取り専用のためクリックしても星の数は変わりません。

## データ活用編

レート入力フォームのデータは数値であるため、集計やCSV出力など多くの機能に対応しています。

|[集計可否](/report/totalling/form/)|[CSV出力](/report/totalling/csv/)|[PDF出力](/report/read/pdf/)|[文字検索](/report/read/list/)|
|:---:|:---:|:---:|:---:|
|○|○|○|○|

集計方式は星の合計ではなく、星の選ばれた回数を集計する形式です。
アプリストアのレート集計と同じと考えてください。
星5の人はxx人・星4の人はyy人・・・というように集計されていますよね？NipoPlusでもあれとおなじスタイルで集計が行われます。

{{<alice pos="right" icon="here">}}
星5が10回で50・・・とはならないのです。集計を合計する[スライド入力フォーム](/org/groupsetting/template/step/)とはこの点が大きく異なります
{{</alice>}}

### レートの含まれたチェックシートを集計

レート入力の含まれたチェックシートは集計できます。先述の通り、各レートごとに選択された回数を集計する方式で集計が行われます。
この集計を更にスタッフごとに分けておこない、一覧表として出力します。詳しくは[データ集計](/report/totalling/transition/)を御覧ください。
純粋に合計として集計したい場合は、レート入力の代わりに[スライド入力フォーム](/org/groupsetting/template/step/)を使用してください。

{{<imgproc sum.png "レート入力フォームを含んだチェックシートの集計結果画面" />}}

またこの集計結果はそのままの形式でダウンロードすることもできます。

{{<alice pos="right" icon="here">}}
細かい点ですが選択したアイコンが一覧表に使用されているのもポイントです。視認性を高めるためにもアイコンの種類を分けると良いですね
{{</alice>}}

### レートの含まれたチェックシートをCSVに出力する

レートのデータをCSVに出力できますが、レートにおいては出力前にオプションの設定が可能です。CSV出力ボタンの右側にある下向きの三角ボタンをクリックすることで設定を表示できます。

{{<imgproc csvsetting.png "CSV出力前の設定画面（レート）は列展開のON/OFFが選べます。" />}}

レートに関する設定は「レートの展開」という項目です。

|名称|説明|
|---|---|
|列の展開をON|１つのレートに対して複数の列（例えば最大値が5であれば5列）が生成されます|
|列の展開をOFF|１つのレートに対して１列(1セルに数値が直接記載)のみ出力されます|

列展開がONだと列の数がどうしても多くなることに注意してください。列展開がONの場合は集計などに適しており、OFFの場合は保管用や視認用に適しています。
文章では伝わりにくいと思いますので、実際にONの場合とOFFの場合で同じチェックシートをCSVに出力したデータを比較してみます。

{{<imgproc csv.png "列展開がON・OFFの場合でそれぞれ比較しています。列数が双方で全く変わることがわかりますね。でもデータの指す意味としてはどちらも同じです。" />}}

{{<alice pos="right" icon="here">}}
アンチパターンとして例示した項目は100列も出力されるため結構大変なことになります。
{{</alice>}}

CSV出力は複数の日報やチェックシートを[まとめてCSV出力する](/report/totalling/csv/)方法と、[1つの日報・チェックシートだけをCSV出力](/report/read/csv/)する方法があります。詳細な手順は各ページを参照してください。

### データの検索

レート入力でセットされた値は数値ですが、検索用データベース上は（数値ではなく）数字として記録されるため文字として検索できます。例えば59のように直接文字で検索することで、該当する日報やチェックシートが検索できます。
ただ、数字に関する検索精度は比較的低いため、オマケ程度に捉えてください。

### レートのデータをPDFに出力する

最後にレートのデータをPDFに変換してみましょう。レートのアイコンはPDFによって使用できないものが含まれているため、PDF出力時はすべて●と○に置き換えられます。

なお、PDFに出力したときはこのように表現されます
{{<imgproc pdf.png "レート入力フォームを含んだ日報をPDFに出力したときの画面" />}}
集計した結果はCSVにエクスポートすることができます。実際のデータを確認したい方は本ページ末尾のサンプルデータからダウンロードできます。

{{<alice pos="right" icon="here">}}
設定したアイコンは無視されていることがわかりますね
{{</alice>}}

### サンプルデータ

{{<attachments style="orange" />}}
