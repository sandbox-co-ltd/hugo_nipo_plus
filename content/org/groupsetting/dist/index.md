+++
title = "日報の提出先を固定する"
draft = false
description = "スタッフ毎やテンプレート毎に提出先を細かく指定できます。指定がない場合は日報作成時にスタッフが自由に選択できますが可能であれば指定することでスタッフの日報作成業務負担を軽減でき、無用な混乱を避けることができます"
tags = ["スタッフ管理", "編集者権限", "グループの管理"]
weight = 20
+++

NipoPlusではスタッフが日報やチェックシートを書き終えたあと**提出先と共有先を選んで提出**します。
初期設定時では日報やチェックシートを書くスタッフが提出先や共有先を自由に選べます。
自由に選ばれると困る場合は管理者側が日報やチェックシートの提出先を指定して固定することもできます。日報やチェックシートの提出先を固定する方法は2つあります。

- スタッフごとに個別に提出先を指定する
- 日報テンプレートごとに提出先を指定する

競合してしまう設定の場合は、スタッフ毎の個別指定が優先されます。

## スタッフごとに個別に提出先を指定する

最も優先度が高い指定方法です。スタッフ一人ひとりに対して、「どの日報やチェックシートを使ったとき誰あてに提出するか」を細かく指定できます。すべてを設定する必要はなく必要な項目一部の設定でも有効です。

{{<alice pos="right" icon="here">}}
例えば **「Aさん」** が **「業務報告書」** を使った場合は **「X部長宛」** といった具合です
{{</alice>}}

設定手順は以下のとおりです。

1. グループ設定をクリック
1. スタッフ管理をクリック
1. 提出先を指定するスタッフ行で「日報の提出先を指定」をクリック
1. 設定する日報テンプレートを選択
1. 提出先を指定する
1. 共有先を指定する（任意）

{{<imgproc staffs.png "グループに所属しているスタッフ一覧から、提出先を指定したいスタッフを見つけて提出先の指定をクリックしてください" />}}

ポップアップで提出先の指定ウインドウが表示されます。今回は「アルバイトA」さんの提出先を固定すると仮定して設定手順を見ていきましょう。
まずアルバイトAさんの設定ウインドウが表示されたら、

1. Aさんがどの日報テンプレートを使ったときに、
1. 誰あてに提出するのか

この２つをを指定します。

{{<imgproc dist.png "ポップアップで提出先の指定ウィンドウが表示されます。テンプレートごとに指定が可能です" />}}

この製造部では作業点検シートと業務報告書の2種類が登録されていることが上の画像から確認できます。ここで仮に「作業報告書」を書いたときは「管理者宛」に提出先をセットしたい場合は、上のような画像の設定になります。
これで「アルバイトA」さんが「作業報告書」を使って日報を作成するとき、日報の提出先が「管理者」で固定されます。

|名称|説明|
|---|---|
|提出先や共有先の変更を許可しない|ONの場合、日報作成時に提出先や共有先を変更できなくします。OFFの場合は日報作成時に初期値で指定した提出先が選ばれますが、日報提出時に変更することもできます。|
|グループ内の全スタッフを自動で含める|ONの場合、共有先にグループ内の全スタッフが自動でセットされます。OFFの場合は個別に共有先を指定する入力フォームが出現します。|
|設定をクリア|提出先、共有先の情報をリセットします|

## 日報テンプレートごとに提出先を指定する

スタッフ毎に指定するのは設定量が多くて大変ですが、こちらは簡単な方法です。
日報やチェックシートのテンプレートを作成した際、そのテンプレートごとに提出先や共有先を指定できます。

例えば「トラブル報告書を使った場合はZ社長あてとして設定」のように設定ができます。もしスタッフごとの設定で同じテンプレートが設定されていた場合は、スタッフごとの設定が優先されます。
こちらの手順はテンプレート毎に設定される大まかな指定です。

{{<alice pos="right" icon="here">}}
まだテンプレートを作っていない場合は先に[テンプレートの作成](/org/groupsetting/template/make/)を済ませておきましょう
{{</alice>}}

1. グループ設定をクリック
1. テンプレート管理をクリック
1. 提出先を指定したいテンプレートの行にある「提出先の指定」をクリック
1. 設定画面が表示される
1. 提出先や共有先を指定する

{{<imgproc dist2.png "日報やチェックシートのテンプレートごとに提出先や共有先の指定が可能です" />}}

「提出先の指定」をクリックするとポップアップで設定画面が表示されます。
設定画面自体はスタッフごとの指定と似ていますね。テンプレートの選択が無い分、こちらのほうがシンプルです。

{{<imgproc dist3.png "ポップアップで設定画面が表示されます。提出先や共有先を選びます。" />}}

ここで指定された提出先が、日報作成時に自動でセットされる名前となります。

### 実際にロックされる画面のイメージ

さて、実際にロックされた画面はどのように見えるのでしょう？例えば作業点検シートは管理者に提出で編集をロックしたと仮定します。この場合、日報作成時に作業点検シートを選ぶと、
提出先の項目が自動でセットされていることが確認できます。また「提出先や共有先の変更を許可しない」がONの場合はその名の通り、提出先や編集先を変更することができなくなっています。

{{<imgproc lock.png "日報提出先の変更を許可しない場合は、日報作成時に提出先・共有先の変更ができません" />}}

このように予め提出先や共有先を設定しておくことで、スタッフの日報作成時に余分な作業を軽減できます。誤操作や現場の混乱などのリスクも軽減できます

{{<alice pos="right" icon="here">}}
そもそも誰に提出するのかわからない？といった事態も解消できます。
{{</alice>}}

## 提出先の指定設定が無い場合は履歴をもとに自動セット

これまでお伝えしてきたような提出先・共有先の指定がされていない場合は、日報作成者が日報作成時に提出先や共有先を手動で設定します。  
1度目の提出は情報がまったくないため手動で設定する必要がありますが、2度目以降は提出先、共有先の情報がテンプレートごとに記録されます。
最も最後に指定した提出先と共有先が自動でセットされます。この履歴による設定は最も優先度が低く、あとから「テンプレートごとの提出先指定」などが設定されるとそちらが優先されて適用されます。
