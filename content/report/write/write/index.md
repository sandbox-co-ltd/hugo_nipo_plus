+++
title = "日報を書くまでの流れ"
draft = false
tags = ["日報テンプレート", "日報を書く"]
weight = 10
+++


日報やチェックシートを書く大まかな流れは次のとおりです。

1. 日報作成をクリック
1. 使用する日報テンプレートの選択（複数ある場合）
1. テンプレートに沿って内容を記入
1. 提出先や提出日などの情報をセット
1. 提出ボタンをクリック

詳しく見ていきましょう。

## 使用するテンプレートを選ぶ

使用するテンプレートを選びます。テンプレートには日報や報告書・点検チェックシートなど色々なものがあるはずです。使用したいテンプレートを選んでください。
一覧にテンプレートがない場合はグループの管理者に伝えて[テンプレートを作って](/org/groupsetting/template/make/)もらいましょう。

{{<imgproc choice.png "「日報作成」をクリックするとテンプレートの選択画面が表示されます。（テンプレートが1種類しかない場合はこの画面は省略されます）" />}}

日報テンプレートは**テンプレート名の順**に並びます。頻繁に使用されるテンプレートは _や . などを名前の前につけることで上位に表示させることが可能です。
またテンプレートにはタグを付けることで見つけやすくしたり、テンプレート名から絞り込み検索を行うこともできます。

{{<alice pos="right" icon="here">}}
日報テンプレートが1種類しか登録されていない場合は直接日報作成画面へ切り替わります
{{</alice>}}

## 日報・チェックシートを書く

使用するテンプレートを選ぶと日報・チェックシートの入力画面に切り替わります。選んだテンプレートによって日報やチェックシート・報告書など名称が色々変わりますが本質的には同じものです。
スマートフォンから日報を書く場合と、タブレット・PCから書く場合では見た目が大きく変わりますが、入力すべき項目は同じです。

{{<imgproc write.png "選んだテンプレートをもとに日報画面が表示。左はiPad・右はiPhoneで開いた例。見た目が違いますが項目は同じであることが確認できます。必要事項を記入して日報を書き上げます" />}}

日報作成は大きく分けて3つのセクションに分離できます。

|エリア|説明|
|---|---|
|日報作成エリア|選択したテンプレートをもとに表示される入力エリアです。スマートフォンでは縦1列に表示されます。タブレット以上の画面では[テンプレート作成時](/org/groupsetting/template/make/)の設計どおりのレイアウトで表示されます。|
|タグエリア|日報のすぐ下に表示されている色とりどりなボタンの集まりです。クリックするとその日報にタグを付けることができます。タグは検索や目印として使用します。日報作成後でも付け外しが簡単に行なえます。|
|ヘッダーエリア|日報の日付や提出先、共有先、下書きなどの情報を設定します|

### まずは日報・チェックシートの本文を書き上げよう

テンプレートに沿って必要事項を記入していきます。[入力フォームの種類](/org/groupsetting/template/)によっては入力方式を切り替えることができるものもあります。お好みの方法で入力方式を切り替えてみてください。
今書いている日報やチェックシートに対してタグを付けることも可能です。これは日報を読む側にとっての目印になる他、タグによる絞り込み検索なども可能です。タグは1度クリックするとセットされ、もう一度クリックすると解除されます。
タグは日報を読む側でも読みながら付けたり外したりできます。付箋のようなものとお考えください。

{{<imgproc write2.png "テンプレートに添って報告内容を書き上げていきます。項目によっては入力方式の切替が可能なものもあります" />}}

今回の例では出てきませんが、テンプレートの設計によっては入力必須が指定されているものもあります。入力必須の項目は空欄だと提出できませんので注意してください。

### 提出先や日付を調整しよう

さて日報本体が終わったら続いて日報のヘッダー情報を確認しましょう。
ヘッダー情報とは提出日や提出先、共有先を設定する箇所のことです。下書きのON/OFFもヘッダー情報に含まれます。

{{<imgproc header.png "ヘッダー情報の設定を行います。" />}}

|エリア|説明|
|---|---|
|提出日|自動で本日の現在時刻が入ります。昨日の報告が時間の関係で作成できなかった場合は手動で調整してください。この日付は日報の集計やカレンダー上の表示に影響します。この日付とは他にシステム上本当に提出された時刻もありますがシステム時刻は変更できません。|
|提出先|日報の提出先です。提出先に指定されたスタッフはその日報を承認・棄却できます。提出先は複数名指定でき、その場合は指定された順に承認のリレーが行われます。|
|他に日報を読める人（共有先）|承認はできませんがこの日報を読める人を指定します。複数名指定可能です。提出先に指定している場合はあえて共有先に指定する必要はありません。|

提出先や共有先は管理者が指定している場合もあります。[管理者が提出先を指定](/org/groupsetting/dist/)している場合は提出先や共有先は指定されたスタッフが自動でセットされます。  
指定がない場合は、過去に同じテンプレートを使って書かれた日報の提出先・共有先をそのまま自動でセットされます。もし過去の提出先情報もない場合は空欄となります。

{{<alice pos="right" icon="here">}}
つまり提出先や共有先が空欄になるケースは「提出指定がない」かつ「初めて使った日報テンプレート」の場合だけです。
{{</alice>}}

提出先や共有先については少しイメージがつかみにくいかもしれません。[日報の提出先](/report/write/dist/)ページでより詳しく解説していますので参照してください。
最後に**提出**ボタンをクリックして完了です。これで日報が作成され、NipoPlusのサーバ上に保管されました。
提出先に指定されたアカウントに対して[通知が発行](/notice/)されるので、あとは読んでもらうのを待つだけです。

{{<alice pos="right" icon="ok">}}
お疲れでした。これで日報が提出できました
{{</alice>}}

### 提出後のアクション

無事に日報が提出されると次のアクションを選ぶ画面が表示されます。

{{<imgproc posted.png "日報提出後に次の操作を選ぶ画面が表示されます" />}}

|エリア|説明|
|---|---|
|続けて書く|同じテンプレートを使用して日報を新規作成します|
|テンプレートを変更|テンプレート選択画面に切り替わります|
|提出した日報表示|先程提出した日報を表示します(送信BOXへ移動)|

この時点で日報の提出は完了しているので、それ以上作業をしないのであればこのままアプリを閉じてしまっても問題有りません。続けて書きたい場合や作成した日報を確認したい場合はそれぞれのボタンをクリックしてください。
メール送信ボタンはクリックするとお使いのメールソフトが起動します。宛先には提出先アカウントのメールアドレスが自動でセットされ、本文には先程提出した日報へのリンクURLが自動でセットされます。
通知は発行されますがそれとは別に、例えば緊急連絡で急いで読んでほしい場合などはメール送信も併用すると良いでしょう。
メール送信はご利用者様の端末で登録されているメールソフトを使用して送信します。
もしG-mailを使用していて、本文や宛先が空欄になってしまう場合はソフトウェアの許可がされていない可能性があります。詳しくは[こちらの手順](https://support.google.com/a/users/answer/9308783?hl=ja)に従って許可をしてください。主に手順7・手順8・手順9を設定すれば動くようになります。

## 【補足】リカバリーについて

記入中のデータは常に自動でPC本体に自動でバックアップがとられます。そのため万が一記入中にフリーズしてしまった場合でも入力したデータが失われる事はありません。

{{<imgproc recover.png "記入途中のデータが検知されると復元確認のメッセージが表示されます。" />}}

書きかけの自動バックアップデータは日報が提出された時点でクリアされます。
