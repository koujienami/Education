# 第6回現場で使えるAWS勉強会

### 今日やる事
****
**EC2インスタンスの立ち上げまで。**  
**EC2、RDS、ELB、S3の環境を構築しながら、各種繋ぎこみとアプリケーションのデプロイ。**  

### 実施した学習内容
****
EC2インスタンスの立ち上げを行い、Railsアプリケーションのデプロイ準備まで。  
一部の処理でハマりポイントもあり、Railsアプリケーションのデプロイまでは出来ず。  

### 理解したこと
****
Rails固有のハマりポイントがあること。  
EC2やRDSを使ったAWSの環境構築。  
ポートフォリオを作成する事の是非や採用サイドのちょっとした小話。  

### ハマった部分と解消方法
****
#### アプリケーションの課題
ruby 2.5.3とbundler2.0.1の組み合わせはbundler側にバグがあり、bundle installが動かない。  
config/secrets.ymlはrailsの5.2からはデフォルトでは作られないようになっている。  
credential.yml.encに記載されており、専用のコマンドで編集することで設定変更が可能。  

#### 環境構築作業手順の不備
epelのリポジトリ設定の仕方が参考サイトに記載がない。

#### 環境構築時にハマったポイント
EC2にWindowsからログインするとき、Key-Pairをどう使うのかがわからなかった。  
EC2にパブリックDNSが振られていない為に接続できなかった。  
それぞれ参考サイトを参照して解決。

### 参考サイト
****
#### AWSにアプリケーションデプロイまで
[(下準備編)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/f795fe3e661a3349a7ce)  
[(DB・サーバー構築編)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/22cfbf4bf7ec95f6ac1c)  
[(デプロイ編①)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/814e0979217b1a25aa3e)  
[(デプロイ編②)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/5a1757d222806cbe0cd1)  

#### 課題解決
[【Ruby2.6.0】find_spec_for_exe: can't find gem bundler (>= 0.a) with executable bundle (Gem::GemNotFoundException)　エラーの解決方法](https://www.yokoyan.net/entry/2019/01/11/181500)  
[Rails5.2からsecrets.yml*が廃止されcredentials.yml.encに統合されるよ](https://qiita.com/daichirata/items/da40e205d273ae69fcfc)  
[Amazon EC2 での EPEL の有効化](https://aws.amazon.com/jp/premiumsupport/knowledge-center/ec2-enable-epel/)  
[[初心者向け] 初めてのEC2ログイン：Linux編](https://dev.classmethod.jp/cloud/aws/first-login-to-ec2-linux/)  
[AWS EC2 インスタンスにパブリックDNSを割り振られない時の解決方法　初心者向け](http://hakumaix.hatenablog.com/entry/2017/09/02/132146)  

#### GitHub
[Ruby on RailsでWebアプリ作成](https://github.com/koujienami/TimeLine)