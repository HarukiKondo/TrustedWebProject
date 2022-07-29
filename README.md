# TrustedWebProject
TrustedWeb公募に向けたドキュメントやアイディアをまとめるリポジトリです。


### 想定シーケンス図

[![](https://mermaid.ink/img/pako:eNqdlM1u00AUhV9lNCsQ7Qt40Q2wRUggdeONiacQKbHBGSOhqlI804SQRARVaoqRUBNS2vDXqqVA6lTwMNf22G_BJHYgTUwb4YVljc-5P5-OZh3nTJ1gBZfIE5sYOXIrrz20tKJqIPnQPC0QBYnTM3_YEPXv4BwC2wRWD1pt-b5237JLlOholTwQL2rXE1PIelG5gpaXV1ZupNagOUQKClo7Ud9LRH_PE9lOJXbf_dH4P9_GnfNUmfway-6aN4H9AHYGvAq8M6MX7jBuniSuOyYlyHxKrFmPgoC3gX8BzoEdAXeAHQA_B_7VtIJaNdzujaU14J9Hx2zgD-rgfPK9mjjdDHkl6BwD25puNTvU3N6JV07qD18Hh03fq8blN2L3_SUkppnz5-NBfkn4wvWibjPZNi73xLfulYwWqHQFMZRZgm39F8ekLzgusMYl-NIMyc5j_Ty1iyGbpCfqfwy2WxcV2blJLOAMRiyyAMXthtjzon0nPGYLAJqUm68Vt0-i_YOw_yF2X8kA-IOXi-Q6c6bpabJTNwGRbe_25Ur_5DfC5wVHu0g18BIuEquo5XV5M6yPHCqmj0iRqFiRnzpZ0-wCVbFqbEip_VjXKLmt56lpYWVNK5TIEtZsat57ZuSwQi2bTETp7ZKqNn4DlJ5uSA)](https://mermaid.live/edit#pako:eNqdlM1u00AUhV9lNCsQ7Qt40Q2wRUggdeONiacQKbHBGSOhqlI804SQRARVaoqRUBNS2vDXqqVA6lTwMNf22G_BJHYgTUwb4YVljc-5P5-OZh3nTJ1gBZfIE5sYOXIrrz20tKJqIPnQPC0QBYnTM3_YEPXv4BwC2wRWD1pt-b5237JLlOholTwQL2rXE1PIelG5gpaXV1ZupNagOUQKClo7Ud9LRH_PE9lOJXbf_dH4P9_GnfNUmfway-6aN4H9AHYGvAq8M6MX7jBuniSuOyYlyHxKrFmPgoC3gX8BzoEdAXeAHQA_B_7VtIJaNdzujaU14J9Hx2zgD-rgfPK9mjjdDHkl6BwD25puNTvU3N6JV07qD18Hh03fq8blN2L3_SUkppnz5-NBfkn4wvWibjPZNi73xLfulYwWqHQFMZRZgm39F8ekLzgusMYl-NIMyc5j_Ty1iyGbpCfqfwy2WxcV2blJLOAMRiyyAMXthtjzon0nPGYLAJqUm68Vt0-i_YOw_yF2X8kA-IOXi-Q6c6bpabJTNwGRbe_25Ur_5DfC5wVHu0g18BIuEquo5XV5M6yPHCqmj0iRqFiRnzpZ0-wCVbFqbEip_VjXKLmt56lpYWVNK5TIEtZsat57ZuSwQi2bTETp7ZKqNn4DlJ5uSA)

```
sequenceDiagram
    title: 紹介状のやり取り(Trusted Web版)
    患者 -->>+ 紹介医 : 受診
    紹介医 ->>+ 病院 : 受診依頼
    病院 ->>+ PoCシステム : 受診依頼登録
    Note over PoCシステム: ブロックチェーンor分散ストレージ上に予約情報を登録
    PoCシステム ->>+ 紹介医 : 予約受付完了通知
    紹介医 ->>+ 病院: 紹介状データの発行依頼連絡
    病院 ->>+ PoCシステム: 紹介状データの発行依頼
    Note over PoCシステム : 紹介状データをブロックチェーンor分散ストレージ上に発行する
    PoCシステム ->>+ 患者 : 発行完了通知
    患者 -->>+ 病院 : 訪問
    患者 ->>+ PoCシステム : 病院への紹介状データの開示要求
    Note over PoCシステム : 病院へ紹介状データ閲覧権限付与
    病院 ->>+ PoCシステム : 紹介状データの要求
    PoCシステム ->>+ 病院 : 紹介状データの表示
    患者 -->>+ 病院: 診察 
```
