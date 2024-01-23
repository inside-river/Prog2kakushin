# Prog2kakushin
課題用のリモートリポジトリ

#work１

　・どういうプログラム？
 
　　　相関係数のヒートマップを各プロットの相関係数に応じてプロットの大きさを変えるように表示したもの。
  
  ・どんな状況で役立つか？なぜ作ったのか？
  
  　　色だけの場合、微妙な色の違いが分かりにくいが、大きさに違いを出すことで、最初にどこを見るべきか、あるいは、ある項目に対して強く相関している変数ベスト３がどれか、といったような情報がより分かりやすい。
  
  ・出力と入力
  
  　　10行目でcsvファイルのファイル名を入力して読み込むと、そのファイルのデータの相関係数のヒートマップを出力する。今回は、csvファイルが無くても実行できるように、データをあらかじめ用意しているため、10行目を「＃」でコメントにするなどして、実行されないようにし、13～24行目の「＃」を外して実行できるようにすれば、用意したデータの相関係数のヒートマップを出力するので、動作を確認することができる。



≪work2について≫

　・どういうプログラム？

   　入力された値をもとに、最小二乗法を用いて確率誤差を求め、入力した座標の点、近似式の直線、確率誤差の範囲を示すグラフが出力される。

  ・どんな状況で役立つか？なぜ作ったのか？

  　　物理実験でグラフを書いたり、考察する際に確率誤差を考慮するが、確率誤差を求める計算の過程が多く、Excelを用いてもある程度時間が掛かる。そこで、値だけ入力すれば確率誤差を出してくれるプログラムがあれば便利だと思ったから。


   ・出力と入力

   　　始めにinput関数によって出力される指示通り、xの値とyの値を入力する。値の入力を終えるときに「stop」と入力すれば、入力した値のリストと、確率誤差、グラフが表示される。グラフは、入力した値がとる点をシアン、近似式を青、確率誤差の範囲を水色で塗りつぶしたものが出力される。



≪work3について≫

　・プログラムの概要

   　画像の一部を切り抜き、別の画像に貼りつけるプログラム。

  ・工夫した点
  
  　　インターネットで調べた方法を参考にしたが、それは切り抜いた画像を白黒にし、元の画像に貼りつけて戻す、というものだった。そこで、切り抜く画像と背景の画像は別のものを使用すること、合成した画像が白黒ではなくカラーになること、を実現すべく、に自分で考えてコードを書いた。


   ・出力と入力

   　　以前の授業で使用したファイルからキツネの画像と砂漠の画像を使用しており、キツネの画像からキツネだけを切り抜き、砂漠の画像に貼りつけたものが保存される。ファイルには、いくつかの画像が入っているので、別の画像に変更してもよい。
