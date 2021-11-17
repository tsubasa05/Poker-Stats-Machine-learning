# Poker-Stats-Machine-learning
### 概要
ポーカーのstatsを利用したプレイヤーの実力の判別。試行回数が少ないプレイヤーの実力を機械学習で見極めます。
分類器の手法にはニューラルネットワークを用いたものと、SVMを用いたものの2つのパターンで行っています。
### データ
プレイヤーの実力の定義について、100プレーあたりに平均して稼ぐチップの量を指標としました。この指標はwin rateと名付けます。プレイヤーの平均win rateよりも高いか低いかで、実力判定を行います。このリポジトリには16人の統計情報を、csvファイルとして上げています。
1人プレイヤーのラベリングを行う際、このプレイヤーのラベルを30万回以上のプレーデータによって得られたwin rateに基づいて決定します。そのあと、このプレイヤーのデータを5万プレー毎のデータに分割します。そしてこの5万プレーのデータすべてに、最初に決定したラベルを貼り付けます。5万プレーそれぞれのwin rateは無視します。こうすることで5万回のプレー回数という少ない試行回数による分散の影響に惑わされず、5万回プレーの情報に対して正しいラベル付けを行うことができます。

