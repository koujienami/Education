# 第1回現場で使えるAWS勉強会

### 今日やる事
**Ruby on Railsの開発環境(IDE)を用意し、簡単なHelloWorldの実装。**  
**基本型、クラス、メソッドなどのプログラミング基礎。**

### 実施した学習内容

### 理解したこと

### ハマった部分と解消方法
RailsによるHelloWorldアプリケーションを作成する際、Model/Controller/Viewを作成するが  
参考にした記事ではController側に一切処理を記載していなかった為  
ViewでHelloWorldを表示する際に、NoSuchMethod例外が発生した。  
Controller側に処理を追加して対応した。結果はGitHub側のソースに反映済み。  
  
Macでのインストール作業時にrbenvを入れてrubyのバージョン切り替えを行ったがうまく行かず。  
参考サイトを参考に、rbenvのパスの確認や、bash_profileへのパス追加を行って変更出来た。  
  
Railsの環境を作り、プロジェクトのbundle install時にmysqlが入らなかった。  
こちらも参考サイトのコマンドを入力することで、うまく動作した。原因はなんだろう……Macで発生。  

### 参考サイト
[WindowsでRuby on Rails Tutorial (Railsチュートリアル) の環境構築。localhost:3000を表示するまで。](https://azumayuri.hatenablog.com/entry/2018/08/08/034005)  
[MacにHomeBrew,rbenv,bundlerをインストールする](https://qiita.com/shinkuFencer/items/3679cfd966f6a61ccd1b)  
[Ruby on Rails チュートリアル 第1章 ゼロからデプロイまで](https://railstutorial.jp/chapters/beginning?version=5.1#sec-installing_rails)  
[Ruby on RailsでHelloWorldプロジェクト](https://qiita.com/Knoth/items/8627c33fcd926ff014a4)  
[RailsプロジェクトでMySQLがbundle installできなかった](https://qiita.com/akito19/items/e1dc54f907987e688cc0)
  
[Ruby on RailsでHelloWorldのGitHub](https://github.com/koujienami/HelloWorld)