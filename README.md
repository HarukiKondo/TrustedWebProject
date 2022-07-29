# TrustedWebProject
TrustedWeb公募に向けたドキュメントやアイディアをまとめるリポジトリです。


### 想定シーケンス図

[![](https://mermaid.ink/img/pako:eNqdlMtu00AUhl9lNCsQ7Qt40Q2wRUggsfHGxANEamxwx0ioqhTPNCEkEUGVmuJKqAmBNtxatRRInQoe5tge-y2YZBLIxbQRXlie4_8_l09Hs45ztkmwhtfIE5dYOXIjbzx0jIJuIfnQPF0lGhKnZ2G_JqrfwTsEtgmsGjWa8n3lruOuUWKie-S-eFG5qkwx6yTFElpeXlm5NrJG9T7SUNTYSbqBEv2NK9lOKfXf_tGEP9-krfORUv0aym7b14H9AHYGvAy8NaMXfj-tnyjXLZsSZD8lzqxHQ8CbwL8A58COgHvADoCfA_9qO1GlHG93htIK8M-DMOuFvSp4n8KgIk43Y16KWsfAtiZLzTY1N7fyyk7D_uvosB4G5bS4K_beX0Bikjl_Pmzkl4Qv_CBp19W0abEjvrUvZbRApkuIocwUbOu_OKq64PnAahfgG-2QrDzUz1ObXrLx9iTdj9F2Y1qRvTfKAl5vwCILUNqsiXdBsu_Fx2wBQON087nS5kmyfxB3P6T-K7kAYe_lInud2dNkN3PYpklk-9tdOdM_AQ74BdHRHtItvIQLxCkYeVNeDesDh47pI1IgOtbkp0keGO4q1bFubUip-9g0KLlp5qntYI06LlnChkvtO8-s3PisNKPbRQU3fgP81W3f)](https://mermaid.live/edit#pako:eNqdlMtu00AUhl9lNCsQ7Qt40Q2wRUggsfHGxANEamxwx0ioqhTPNCEkEUGVmuJKqAmBNtxatRRInQoe5tge-y2YZBLIxbQRXlie4_8_l09Hs45ztkmwhtfIE5dYOXIjbzx0jIJuIfnQPF0lGhKnZ2G_JqrfwTsEtgmsGjWa8n3lruOuUWKie-S-eFG5qkwx6yTFElpeXlm5NrJG9T7SUNTYSbqBEv2NK9lOKfXf_tGEP9-krfORUv0aym7b14H9AHYGvAy8NaMXfj-tnyjXLZsSZD8lzqxHQ8CbwL8A58COgHvADoCfA_9qO1GlHG93htIK8M-DMOuFvSp4n8KgIk43Y16KWsfAtiZLzTY1N7fyyk7D_uvosB4G5bS4K_beX0Bikjl_Pmzkl4Qv_CBp19W0abEjvrUvZbRApkuIocwUbOu_OKq64PnAahfgG-2QrDzUz1ObXrLx9iTdj9F2Y1qRvTfKAl5vwCILUNqsiXdBsu_Fx2wBQON087nS5kmyfxB3P6T-K7kAYe_lInud2dNkN3PYpklk-9tdOdM_AQ74BdHRHtItvIQLxCkYeVNeDesDh47pI1IgOtbkp0keGO4q1bFubUip-9g0KLlp5qntYI06LlnChkvtO8-s3PisNKPbRQU3fgP81W3f)

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
    PoCシステム -->>+ 病院 : 紹介状データの表示
    患者 -->>+ 病院: 診察 
```
