---
layout: post
title: アルゴリズムデザイン
categories: rank_5
tags: [プログラマ]
---


<div class="book"><div class="book_image"><a href="http://www.amazon.co.jp/dp/4320122178"><img src="/images/alghorithm_design.jpg"></a></div><div class="book_info">Jon Kleinberg, Eva Tardos/共立出版</div><div class="clear"></div></div>

Collective Intelligence以上に良い今年一番の本。 

計算量理論(complexity theory)は、計算機がどこまで賢くなれるかという限界を示す一つの考え方だと思う。不完全性定理の方は熱中したけどこちらはそれほど興味はなかった。それでも、不完全性定理と計算停止問題のアナロジーからそれらは密接に関係しているのではないか。と、知ったようなことを言う。 
というより、ふと思ったのだけど計算停止問題と不完全性定理は同じことではないか。不完全性定理は論理体系の上に“証明する”ということを形式化して、その上で証明出来ない論理式があることを証明したのだけど、計算停止問題も“計算する”ということを形式化していたのだとしたら同じ気がする。証明も対角線論法だった気がするし。うろ覚えだ。多分、学部時代に読んだ教科書がそこら辺(“計算する”ことを形式化する)を適当に書いていたのだろうと、勝手に人のせいにすることにした。 

まあとにかく、NPなどの意味で現在の計算機で解くのが難しい問題について知ることは教養として重要だと思った次第。 

amazonで値段も見ずに買ったので値段(15,000円)にビビった。1 click恐るべし。さらに到着後、でかさと分厚さにビビった(B5で800ページ!)。持ち運べる大きさではないので、読み始めるのに時間がかかったのだけど、会社の金で同じ本を買った人がいたのでコピーさせてもらってそれを持ち歩いて読んだ。ラッキー。と言いながらもあまりの厚さに恐れをなして、興味のあるNPとかが書いてある8章から読み始めた。 

衝動買いしたのは序文の解説に共感したため。ぜひ、読んでほしいし、そして確かにその序文にふさわしい内容だった。下のURLでもその雰囲気が分かるし、今なら“アリゴリズムデザイン 序文”でGoogleすると訳者の一人がアップロードしているpdfが検索結果として出る。 
http://www.kyoritsu-pub.co.jp/shinkan/shin0807_03.html 

内容的には序文にも書いてあるけど学部や大学院向けに広く使えると思う。 

この本は教科書として素晴らしい。分かりづらい抽象的な文章の後には的確な例や図が載っていて理解を助けてくれる。例えば、NPの定義がこんなにシンプルに書かれた定義は見たことがなかった。分厚い本は難しいと思いがちだけど、経験的にそんなことはなくむしろ逆だと言える決定的な本だと感じた。単にアルゴリズムの羅列ではなく、なぜ、いかにこのアルゴリズムにたどり着いたかの過程が書いてあるので、もっとも大切な考え方が読むだけで得ることが出来る。読んでいるだけで自分が賢くなった気になれる幸せを感じれる本だ。 

そして、良く疑問に思う“こんなの知って何になるの?”という疑問を積極的に解消してくれる。うれしい。例えば、ゲームを考えたとき、このゲームの攻略方法がNPであることを証明させ簡単な攻略方法がないこと、すなわちすぐ飽きることはないという演習問題が出ていたり。そのゲームの説明文の具体的な記述も優れいている。そういえば、かなり前にテトリス(ぷよぷよ?)がNPだとかWebで見たような。 

知ってうれしかったことは、NP完全の一つナップザック問題が、εを与えると最適解の1/(1+ε)倍の答えを出すアルゴリズムがＯ(n^3/ε)で与えられること。これは、計算時間と精度を交換可能であることを表している。ただし、精度を10倍高めようとすると計算時間も10倍かかる。Pが多項式時間で解ける問題、NPが指数時間をかければ解ける(e.g. 2^nの総当たりで調べる)問題の良い橋渡しだと感じた。ナップザック問題(正確にはナップザックの決定問題)はNP完全なので全てのNPはこの方法が適用できる(変換に多項式時間かかるけど、精度と計算時間の関係は適用できるはず)。 

他にうれしかったこと。局所解を見つける方法として、Z=Σexp(-E(S)/kT)というGibbsの方程式を用いて、温度Tを徐々に低くしながらエネルギーを変化させ、その状態遷移の確率に利用する方法がある。この方法は直感的にわかりやすいのだけど、今までなぜTを下げていけば、より良い局所解に達するかが分からなかった。それを、ズバリ、そんな保証はないと言い切ってくれた文章を読んでとてもうれしかった(c.f. p.611のメモ) 

そして、13章のランダム性を用いたアルゴリズムの強力さに驚いた。大雑把に言えば、最悪の状況を避けるためにランダム性を利用することで良い性能を確率的に保証するのだと感じた。わかりやすい例で言えば、既にソート済みのデータに対してクイックソートを適用するとき、ピボットを先頭に選べばO(n^2)になるが、これをランダムに選ぶことでO(n logn)になる(実際は前者のアルゴリズムでも平均O(n logn)になるので適切な例ではないけれど)。他には、ハッシュ関数 h(x)をΣa_i x_i mod pで表現する。ここで、x_iはxのnビット表現の(x0, x1, ..., xn-1)の要素であり、pはnに近い素数、a_iは{0, 1}からランダムで選んだビット列。これにより、任意のu, vに対してh(u)=h(v)の確率が1/nというハッシュ関数に重要な性質が得られる。また、この証明が気持ちよい。(ただし、実際はより工夫されたO(1)回だけの算術演算でハッシュ関数値を計算する他の普遍ハッシュ関数が利用されているとのこと。cf. p.684) 

