# MTSA-Training
*Modal Transition System Analyser*

[MTSA webpage](http://mtsa.dc.uba.ar/)

## 注意 ##
このリポジトリに含まれるmtsa.jarは，FSPをコンパイルするごとに「mtsa.jar」が置かれているディレクトリのファイルすべてがgit上にアップロードされます．
必ず，ネットワークのつながる環境で作業を行ってください．
※通常盤はこちらからダウンロードしてください(https://github.com/iTaku3/mtsa_waseda.git)

以下，MTSAでFSPコンパイル時に自動で実行されるコマンドです．（MTSAコンパイル結果の頭の方に少しだけログが出ます）
```
$ git add <mtsa.jarがあるディレクトリ>
$ git commit -m "automatic logging"
$ git push
```

## 環境構築 ##
1. リポジトリのクローン  
以下のコマンドを自身のPCのターミナル（コマンドプロンプト）上で実行する
```
$ git clone https://github.com/tei-lab-univ/MTSA-Training.git
```

2. 自分用作業ブランチの作成  
以下のコマンド実行し，自身の作業するブランチをローカルとリモートに作成する．
<ブランチ名>には好きな文字列で良いですが，自身の名前（例：yamauchi）を推奨します．
```
$ cd MTSA-Training
$ git checkout -b <ブランチ名(ローカル)>
$ git push -u origin <ブランチ名(リモート)>
```

3. mtsa.jarをダウンロードして「MTSA-Training」に配置する  
以下のURLからmtsa.jarをダウンロードして，「MTSA-Training」ディレクトリ内に配置する．  
mtsa.jar：https://waseda.box.com/s/asm6gj8b6h0sp6xrx1mop5gvwhhcwjj1
```
MTSA-Training
├── mtsa.jar /*ここに配置する*/
├── README.md
├── log.out
└── workspace
    ├── xxxx.lts
    ├── xxxx.lts
    :
```

4. mtsaを起動して，制御器合成を行う  
mtsaを起動して演習を実施する．「-Xmx」以降には使用したいメモリを指定すると良い．
jarファイルをダブルクリックして起動することも可能だが，使用メモリをOSが勝手に制限するため，評価実験の際には必ず以下コマンドで起動すること！
```
$ java -jar -Xmx8G mtsa.jar
```

## 参考 ##
MTSAコードの記述方法（FSP）やLTSについて詳細を知りたい場合は以下ページを参照してください．  
  
FSP Reference：https://www.doc.ic.ac.uk/~jnm/LTSdocumention/FSP-notation.html  
FSP Quick Reference：https://www.doc.ic.ac.uk/~jnm/book/firstbook/ltsa/Appendix-A.html  
LTSA：https://www.doc.ic.ac.uk/ltsa/  