+++
title = "タスクと日報を紐付けする"
# description = "チャプター"
tags = ["タスク", "日報を書く"]
weight = 30
+++

タスクが作成された時点では、そのタスクはまだ着工されていないため予定です。  
時が進みタスクが完了したときその結果を日報として報告します。
日報とタスクを紐付けすることで日報を受け取るスタッフから見ると、「タスク（予定）」と「日報（実績）」の対比をしながら確認できます。
紐付けするには、タスクを表示してから日報を書くという手順を踏みます。

1. タスクを詳細表示する
1. 右パネルから日報テンプレートを選択する
1. 日報を通常通りに作成する

{{<imgproc select.png "タスク詳細画面から報告する日報のテンプレートを選択する" />}}

テンプレートを選択すると選択したテンプレートを元にした日報作成画面へ切り替わります。このとき日報作成画面上には**この日報はタスクの報告として紐づきます**という説明バナーが表示されています。

{{<imgproc write.png "タスク詳細画面から日報作成画面へ切り替わります。" />}}

これで日報とタスクは紐付いた状態になりました。あとは通常通りに[日報を作成](/report/write/write/)してください。保存する際に自動でタスクと日報の紐づきが記録されます。

{{<alice pos="right" icon="here">}}
日報の画面自体は通常の日報と全くおなじです。違いは紺色の説明バナーだけです
{{</alice>}}

## タスクと日報の紐づきを確認する

日報とタスクはいわゆる**相互リンク**された状態になります。例えばタスクを表示してみると、そのタスクと紐付けされた日報が下部に表示されています。
{{<imgproc tasktoreport.png "タスク詳細画面下部には紐付けがされた日報が表示される" />}}

この日報へのリンクをクリックするとその日報がポップアップで表示されます。  

{{<alice pos="right" icon="here">}}
カレンダーから見ると、タスクのポップアップー＞日報のポップアップと少し画面がにぎやかになります
{{</alice>}}

タスクから見た日報は一対多の関係になります。１つのタスクに対して、複数の日報を書くことができます。複数の日報が書かれた場合はタスク詳細画面から見た日報へのリンクがその数だけ増えます。

{{<imgproc onetoany.png "タスクと日報は常に一対多の関係にあります。タスクに複数の日報が紐付けられるとその数だけ日報が一覧に追加されます" />}}

逆に、日報から見たタスクは常に1つです。図で表現すると次のような相関図になります。

{{<mermaid align="center">}}
graph LR;
  タスクA --> 日報A
  タスクA --> 日報B
  タスクA --> 日報C
{{< /mermaid >}}


{{<alice pos="right" icon="default">}}
日報の表示画面からタスクを確認する機能については現在実装されておりませんが将来的に実装される予定です
{{</alice>}}
