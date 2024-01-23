# Prog2kakushin
課題用のリモートリポジトリ

# work１

## 概要
 
　　相関係数のヒートマップを各プロットの相関係数に応じてプロットの大きさを変えて表示します。

## 用途

  　色だけの場合、微妙な色の違いが分かりにくいですが、大きさに違いを出すことで、最初にどこを見るべきか、あるいは、ある項目に対して強く相関している変数ベスト３がどれか、といったような情報がより分かりやすくなります。
  
 ## 出力と入力

 ### 入力について
  
  10行目でcsvファイルのファイル名を入力して読み込むと、そのファイルのデータの相関係数のヒートマップを出力します。今回は、csvファイルが準備できなくても実行できるように、データをあらかじめ用意しているため、10行目を「＃」でコメントにして、実行されないようにし、13～24行目の「＃」を外して実行できるようにすれば、用意したデータの相関係数のヒートマップを出力するので、動作を確認することができます。


# work2

## 概要

  入力された値をもとに、最小二乗法を用いて確率誤差を求め、入力した座標の点、近似式の直線、確率誤差の範囲を示すグラフが表示されます。

## 用途

 　物理実験でグラフを書いたり、考察する際に確率誤差を考慮しますが、確率誤差を求める計算の過程が多く、Excelを用いてもある程度時間が掛かっていました。そこで、値だけ入力すれば確率誤差を出してくれるプログラムがあれば便利だと思い、作成しました。


## 入力と出力

### 入力

　始めに、近似するxとyの値を入力してもらいます。プログラムを実行すると、「x座標を入力せよ」と表示されるので、近似するxの値を入力してください。

 ![スクリーンショット 2024-01-23 170059](https://github.com/inside-river/Prog2kakushin/assets/153084918/2585c8b8-c962-4956-a480-f0fa93665d76)


 　次に、「対応するyの値を入力せよ」と表示されるので、先ほど入力したxの値に対応するyの値を入力してください。
  
  xとyの値の入力を繰り返し行い、近似に必要なデータを全て入力し終えたら、「x座標を入力せよ」の表示の時に、「stop」と入力してください。すると、入力は終わり、最小二乗法の計算を実行します。

### 出力

出力内容は以下の通りです。

#### １．入力したxとyの値

入力したxとyの値がリストの形式で表示されます。

#### ２．回帰式の傾きa、y切片b

入力したデータから最小二乗法で求められた回帰式の傾きa、y切片bを、確率誤差を含めて表示します。

#### ３．グラフ

入力したx、yの値が示す座標をシアンの丸い点、求めた回帰式直線を青い線、確率誤差を考慮した範囲を水色で塗りつぶしたグラフを表示します。


≪work3について≫

　・プログラムの概要

   　画像の一部を切り抜き、別の画像に貼りつけるプログラム。

  ・工夫した点
  
  　　インターネットで調べた方法を参考にしたが、それは切り抜いた画像を白黒にし、元の画像に貼りつけて戻す、というものだった。そこで、切り抜く画像と背景の画像は別のものを使用すること、合成した画像が白黒ではなくカラーになること、を実現すべく、に自分で考えてコードを書いた。


   ・出力と入力

   　　以前の授業で使用したファイルからキツネの画像と砂漠の画像を使用しており、キツネの画像からキツネだけを切り抜き、砂漠の画像に貼りつけたものが保存される。ファイルには、いくつかの画像が入っているので、別の画像に変更してもよい。
