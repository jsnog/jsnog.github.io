---
title: "概要"
weight: 10
---

JSNOGでは[IHANET](https://www.ihanet.info/)や[DN42](https://dn42.eu/)に代表されるインターネットで使用される技術であるBGPによる経路交換を、VPNでの閉域網で実験する場、平たく言うと インターネットごっこをする場 を提供しています

## 閉域網BGP遊びとは?

間瀬BBがJSNOG-LT-1で初心者向けに発表した資料があります

<iframe class="speakerdeck-iframe" src="https://speakerdeck.com/player/678d846f086c40e2b56475405630bda6?slide=3" title="#閉域網プライベートas運用 の人たちは一体何をしているのか?" allowfullscreen="true" frameborder="0"></iframe>

BGPをやるためには、広報するアドレスとAS番号が必要になります。本物のインターネットではJPNICやARINなどといった資源管理団体が管理している グローバルIPv4/v6のアドレス帯、AS番号ですが、インターネットごっこをやるためにJSNOGではプライベート領域からAS番号、IPv4/v6帯を割り当て、それをBGPで広報していただきます。

## 必要なもの
- **トンネルが張れるBGPルーター**
  - ソフトウェアルータのVyOSを用いたり
  - UbuntuにFRRoutingを入れたり
  - もちろん適当なハードウェアルータでも
- **インターネット**
  - トンネルを張るため、IPができるだけ変動しないほうが好ましい
    - [Hurricane Electric Free IPv6 Tunnel Broker](https://tunnelbroker.net/)などでタダIPv6プレフィックスを取得してそこから固定するもよし
    - クラウドのVPSなどに乗せてもよい
  - フレッツ-フレッツの場合、網内折り返しが使えて低遅延でスループットもよい
- **技術力**
  - VPNﾁｮｯﾄﾜｶﾙぐらい

## 参加方法

1. JSNOG Discordの **#閉域網プライベートas運用 チャンネルで「AS番号とアドレスください～」的なことを言います**
2. 担当者が発行するまで待っていてください
3. 発行完了後、#閉域網プライベートas運用 チャンネルで **「ピアを張りたいです～」的なことを言います**
4. **反応してくれた人とVPNを張るために、接続情報を交換します。** VPNで接続が完了し次第、BGPでピアを張り、接続完了です。
5. これ(ピアリング)を繰り返し、*インターネット2*を手に入れよう！

## 留意事項

- **適当にやりましょう**
- 基本的に学生のみでの運用です
- 基本的に公開の場でピアを張り合ってください(VPN接続の資格情報などの機密情報などは外でやり取りしてください)
- 資源が発行されたからと言って直ぐに活動を開始しなければいけないという訳ではありません

## 資源割り当て範囲

- AS番号は`65000-65535`から順番に割り当て
- IPv4アドレス帯は`172.29.0.0/16`から基本/27で順番に割り当て
- IPv6アドレス帯は`fd17:2290::/32`から基本/56でランダムに割り当て

## 資源割り当て状況 / 把握している接続先

 <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTtEyxTIZqKzPRuJoP8pGsugpoU8Aqh-gGrUK_3qPlQPy1vDwf_spAJQaD9t-RoUr4tbC3o68HKNoht/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

## 乗っかっているサービス
何もない...
