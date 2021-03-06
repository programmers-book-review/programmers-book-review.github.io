---
layout: post
title: キャパシティプランニング
categories: rank_3
tags: [web]
---


<div class="book"><div class="book_image"><a href="http://www.amazon.co.jp/dp/4873113997"><img src="/images/capacityplanning.jpg"></a></div><div class="book_info">John Allspaw/オライリージャパン</div><div class="clear"></div></div>

キャパシティプランニングという言葉は全く聞いたことがなかった。本を読んで、増加し続けるリソースに対して、いつ新たなシステムを導入すべきかを計画することなのか、と勝手に解釈。 

サブタイトルのHow to Build the Next Flickrは反則だと思う。惹かれてしまうじゃないか。 

基本的には性能のチューニングと同じように、ひたすら計測して、その事実をもとに計画を立て実行するというものだと感じた。この本を読んでもそれが出来るようにはならないけど、自分のように全く知識がない者にとっては雰囲気が分かってちょうど良かった(100ページ程度と薄いのもうれしい)。 

目から鱗というか、フムリと思ったのは、キャパシティプランニングでは、CPUやディスクなどのリソースがなぜそのような状態になっているのか、その原因を探ることはしてはいけないということ(キャパシティプランニングには何の役にも立たないため)。それはあるものとして、プランニングを行う必要がある。(ハードウェア購入のプランニングが終了後パフォーマンスチューニングによりその原因を突き止める)(p.45 「好奇心がキャパシティプランを台無しにする」を読んでの感想) 

以下、自分用メモ

 p.15 アーキテクチャの設計に関する本 「Scalable Internet Architectures」Theo Schlossnagle, Peason (O'ReillyのスケーラブルWebサイトと同じくオススメされていた) 
上の本のプレゼンテーション(pdf版) http://www.omniti.com/~jesus/misc/Scalable%20Ti.pdf 
(slideshare版) http://www.slideshare.net/shiflett/scalable-internet-architectures 

p.120 複数の企業のユースケースから得られたクラウドの検討事項 

非技術的な検討事項: 

* プライバシー、セキュリティ、第三者によるデータ所有に関する法的な懸念 
* クラウドインフラの可用性やパフォーマンスに対する信頼 
* インフラの一部という観点で見たSLA(またはSLAがないこと)の影響 
* いまだ新興である技術プラットフォームに対する安心感のレベル 

 技術的な検討事項: 

* クラウドリソースを最も効率的に使うための、アプリケーションの設計。転送コストをできる限り回避するためのアーキテクチャや、必要な時にだけ計算インスタンスを配置することは、非常に一般的な実践です。 
* データが物理的に存在する場所を感知しません。このため、開発者はアプリケーション(およびアプリケーション管理)をより高水準に考えるようになります。計算インスタンスのインストール、破棄、移行の可能性を予期して、冗長性を取り入れる必要があります。
