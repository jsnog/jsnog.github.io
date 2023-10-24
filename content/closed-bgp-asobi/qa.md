---
title: "Q&A"
weight: 900
---


### Q: ASって何?
Autonomous System 自律システム の略。

ASとは、インターネット上での独立した組織の単位で、インターネットは多数のASを接続してできている。本物のインターネットではISP等に付与されている。例えば、NTTコミュニケーションのOCNはAS4713、オプテージのen光はAS17511、So-netのNuro光などはAS2527などがあげられる。

- [インターネット用語1分解説～ASとは～ - JPNIC](https://www.nic.ad.jp/ja/basics/terms/as.html)
- [AS番号とは｜「分かりそう」で「分からない」でも「分かった」気になれるIT用語辞典](https://wa3.i-3-i.info/word12229.html)
- [自律システムとは？| ASNとは？ | Cloudflare](https://www.cloudflare.com/ja-jp/learning/network-layer/what-is-an-autonomous-system/)

### Q: BGPって何?
Border Gateway Protocolの略。自分のASがどのようなIPアドレス帯への経路を持っているのかを他のASに伝え、他のASからどのようなIPアドレス帯の経路を持っているのか、を教えてもらうためのやり取りの決まり。BGP機器はここでやり取りしたメッセージを元に、IP経路を設定する

AS同士はBGPを用いて接続されている。

- [BGPとは｜「分かりそう」で「分からない」でも「分かった」気になれるIT用語辞典](https://wa3.i-3-i.info/word12234.html)
- [インターネット用語1分解説～BGPとは～ - JPNIC](https://www.nic.ad.jp/ja/basics/terms/bgp.html)

### Q: 「アドレスを広報」とは?
ルータにIPアドレス帯を設定し、BGPで自分のAS番号にはこんなIPアドレス帯がありますよ～と他のASに伝えるようにすること。

### Q: ピアって何?
Peer: 相手

ASの接続先のこと。

### Q: なぜVPNで繋ぐの?
確かにBGPのメッセージをやり取りするだけでは、VPNでトンネルを張る必要性はなく、そのままIP直でもいい気がする。が、BGPでやり取りした後、そこを様々なIPパケットが通ることになり、その際に家のルータなどにブロックされていたりしたらたまらないため、トンネルを張りそこをくぐらせる。

### Q: [Hurricane Electric Free IPv6 Tunnel Broker](https://tunnelbroker.net/) って何?

### Q: フレッツ網内折り返しって何?

### Q: トンネルの張り方について、もう少し詳しく教えて
