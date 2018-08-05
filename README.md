# 二分木の演習

# 進め方
## はじめてのとき
* [GitHub](https://github.com/)のアカウントを作成してください
* [Travis CI](https://travis-ci.org/) のアカウントを作成してください
* GitHubのアカウントを[こちらのフォーム](https://goo.gl/forms/anAdoxqPKVt8sJGZ2)から教えてください。
## 毎回の進め方
* このリポジトリをforkしてください
* Travis CI を設定して、自動ビルドが通るようにしてください
   * Travis CI のGitHubアカウントでの登録とforkしたリポジトリをTravisCI側で許可する
   * 参考サイト：[Travis CI入門 Travis CIとGitHubでCIを実現する方法(Change the World!)](http://changesworlds.com/2014/09/introduction-to-travis-ci-and-github-001/)
* forkしたリポジトリの README.md ファイルの「t-kougei-game-comp」の部分を自分のGitHubアカウント名に差し替えてください(2箇所)
* 問題を解いて、テストを通るようにしてください。
* fork 元の master ブランチにプルリクエストを投げてください

# テスト結果

[![Build Status](https://travis-ci.org/t-kougei-game-comp/09_tree.svg?branch=develop)](https://travis-ci.org/t-kougei-game-comp/09_tree)

# 今回の問題

2分木の勉強です。

入力される数字を木構造に格納してください。

input?.txt ファイルを標準入力として読み込んで、標準出力の結果を output?.txt ファイルと一致するか比較するテストをします。

main.c ファイルだけを書き換えて下さい。

## 入力される値
入力は以下のフォーマットで与えられます。
~~~
n
n
n
~~~

nは数字です。入力された数字をもつノードを作成し、数字が小さければ左のノードとして、数字が大きければ左のノードとして再帰的に格納して下さい。

## 期待する出力

全ての入力を読み込んだ後、全てのノードを数字の小さな順に出力してください。各行、次のフォーマットで出力をしてください。
~~~
n l r
~~~
* n: 現在のノードの値
* l: 左側の子供のノードの値(子ノードがなければ0)
* r: 右側の子供のノードの値(子ノードがなければ0)

最後は改行し、余計な文字、空行を含んではいけません。

## 条件
すべてのテストケースで以下の条件を満たします。
* 1 <= n <= 100


## 入力例1
~~~
2
1
3
~~~
* 1行目の文字列はは「2」なので、新たにノードを作り、値に2を格納します
* 2行目の文字列はは「1」なので、「2」のノードの左側の子供として、値1を持つ新たなノードを追加します
* 3行目の文字列はは「3」なので、「2」のノードの右側の子供として、値3を持つ新たなノードを追加します

## 出力例1
~~~
1 0 0
2 1 3
3 0 0
~~~

## 入力例2
~~~
3
2
1
~~~

## 出力例1
~~~
1 0 2
2 0 3
3 0 0
~~~