NP-SPACEの問題解決空間がNP完全より大きい(と考えられている)ことを考えると、現在は計算時間を短くするために富豪的にメモリをに使っているけど、将来的に量子コンピューティングが実用化され非決定性問題がバシバシ解けるようになると、メモリよりも計算時間を富豪的に使う日が来たりするかもという夢を見たり。こんなことを考えられるきっかけを与えてくれる本に感謝します。 

ところで、P=NPなのだけど、ここまでカシコイ人達がかかって解けない問題なのだから、連続体仮説のように仮説やその否定のどちらを公理として受け入れても無矛盾な体系が作れる、とか言う玉虫色(?)の決着を見るのではないか、とこれまた勝手に夢を見る(と思って、“P=NP 連続体仮説”でGoogleしてみるとP=NPが証明されたとか言う変なおっさんが騒いでいるのが見つかって、これと同じ思考回路なのかと思ってゲンナリ)。 

ふと、思ったのだけど、これらの内容のうちどれだけのことを知っているべきなのだろう。プログラマとしては、直接役立つものではないけど、教養として知っておくべきものだと思う。その程度は人によって違うだろうけど、ここら辺を無視する人には大したコードは書けない気がする。 

以下、自分用メモ。NPやNP完全の定義をすぐ忘れるので。<!--more--> 

* Y ≦ X: Xが多項式時間で解ければXも多項式時間で解ける。 
* P: 多項式計算時間で解ける問題の集合。 
* NP: 証明が与えられた時に、多項式時間でそれを確認できるもの。例えば、SAT(下参照)の場合、変数の環境を実際に論理式に代入することで論理式の真偽が多項式時間で確認できるのでNP。 
* P=NP問題: P ⊆ NPは証明されるが、P ⊂ NPは証明されていない。 
* NP完全: 全てのNPのYにおいてY ≦ Xが成り立つX(すなわち、NPに属するすべての問題がXに多項式時間帰着可能)。 
* NP完全の例: 充足可能性問題(Satisfiability Problem:SAT)。論理式を真にする変数の環境を求める問題。 
* PSPACE: 多項式領域で解ける問題。2^nの状態がn bitで表現出来ることから類推されるように、NPより大きい範囲の問題を解くことができると考えられている。NP ⊆ PSPACEは証明されるが、NP ⊂ PSPACEは証明されていない。 

以下、序文より抜粋。 

> 本書では，様々な応用で生じる計算が必要となる問題に対して，まずその問題を定式化することから始めて，複数あるアルゴリズム設計技法からどの技法を用いるべきかをきちんと判断できる力を確立し，そして最終的にこれらの問題に対する効率的な解法を構築する，ということがアルゴリズムを設計するプロセス（過程）であるという立場をとって，アルゴリズムにアプローチしていく．情報科学におけるアルゴリズム的な考え方の役割を幅広く探求していき，これらの考え方を，アルゴリズムを設計し解析できるように正確に定式化された問題に関連づけていく．言い換えれば，これらの問題の動機付けとなっている潜在的な問題点とは何なのか，そしてそれらを定式化する特定の方法はどのようにすれば選べるのか，あるいは，さまざまな状況においてどの設計原理を適用すれば適切なのか，というようなことを解決していくのである． 
このようなことを考慮して，本書の目標は，計算を伴う様々な分野から生じる複雑な形式をした問題からアルゴリズム的な問題の明快な定式化を発見する方法と，その定式化に基づいて実際の問題に対する効率的なアルゴリズムを設計する方法に関する助言を提供することであると言える．さらに，洗練されたアルゴリズムを理解するには，誤った出発点や袋小路も含めて，単純な最初のアプローチから，最終的な解に至るまでの一連のアイディアを再構築するのが最も良いということもしばしば経験されている．したがって，本書のアルゴリズム記述の形式は，必ずしも問題の記述からアルゴリズムへ至る最短の道になっていないことも多い．著者らは同僚とともに，これらの点について一生懸命熟考した結果，特定のある問題に対してはこのやり方がより良いものであると確信している． 

> 物理システムでは、アニーリングにより、エネルギー最小の状態に到達すると信じられているが、シミュレーテッドアニーリング法で最適解が得られるという保証はない。それを理解するために、例えば、図12.2の二重漏斗(勝手な注 複数の穴が開いているポテンシャル)を考えてみよう。二つの漏斗の断面積が同じならば、高温では、本質的に、システムはどちらの漏斗にも等確率でいることになる。温度が下げられるにつれて、二つの漏斗の一方から他方への移動はますます困難になっていく。したがって、アニーリングの最後に、より低い方の漏斗の底にいるという保証はできそうもない。(p.611)
