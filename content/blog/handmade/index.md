+++
title = "日報のシステムを自作する"
description = ""
tags = ["日報を読む", "日報を書く"]
weight = 10
draft = true
[sitemap]
  changefreq = 'monthly'
  priority = 1.0
+++


{{<alice pos="right" icon="pc">}}
既存の日報アプリだと必要な入力項目が不足していたり、逆に多すぎて使い勝手が悪い。そんな経験は有りませんか？
{{</alice>}}

日報は業務の報告として使用されますが、業務の報告すべき内容は業種はもちろんのこと、同業種であっても会社によって全く異なるケースが多々あります。
そのため多くの企業では日報をワードやエクセルなどでテンプレートを作成し、それを複製して使用することでオリジナルの日報として使用していることと思います。
日報をシステム化する難しさは会社ごとの独自なテンプレートを再現しにくいことにあります。一般的な既製の日報アプリで必要な項目が会社の日報に完全にマッチしていることは極めてまれです。
業務内容が変われば報告内容も当然変わるわけですから、既製の日報アプリだとどうしても使い勝手の悪さが目立ってしまいます。

## 日報のテンプレートを設計する

日報の入力画面がシンプルな四角い箱１つで完結している日報アプリの場合、枠の中にテンプレートを記述することで日報のテンプレートとしています。

<textarea name="example" cols="30" rows="6">
---報告内容---


---引き継ぎ---
</textarea>

