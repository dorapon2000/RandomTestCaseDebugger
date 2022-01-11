# 概要

以下のことができる環境です

1. ランダムなテストケースの作成
2. 作成した2つのプログラムに対して1.で作成したテストケースを実行
3. 2.の実行結果を比較し、実行結果を出力

WAが出たときにどんなケースでWAが出るのかあぶりだす用途を想定しています

WAが出た解法と愚直解を用意してください

当然ながら、愚直解が誤っていた場合は正しく動作しません

また、本環境を使えば必ずWAが出るケースを特定できる保証もありません

本環境に含まれるプログラムがバグっていたとしても責任は負いません

# 各ファイル

### Solve1.py

解法1を書くファイルです

01_Template.txtのフォーマットに従ってください

### Solve2.py

解法2を書くファイルです

Solve1.pyと同じ対応をしてください

### TestCaseMaker.py

テストケースを作成するpythonファイルです

実行すると、テストケースの作成処理が走ります

生成するテストケースの数を変えるときはtestCaseNumの値を変えてください

MakeTestCase()の中を書き換えて入力の形式を指定してください

詳しくは下記の「入力形式の指定方法」を参照してください

作成したテストケースはin以下にtext形式で保存されます

### Debug.py

各テストケースの実行および結果を管理するプログラムです

実行すると、実行と結果管理の処理が走ります

特に変更が必要な箇所はありません

実行結果の出力はout以下に保存されます

すべてのケースに対する結果のまとめがresult.txtに記載されます

### FileLib.py

デバッグに必要な結果ファイルを管理するためのライブラリです

特に変更が必要な箇所はありません

# 入力形式の指定方法

TestCaseMaker.pyの中のMakeTestCase()を書き換えて入力形式を指定します

TestCaseMaker.pyの中の各関数を利用して値を作成してください

PrintTestCase()に値を渡すことでファイルに書き込みを行います

PrintTestCase()は通常のPrint()と同じ形式で使えます

デフォルトの状態では下記の形式になっています

```
n m
a1 a2 a3 ... an
b1 b2 b3 ... bm
```
