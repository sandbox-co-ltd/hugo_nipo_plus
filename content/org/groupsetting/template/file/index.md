+++
title = "ファイル入力フォーム"
draft = false
tags = ["日報テンプレート", "入力フォーム", "編集者権限"]
weight = 230
description = "日報やチェックシートにZipやExcelなどのバイナリーファイルを添付するフォームを追加します。添付されたファイルはNipoPlusのサーバ上に保管され、日報本体を削除すると連動してサーバ上からファイルが削除されます"
+++

{{<imgproc file.png "ファイル入力フォームを含んだ日報テンプレートの例" />}}

日報やチェックシートににファイルを添付できるフォームを追加できます。**１つのファイルにつき１MB、最大で10ファイルまで**ファイルを添付できます。
現場写真など画像データを添付したい場合は、ファイル入力フォームではなく写真入力フォームが別途用意されています。もちろん本フォームでも写真を添付できますが、いくつかの理由により[写真入力フォーム](/org/groupsetting/template/picture/)の利用を推奨します。
ファイルの追加はファイル入力フォームをクリックするか、ファイル入力フォーム上にファイルをドラッグ＆ドロップします。
追加と同時にアップロード処理が行われます。アップロードが完了するまで日報の保存はできません。

## ファイル入力フォームの初期設定

ファイル入力フォームの初期設定項目は少ない上に、そこまで重要な項目も特にありません。

|名称|説明|
|---|---|
|表示名|項目見出しエリアに表示される文字です|
|色|項目見出しエリアの背景色を設定できます。灰色・茶色・緑色・紺色・赤色から選択してください。初期値は灰色です|
|サイズ|表示名の文字サイズを最小・小・中・大の４段階から設定できます。初期値は「中」です。表示名が長すぎる場合は設定が無視されます|
|メモ|入力エリアの画面左上に赤文字で表示されます。日報・チェックシートの作成者が迷うことのないように補足文として活用できます|
|入力必須|これがONの場合、ファイルが添付されていない場合日報の提出ができなくなります|
|初期状態でONにする|これがONの場合、日報作成時にこのチェックボックスはONの状態でスタートします|
|幅|1〜12の幅を選択できます。推奨幅は3〜4です|

## ファイル入力フォームの日報テンプレートを作成

ファイル入力フォームのみで構成された日報テンプレートを作成しました。このテンプレートをもとに入力時、出力時の画面イメージや操作手順を解説していきます。

{{<imgproc template.png "テンプレートの構造はこのように設計しました。すべてのフォームで色を替えてみました" />}}

設定項目が非常に少ないため、ここではカラーを全部変更してみました。カラフルな入力フォームがどのように見えるのかについてもご注目ください。

### ファイル入力フォームの使い方

使い方はシンプルです。「ファイルを選択」と書かれたフォームをタップして添付するファイルを選ぶだけで日報に添付ファイルとして紐付けることができます。
PCの場合はファイルをドラッグ＆ドロップすることでも追加できます。
1つの入力フォームに対して10ファイルまで添付できるので、この例では最大40ファイルまで添付できます。
ただし1ファイルに付き1MBを超えることはできません。

{{<imgproc input.png "ファイル入力フォームを使った日報の作成画面イメージ。添付したファイルは即座にアップロードされます。" />}}

{{<alice pos="right" icon="default">}}
特にそれ以上の見ごたえがある項目はないので無駄にカラフルにしてみました
{{</alice>}}

## 受信日報の表示

添付時のファイル名がリスト上に表示されます。クリックでそのファイルをダウンロードできます。

{{<imgproc post.png "ファイルフォームを含んだ日報を受信した画面イメージ" />}}

添付したファイルが写真データであっても表示されず、一旦ダウンロードして端末上で表示する必要があります。このような点から、写真データの場合は専用の写真入力フォームを検討してください。
またファイルは添付時の名前とダウンロード時では名前が少し変わります。重複防止と、より高い安全性を保つためにアップロード時のファイル名に加えて日付とランダムな文字列が自動で付与されます。

{{<alice pos="right" icon="shield">}}
日報表示画面ではもとのファイル名のままだよ。ダウンロードするときだけ名前が少し長くなるんだ。
{{</alice>}}

## データ活用

ファイル入力フォームはCSV出力やPDF出力に対応しておらず、またその性質上、検索や集計にも対応しておりません。
よって行えることは、添付されたファイルをダウンロードすることだけです。

|[集計可否](/report/totalling/form/)|[CSV出力](/report/totalling/csv/)|[PDF出力](/report/read/pdf/)|[文字検索](/report/read/list/)|
|:---:|:---:|:---:|:---:|
|✗|✗|✗|✗|

### ファイルの安全性

ファイル入力フォームを使って提出されたファイルは、NipoPlusのWebサーバ上に保管されます。
ファイルには非常に長いダウンロード用URLが自動で割り当てられます。このURLにはトークンが含まれており、１文字でも異なる場合そのファイルをダウンロードできません。
URLそれ自体にIDとパスワードが含まれているものとお考えください。例えばURLは次のような形式で構成されています。

```sh
https://firebasestorage.googleapis.com/v0/b/nipo-plus.appspot.com/o/a16h8Q74slMYzLlsHlCg%2Fnipodefaultgroup%2FAEUfmePA4eTHGPCleVQJ%2F20220510164077Vzm_28CE19C9-B5F3-4E22-A873-2DXDE010EX6A.jpg?alt=media&token=9a6c1908-ea48-zc0e-b858-fd42870b014f9
```

このように非常に長いURLになっています。URL内には添付元の日報IDやグループID、ファイルトークンキーなどが含まれています。
換言すればURLが漏洩することでそのファイルを第三者が閲覧できてしまうリスクがあります。[通信は全て暗号化](/system/security/)されているためURLの漏洩リスクは限りなく低いですが用心に越した事はありません。

{{<alice pos="right" icon="shield">}}
上記URLはいくつかのフェイクを入れているため実際にダウンロードすることはできません。1文字でも異なれば弾き返します！
{{</alice>}}

### サンプルデータ

このページで使用した実際のサンプルをダウンロードできます

{{<attachments style="orange" />}}
