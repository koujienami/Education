# 第1回現場で使えるAWS勉強会

### 今日やる事
****
**Ruby on Railsの開発環境(IDE)を用意し、簡単なHelloWorldの実装。**  
**基本型、クラス、メソッドなどのプログラミング基礎。**


### 実施した学習内容
****
勉強会の概要について簡単に解説。Rubyという言語の選定理由など説明。  
学習については、 **Ruby on Railsの開発環境(IDE)を用意し、簡単なHelloWorldの実装。** の途中まで。  
**基本型、クラス、メソッドなどのプログラミング基礎。** については時間が足りず。


### 理解したこと
****
勉強会の主旨。概要。目的。  
環境構築の難儀さ( ≠ 難しさ)やハマりポイントでの解決方法。  
自己解決能力の重要性。  
Railsでのアプリケーション作成の基礎や手順。  
いくつかの基礎的なLinuxコマンドやruby、bundler、railsのコマンド。


### ハマった部分と解消方法
****
#### Controllerの処理未記載
RailsによるHelloWorldアプリケーションを作成する際、Model/Controller/Viewを作成するが  
参考にした記事ではController側に一切処理を記載していなかった為  
ViewでHelloWorldを表示する際に、NoSuchMethod例外が発生した。  
Controller側に処理を追加して対応した。結果はGitHub側のソースに反映済み。  

#### rubyバージョンの切り替えが出来ない(Macのみ)
Macでのインストール作業時にrbenvを入れてrubyのバージョン切り替えを行ったがうまく行かず。  
参考サイトを参考に、rbenvのパスの確認や、bash_profileへのパス追加を行って変更出来た。  

#### mysqlインストール時にPATHが通っておらず、インストール出来ない(Macのみ)
Railsの環境を作り、プロジェクトのbundle install時にmysqlが入らなかった。  
こちらも参考サイトのコマンドを入力することで、うまく動作した。原因はなんだろう……Macで発生。  

#### rubyコマンドが実行できない。
インストールには成功するが、その後のrubyコマンドやbundleコマンドが実行できない。  
「存在しません」という例外が出るが、実際に確認するとrubyやbundleの実行ファイルがなくなっている。  
原因としては「Avast」によって危険なファイルと認識され除外されていた為。  
Avast側で除外対象から消すことで、正常に動作するようになった。

#### ./Gemfileという記載がわからない。
参考サイトでは、対象ファイルの表示という意図で使っていたが、意味がわからず実行できなかった。

#### MySQLへの接続が失敗する。
MySQLをインストール後にサーバーを起動していなかった為に発生した。  
また、MySQL接続時のユーザーとパスワードの不一致(パスワードが不要だった)により、接続に失敗した。

#### cannot load such file -- sqlite3/sqlite3_native (LoadError)が発生する。(Windows)
Windows環境においてのみ、soファイルというものが必要になるらしく、下記参考サイトに基づいた対応が必要。

#### sqliteとMySQLで変更するポイント
Railsのデフォルトはsqliteとなっており、MySQLにするには定義変更が必要。  
参考サイトはMySQLベースになっているため、コマンドなどで「mysql」とある部分は全て「sqlite」へ変更が必要。


### 参考サイト
****
#### 環境構築
[WindowsでRuby on Rails Tutorial (Railsチュートリアル) の環境構築。localhost:3000を表示するまで。](https://azumayuri.hatenablog.com/entry/2018/08/08/034005)  
[MacにHomeBrew,rbenv,bundlerをインストールする](https://qiita.com/shinkuFencer/items/3679cfd966f6a61ccd1b)  
[Ruby on RailsでHelloWorldプロジェクト](https://qiita.com/Knoth/items/8627c33fcd926ff014a4)  
[環境構築　004　Windows版MySQLインストール](https://qiita.com/KeisyaRinco/items/c3074d8450cad96f7e4f)  

#### 課題解決
[RailsプロジェクトでMySQLがbundle installできなかった](https://qiita.com/akito19/items/e1dc54f907987e688cc0)  
[mysqlが起動できない（Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)）](https://qiita.com/carotene4035/items/e00076fe3990b9178cc0)  
[mysql起動で「The server quit without updating PID file」](https://qiita.com/mogetarou/items/e34ca51d3756d55d7800)  
[WindowsでRailsTutorialするときに気をつけること](https://qiita.com/jun_moka/items/a83a8149bc97cedc16b5)  

#### GitHub
[Ruby on RailsでHelloWorld](https://github.com/koujienami/HelloWorld)