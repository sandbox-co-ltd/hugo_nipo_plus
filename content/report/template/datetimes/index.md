+++
title = "期間入力フォーム"
draft = false
tags = ["日報テンプレート"]
weight = 60
+++

{{<imgproc icatch.png Resize "1200x" "期間入力フォームを含んだ日報テンプレートの例" />}}

## 10:00〜15:00のような期間の入力ができる入力フォームです

期間入力フォームは開始時刻と終了時刻を入力できる入力フォームです。入力形式は時刻のみ、日付と時刻、日付から選択できます。
時刻のみの場合はスライダー方式の時刻入力とキーボードによる入力が選べます。日報作成時に切替が可能です。
日付の場合はカレンダーからの入力とキーボードによる入力が選べます。日報作成時に切替が可能です。


{{<imgproc setting.png Resize "1200x" "期間入力フォームの設定画面" />}}


- 表示名
  - グレーの領域に表示されます
- メモ
  - 入力エリアの左上に赤文字で表示されます
- 入力必須
  - これがONの場合、数値が空欄だと日報の提出ができなくなります
- 幅
  - 1〜12の幅を選択できます。表示名との兼ね合いで自由に調整してください。推奨幅は3〜4です
- 形式
  - 日付（西暦あり）・日付（西暦無し）・時刻のみ・日付と時刻の4種類から選択します
- スライダ上の最小
  - 形式が「時刻のみ」の場合に限り表示されます。スライダ式で時刻入力する際のスライダの左端を何時にするか設定します。初期値は8:00です
- スライダ上の最大
  - 形式が「時刻のみ」の場合に限り表示されます。スライダ式で時刻入力する際のスライダの右端を何時にするか設定します。初期値は20:00です
- 刻み
  - 形式が「時刻のみ」の場合に限り表示されます。1目盛りあたり何分進めるか設定します。初期値は30分です


## 期間入力フォームの入力方式について

期間入力フォームにおいて、入力形式を「時刻のみ」とすると入力フォームがスライダ式になります。
スライダ式では宵越しの入力ができないため、この場合はキーボードからの入力フォームに切り替えてください。

{{<imgproc time.png Resize "1200x" "スライダで時刻を入力する際の注意点として日をまたいだ入力ができない。日をまたぐ場合はキーボードで入力する" />}}

可変長入力と期間入力フォームを組み合わせると時刻の入力を自動で補助する機能が発動します。

{{<imgproc autoset.png Resize "1200x" "可変長で時刻を使用する際に限り初期値セットの動きが変わる" />}}


## 日付と時刻の日報を受け取ったときにどのように見えるのか？

以下のように表示されます。

{{<imgproc post.png Resize "1200x" "日付と時刻フォームを含んだ日報を受信した画面イメージ" />}}



## 期間入力フォームの日報をCSVに出力する

期間入力フォームの日報はCSVに出力できます。オプションは有りません。
期間入力は「開始」と「終了」の２列に展開して出力されます。

{{<imgproc csv.png Resize "1200x" "期間入力フォームを含んだ日報をCSVに出力した例" />}}




### サンプルデータ
このページで使用した実際のサンプルをダウンロードできます


{{<attachments style="orange" />}}
