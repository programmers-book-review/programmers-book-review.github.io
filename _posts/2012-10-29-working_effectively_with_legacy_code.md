---
layout: post
title: レガシーコード改善ガイド
categories: rank_3
tags: [プログラマ]
---


<div class="book"><div class="book_image"><a href="http://www.amazon.co.jp/dp/4798116831"><img src="/images/working_effectively_with_legacy_code.jpg"></img></a></div><div class="book_info">Michael C. Feathers/翔泳社</div><div class="clear"></div></div>

テストのないコードをレガシーコードと位置づけ、それを修正する時のリファクタリングテクニックを網羅したような本。テストドリブンが叫ばれていてその重要性を理解しながらも、やはりテストを後で書きたい自分にぴったりと読んでみた。残念ながら(というかそもそもの認識誤りで)、期待した内容ではなかったものの、本に書かれていること自体は大変ためになると思う。

ただし、最近のリフレクションを持っていて動的にクラスを作れるような言語ではモックが作れる。それを使えば、この本に書かれていることの大半は不要になると思う。レガシーな言語が対象ともいえるだろう。原書が出版されたのは2004年なので仕方がない。でも基本となる考え方はためになると思う。

getterとsetterを同じメソッドでは行わない(コマンドとクエリーの分離)など色々とためになることが書かれてきたのだけど、一番グッときたのは、第24章「もうウンザリです。何も改善できません」(p.335)での著者のレガシーコードへの思い。適当に要約してみる。レガシーコードだけが大変なのではない。隣の新規プロジェクトは立場が異なる大変さがある。きれいなコードを受け持ってもがっくり来ているチームもあれば、大変なレガシーコードを抱えても輝いているチームもある。要は気持ちの持ちようだ、

一番違和感を覚えたのは、テストのために可視化の範囲を広げること。本末転倒の気がする。経験上、リファクタリングをする上で断然便りになるのが可視化の範囲だからだ。当時は試験をするためには仕方がなかったのだろうが、現在の言語ではリフレクションなどを使えばいかようにもなる。

読んでいて思ったのは最初からテストしやすいコードを書くことが重要ということ。それにより、依存性などを最小限に抑えられ、個々のクラスやメソッドの責務が明確になるだろう。テストドリブンで行えば初めからそれが叶えられて理想なのだろうけど、(しつこいけど)それをやりたくない自分には、テストをリファクタリングの機会とするのが現実的だと思った。

テストを先に書きたくない理由を挙げてみる。
* 最初に何を作りたいか分からないから、テストを考えられない。
  もちろん、やりたいことは漠然として思っていて、それを明確にするために、テストを通じてAPIを設計していく方針も分かるのだけど、まだそこまでの所までも行っていない。
* どうすればできるか分からない
  まずは何ができるか、どうすればできるか分からないから、そこを解決したい、という気持ちが先にある。そのときは、APIなどは関係なく、気になっている機能だけを実現する。そこに集中する上でAPIは二の次となる。

要は仕様も決まっていなければ、その実現方法も分かっていないので、何をどうやればできるかを見極めながら、仕様(やアーキテクチャ)が決まっていく感じ。大方の人の決まりきったものを作るのとは立場が異なるのだ(という言い訳をしてテストを後に伸ばす)

そして、最後の理由が一番強いのだけど、
* つまらない
これが正直な所。一番おもしろいプログラミングをようやくできるのに、テストなんて書いてられない。これを言ったら今までの言い訳が無に帰るのだけど、そうなのだから仕方がない。人間のための方法論なのに方法論のために人間が合わせるなんてまっぴらなのです。UIに通じる考え方か。

ただし、試験が重要だということは何を言っても変わらない。しかもリーンや継続的デリバリにおいてより重要になっている。個人的には次の順番の開発が良いのではないかと思っている。

1. とにかく作りたいもの動くものを書く
2. それが通るような試験を書く
3. 試験を仕様として、リファクタリングしてきれいなアーキテクチャに直す
仕様が決まっていない開発だからこそできるのかもしれない。試験すら書いていない自分にとっては、大変な進歩のような気がする。今回のプロジェクトでためしてみたい。