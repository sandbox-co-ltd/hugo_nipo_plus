+++
title = "日報の修正"
draft = false
tags = ["日報テンプレート", "日報を書く"]
weight = 50
+++

作成した日報やチェックシートに不備がある場合はその日報を修正する必要がありますが、NipoPlusはデータの改ざんを防止するために日報の状態が承認・進行の場合は修正できないようにロックが掛かります。

{{<imgproc locked.png "日報にロックが掛かっている場合は修正ボタンが押せなくなっています。この場合は日報の状態が進行のため修正ロックが掛かっています。" />}}

この場合は一度日報を棄却にする必要があります。承認者に対して当該日報を棄却してもらってください。

{{<alice pos="right" icon="please">}}
提出先のスタッフから修正もできるので、軽微な修正であればお願いするのもありですね
{{</alice>}}

## 日報・チェックシートを修正できるスタッフ

NipoPlusでは日報やチェックシートの修正が可能なスタッフは2種類います

- その日報・チェックシートを作成した本人
- その日報・チェックシートの提出先として指定されたスタッフ

それ以外のスタッフは修正することができません。また繰り返しになりますが承認や進行中の日報は、改ざん防止の為修正ができません。新規や棄却の状態で修正する必要があります。

{{<alice pos="right" icon="here">}}
一般的には提出＞棄却＞修正の流れになります。承認されたあとで修正するのはレアケースでしょう
{{</alice>}}

### 自分の書いた日報を修正する

自分の書いた日報は送信BOXに保管されています。送信BOXから修正したい日報を見つけて表示し、修正ボタンをクリックします。

1. 日報保存箱をクリック
1. 送信BOXをクリック
1. 修正したい日報を一覧から選ぶ
1. 日報詳細画面の右側にある修正ボタンをクリック
1. 日報編集画面に遷移
1. 内容を修正して修正ボタンをクリック

まずは日報保存箱をクリックし、送信BOXを開きましょう。一覧で日報やチェックシートが並んでいますので、その中から修正したい日報を選びます。
一般的には修正すべき日報は棄却であることが多いため、棄却（赤色）を目印に探します。

{{<imgproc choice.png "修正したい日報を選択します。ここでは送信BOXから探す手順ですが直接URLを開いてもいいですし、通知エリアからジャンプしても良いです" />}}

{{<alice pos="right" icon="ok">}}
通知エリアの棄却から直接ジャンプしてもOkだよ。どのような方式でもいいから修正したい日報の詳細画面を開ければいいんだ
{{</alice>}}

日報詳細画面に切り替わりました。画面右側に「修正」ボタンがありますのでこのボタンをクリックします。

{{<imgproc edit.png "修正したい日報を選択します。ここでは送信BOXから探す手順ですが直接URLを開いてもいいですし、通知エリアからジャンプしても良いです" />}}

修正ボタンをクリックすると日報の編集画面に切り替わります。

{{<imgproc edit2.png "日報の修正画面に切り替わります" />}}

一見すると日報の作成画面と同じですが、次のような違いがあります。

- タイトルが「日報の作成」から「日報の修正」に変化しています
- 「提出」ボタンが「修正」ボタンに変化しています
- 下書きのチェックボックスが使用できなくなっています

それ以外は通常の日報作成と同じ手順で日報の修正が行なえます。修正時に提出先や共有先の変更もできますが、もとの提出先にとって混乱の元となるため基本的には変更しないことが望ましいです。

### 他のスタッフが書いた日報を修正する

スタッフが書いた日報を提出先に指定されているスタッフが代理で修正することもできます。軽微な誤字脱字程度であればいちいち棄却せずその場で治せるので便利ですが、他人の日報を修正するという行為になりますので修正は慎重に行ってください。
代理の修正も基本的な手順は自分の日報修正と同じです。
修正したい日報やチェックシートを表示させて修正ボタンをクリックして修正を行います。

{{<imgproc edit3.png "日報の提出先似指定されたアカウントから見た画面。承認や棄却の隣に修正ボタンが配置されており、代理で修正できることがわかります" />}}

{{<alice pos="right" icon="ok">}}
些細な違いですが修正ボタンの位置とボタンの形状が少し異なります。
{{</alice>}}

## 修正後の状態について

チェックシートや日報を修正すると状態が「修正」に切り替わります。

{{<imgproc edit4.png "修正された日報やチェックシートは状態が「修正」になります" />}}

もし承認リレーが組まれていた日報やチェックシート出会った場合は、承認リレーがどこまで進んでいても1から振り出しに戻ります。

{{<alice pos="right" icon="default">}}
少しめんどくさく思いますが内容が変わっているんだから仕方ないですね
{{</alice>}}