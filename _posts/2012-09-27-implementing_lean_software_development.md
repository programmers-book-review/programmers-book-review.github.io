---
layout: post
title: リーン開発の本質
categories: rank_3
tags: [イノベーション]
---


<div class="book"><div class="book_image"><a href="http://www.amazon.co.jp/dp/482228350X"><img src="/images/implementing_lean_software_development.jpg"></a></div><div class="book_info">Mary Poppendieck等/日経BP社</div><div class="clear"></div></div>

コンセプトからキャッシュにするまでの時間をいかに短くするかというリーンのお話。

p.326、p.293は自分が標準プロセスに対する嫌悪感をまさに端的に表しているように感じた。人を信じずに、方法論のみを押し付け、それに従っているかどうかでのみ判定する環境。重要なのはなぜそれが必要かであり、それが守られるのであれば、その内容は内部での積極的な修正を許すべきである。

プロセスや改善ツールが広がらない原因のひとつにそれがあるのだと思う。なぜ必要とされるかが理解できないから上辺だけを実践するし、効果が出ないから余計邪魔なものになる。理由とその効果(短期間で、少なくてもプロジェクトが終わるまでに出ることが重要)が極めて明白になっていれば、その手段は彼らなりにやるのだと思う。ツールを提供するのであれば、その方法の一つとして提供するぐらいの位置づけだろう。広げる方法が問題ではなく、理由と背景を明確に説明できないプロセスやツール自体が問題なのだと思う。

ソフトウェア開発ではなく自組織にリーンを当てはめたらどうなるのだろうと読みながら思ってたのだけど、次の本「リーンソフトウェア開発と組織改革」というズバリの本があったのでこちらを読もうと思います。

以下、自分用メモ<!--more-->

> グーグルは、検索結果のランキングとよく似た方法で、どの製品に取り組むかを決定している。つまり、優先順位は、開発チームの興味と、製品にひきつけられたユーザー数を基に決定するのだ。(p.56)

> リーン活動に乗り出す前に、「人について、何を本当に信じているか?」という問いに答えなくてはならない。プロセスにどのような態度で取り組んでいるか、考えてみよう。きちんとドキュメント化され、誰もが質問することなく従えるようなプロセスが、正しい道だと考えているだろうか?それとも、プロセスを標準化するのは、その作業をする人に、疑問に思ったり変更したりするための土台を与えるためだろうか? リーン原則は確実に、後者の考えに根ざしているのである。(中略)リーンを成功させるには、作業を行っているその人本人が、その作業のやり方を最もよく知っているのだ、という基本理念を、(中略)問題解決するには、その本当に、作業を行う人たち自身に、トレーニングを行ったり、ツールや権限を与えたり、支援したりして、自らの問題を解決し、プロセスを改善できるようにするのが最善の手法だということを心から信じなくてはならない。(p.326)

> 思考
トヨタの「思考生産システム」の最大の強みは、人の育成方法にある、と言っている。「『プッシュ』(押し付ける)システムでは、作業者たちは与えられた指示に従って、ただ生産していくだけなので、ほとんど知恵を得る機会がない」と彼は言う。「それとは対照的に、『プル』(引き出す)システムでは、何をどのくらいの速さで作るべきか、一人で決定しなくてはならない製造プロセスを、作業者に自分の頭を使って考え出させるのだ」
たいていの改善活動では、ドキュメントを必要以上に重視しすぎていて、各人に常に自分の作業環境の改善方法を考えさせることに、あまり重点を置いていない。もちろん、ほとんどの企業では、社員に十分に、改善について考えさせている、と思っている。私たち自身、何年も前からいいアイデアがあればそれを書き留めて提出できる提案システムを作業者に用意しているが、その提案活動も改善という点から見れば、ほとんど効果はなかった。ソフトウェア開発では、ふりかえりを使って変更すべき点を書き出したりするが、同じ内容が何度も繰り返しできてくることがあまりに多いようだ。
困ったことに、提案活動やブレインストーミングで出されたアイデアの多くは、誰か別の人に引き継がれて、評価されたり、ときには実現されたりする。これは間違ったやり方だ。アイデアを持っているチームメンバー自身が、自らのアイデアを実現すべきなのである。他の人が実現することを前提に、提案システムにアイデアを出させても意味はないのだ。
優秀なアイデアの長いリストに、自分のアイデアをただ付け足しているだけではダメなのだ。改善に関する優れたアイデアが、誰か別の人の問題として手渡されてしまったら、発案者はそのアイデアを自分で推し進めようとはしなくなる。そして、その問題についての暗黙知もまた、発案者の頭の中に残されてしまう。
すべての作業者が自分たちの現在行っているプロセスのしくみに、常に疑問を感じるべきであり、新しいアイデアを試したり、うまくいくアイデアを実現したりするために、効果的な問題解決テクニックを積極的に使うように奨励されなくてはならない。この問題解決プロセスの基盤として、ドキュメントが存在すべきである。このドキュメントは、作業チームが作って、使い、保守し、手軽に変更できるようでなければならない。
やる気と思考力のある人材に価値があると考えるのなら、ドキュメントに基づいたプロセス評価を見直す必要がある。通常、そのような評価は、組織が、ドキュメント化された手続きに従っているかどうかで、その組織の成熟度を測る。一見、この目的は無害に見えるが、実際には、評価プロセスは組織にドキュメントを凍結するように強いるのが常なので、そのプロセスを変えさせまいとする圧力もかかっているのだ。その結果、困ったことに、ともすると第一線の作業者たちから「考える権利」を奪ってしまう。作業者は、ドキュメントに書かれているとおりにやるように、と促される。しかし、本当は、ドキュメントに書かれている内容に、常に疑問を持つように促されるべきなのである。ドキュメント重視のプロセス評価は、ドキュメントの安定性を重視しがちだ。実際には、ドキュメントの頻繁な変更こそが、その組織が思考できるようになった証拠だと考えるべきなのだ。(p.293)

