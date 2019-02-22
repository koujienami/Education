# 第9回現場で使えるAWS勉強会

### 今日やる事
****
**作成したAWS環境のCloudFormation(JSON)を抽出し、テンプレートを作るためのコード作成。**  

### 実施した学習内容
****
RubyMineの環境構築  
SparkleFormationのインストールと簡単なコード内容  
開発環境(IDE)の違いや選び方  
情報の調べ方  

### 理解したこと
****
RubyMineでの環境構築手順について。  
SparkleFormationのコマンドの内容、やってくれること、コードの中身やJSON出力の方法。  
AtomやVS Codeなどの他の開発環境との違いについて。Atomなどはテキストエディタがベース。RubyMineは開発環境の位置づけ。  
まずは公式から調べるのが基本(英語でも)。別にChromeの翻訳機能を使っても構わない。公式の情報が正としてやる。  

### ハマった部分と解消方法
****
#### RubyMine上でターミナルを起動し、SparkleFormationのコマンド実行した際に文字化け。  
現時点でも原因不明。文字コードを修正したりしても解決せず。  
またRubyMine上ではなく通常通りターミナルから実行しても文字化けしたのでRubyMineが原因ではなさそう。  
  
#### IntelliJ IDEAとRubyMineとで微妙にプロジェクトの構成が違う。  
これはRubyMine側(動画)が正解。  
IntelliJの場合はRubyプラグインを入れる必要があるが、適切に入っておらずプロジェクトにモジュールがインストールされてなかった。  
IntelliJでRuby開発をする場合の参考サイトを見る事で解決。  

### 参考サイト
****
#### CloudFormation関連
[(公式)SparkleFormation](https://www.sparkleformation.io/)  
[CloudFormationのtemplateをRubyで作成 – 「SparkleFormation」を触ってみた。](https://dev.classmethod.jp/cloud/aws/introduce-of-sparkleformation/)  

#### ハマりポイント解決
[IntelliJ IDEA Rubyの開発環境を作成する](https://qiita.com/keitakn/items/76d6707db7d23fe4ca85)

#### GitHub
[Ruby on RailsでWebアプリ作成](https://github.com/koujienami/TimeLine)