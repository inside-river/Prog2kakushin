# Prog2kakushin
課題用のリモートリポジトリ

# work１

## 概要
 
　　相関係数のヒートマップを各プロットの相関係数に応じてプロットの大きさを変えて表示します。

## 用途

  　色だけの場合、微妙な色の違いが分かりにくいですが、大きさに違いを出すことで、最初にどこを見るべきか、あるいは、ある項目に対して強く相関している変数ベスト３がどれか、等の情報がより分かりやすくなります。
  
 ## 出力と入力

 ### 入力について
  
 　 10行目にcsvファイルのファイル名を入力してください。ファイルを読み込むと、そのファイルのデータの相関係数のヒートマップを出力します。今回は、csvファイルが準備できなくても実行できるように、一つ目のセルに、下の画像に示すデータをあらかじめ用意しています。それを使う場合は、先に一つ目のセルを実行し、10行目を「＃」でコメントにして、実行されないようにしてください。そうすれば、用意したデータの相関係数のヒートマップが出力され、動作を確認することができます。

 ![スクリーンショット 2024-01-25 124132](https://github.com/inside-river/Prog2kakushin/assets/153084918/c26bcd76-8ca5-4e5b-a4c6-b0ea9fa9acb4)

 （参考文献　JNTO、”日本の観光統計データ”、https://statistics.jnto.go.jp/　、データ更新日:2020/08/05）

### 出力について

　　データの相関係数のヒートマップが表示されます。正の相関は青、負の相関は赤で表します。また、プロットの大きさでも判断することができ、プロットが大きいほど相関が強く、小さいほど相関が弱いことになります。以下は出力の例です。

![スクリーンショット 2024-01-25 123848](https://github.com/inside-river/Prog2kakushin/assets/153084918/0a80d4f0-c6de-402c-9d66-c08f25d26327)

# work2

## 概要

  　入力された値をもとに、最小二乗法を用いて確率誤差を求め、入力した座標の点、近似式の直線、確率誤差の範囲を示すグラフが表示されます。

## 用途

 　　物理実験でグラフを書いたり、考察する際に確率誤差を考慮しますが、確率誤差を求める計算の過程が多く、Excelを用いてもある程度時間が掛かっていました。そこで、値だけ入力すれば確率誤差を出してくれるプログラムがあれば便利だと思い、作成しました。


## 入力と出力

### 入力について

　　始めに、近似するxとyの値を入力してもらいます。プログラムを実行すると、以下のように「x座標を入力せよ」と表示されるので、近似するxの値を入力してください。

 ![スクリーンショット 2024-01-23 170059](https://github.com/inside-river/Prog2kakushin/assets/153084918/2585c8b8-c962-4956-a480-f0fa93665d76)

　　次に、以下のように「対応するyの値を入力せよ」と表示されるので、先ほど入力したxの値に対応するyの値を入力してください。

![スクリーンショット 2024-01-23 170115](https://github.com/inside-river/Prog2kakushin/assets/153084918/d47b2892-12a6-4658-9585-08561b1c430c)
  
  　xとyの値の入力を繰り返し行い、近似に必要なデータを全て入力し終えたら、「x座標を入力せよ」の表示の時に、「stop」と入力してください。（その例を以下に示します。）すると、入力は終わり、最小二乗法の計算を実行します。

![スクリーンショット 2024-01-23 170153](https://github.com/inside-river/Prog2kakushin/assets/153084918/2d8d43aa-cf88-44b6-bf25-d05974cd1d62)
  
### 出力について

　　出力内容は以下の通りです。

#### １．入力したxとyの値

　　入力したxとyの値がリストの形式で表示されます。

#### ２．回帰式の傾きa、y切片b

　　入力したデータから最小二乗法で求められた回帰式の傾きa、y切片bを、確率誤差を含めて表示します。

#### ３．グラフ

　　入力したx、yの値が示す座標をシアンの丸い点、求めた回帰式の直線を青い線、確率誤差を考慮した範囲を水色で塗りつぶしたグラフを表示します。

![スクリーンショット 2024-01-23 170207](https://github.com/inside-river/Prog2kakushin/assets/153084918/d30645e4-ea9a-406c-8a8f-27769b787105)

# work3

## 概要

　　画像の一部を切り抜き、別の画像に貼りつけるプログラムです。

## 工夫
  
　　インターネットで調べると、画像から背景を削除するライブラリを見つけたので使ってみようと思いました。しかし、参考にしたプログラムは、背景を削除した画像を白黒にし、元の画像に貼りつける、というものでした。そこで、切り抜く画像と背景の画像は別のものを使用すること、合成した画像が白黒ではなくカラーになること、を実現できるように考えました。


## 出力と入力

### 入力について

　　画像については、以前の授業で使用したファイルからキツネの画像と砂漠の画像を使用しています。そのファイルごと持ってきており、いくつかの画像が入っているので、別の画像に変更して実行してもらうこともできます。（変更する場合、'fox'と'desert'の部分を好きな画像の名前に変えてください。）基本的にはそのまま実行できるので、特別何かを入力してもらうことはありません。

### 出力について

　　プログラムを実行すると、最初に、画像の背景削除に必要なrembgというライブラリのインストールを開始します。インストールが終わると、画像処理が実行され、キツネの画像からキツネだけを切り抜き、砂漠の画像に貼りつけたものが保存されます。作成した画像は、左側のファイル一覧の中に「final_output.png」として以下のように保存されるので、ダブルクリックで開いて確認することができます。

![スクリーンショット 2024-01-25 110609](https://github.com/inside-river/Prog2kakushin/assets/153084918/3bb4fd32-f319-4f2b-8956-9c7e22090100)