> 計測
開発チームを効果的に計測する方法を見つけるのは難しいものである。なぜなら、開発作業が終了してからしばらくたたないと、その成果が目に見えない場合が多いからだ。そのため、プロセスの各部分が最適化されれば、プロセスの成果物も最適化されるという前提から、計測を増殖させることになる。この前提は、「システム」としてのものの見方からすれば、根本的に間違っている。まったく制御不能なプロセスをスタート地点とするのであれば、プロセスを部分ごとに最適化していっても利益はあるが、結局は部分最適化によって、システム全体の最適化を妨害することになるのである。
誤った計測を改善しようとしても、間違った要因を作り出すことになり、多くの場合は意図しなかった結果につながる。たとえば、プロジェクトマネジャーはよく、アーンド・バリューに基づいて計測される。しかし、アーンド・バリューを計測すれば、計画どおりに進めたかどうかを計測することになる。つまり、その計画が望まれた結果を達成するための方法であったかどうかという点は、まったく無視されてしまう。これが、予定どおり、予算内で、計画どおりのスコープを完成させた形でソフトウェアを提供しても、やはり顧客に不満を抱かせる原因なのだ。
では、正しい行いを促すためには、どのような計測基準を採用すればいいのだろうか?計測点を増殖させるのではなく、計測対象を減らし、サブシステムレベルでの正しい行いを促すようなシステムレベルでの計測点を見つけるのがいいのだろう。リーンな組織では、何を計測すればよいかがすでによくわかっているはずだ。つまり、サイクルタイム、財務上の成果、顧客満足度である。(p.294)

> リーンソフトウェア開発の7つの原則とそれを妨げる神話

> 原則1: ムダをなくす(Elimnate Waste)
  神話: 早く仕様を固めればムダが減る → 使われることのない機能は最悪のムダ

> 原則2: 品質を作り込む(Build Quality In)
  神話: テストの役目は欠陥の発見だ → 欠陥を防ぐこと(人間だから起きるポカよけ)

> 原則3: 知識を作り出す(Create Knowledge)
  神話: 予測が予測可能を生む → 未来予測は、複雑、詳細、遠い未来、不確実な環境では必ず不正確

> 原則4: 決定を遅らせる(Defer Commitment)
  神話: 計画は決定である → 計画は役に立たないが、不可欠なプロセスであり、重要な学習訓練

> 原則5: 速く提供する(Deliver Fast)
  神話: 急がば回れ → Googleのように品質、速度が両立し得る。そのためには、プロセスの継続的改善、品質を作り込む人を育て、競合他社の何倍ものスピードで繰り返し、確実に顧客の要求に反応する能力を培う

> 原則6: 人を尊重する(Respect People)
  神話: 唯一最高のやり方がある → 改善の余地のないプロセスはない

> 原則7: 全体を最適化する(Optimize the Whole)
  神話: 分解によって最適化する → サブシステムのメトリクスは部分最適に陥るため、本当に重要なひとつだけ最適化する
(p.28以降を適当に抜粋)

> リーン開発を実践するための21ステップ(p.301)

> 全体を最適化する
> 1. バリューストリーム全体、製品全体を通してリーン手法を実践する。
2. 計測基準を作り直す。
3. 境界越えのコストを減らす。

> 人を尊重する
4. チームリーダーや監督者を訓練する。
5. 責任や意思決定をできるだけ下のレベルに移譲する。
6. 技術へのプライドを育てる。

> 速く提供する
7. 小さなバッチで作業を進める。
8. 作業を許容量までに制限する。
9. 利用率ではなく、サイクルタイムを重視する。

> 決定を遅らせる
10. 完全に仕様を決定してから開発に着手するのがよい方法である、という考えは捨てる。
11. 依存性を断ち切る。
12 選択肢を持ちつづける。

> 知識を作り出す
13. 設計・構築チームを作る。
14. 継続的な改善を行う文化を守る。
15. 問題解決手法を教える。

> 品質を作り込む
16. 同期する。
17. 自動化する。
18. リファクタリングする。

> ムダを排除する
19. マーケティングと技術の両方を理解しているリーダーを任命する。
20. 価値のみを生み出す。
21. コードをできるだけ書かない。

