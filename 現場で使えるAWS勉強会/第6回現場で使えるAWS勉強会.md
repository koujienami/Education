# 第6回現場で使えるAWS勉強会

### 今日やる事
****
**EC2インスタンスの立ち上げまで。**  
**EC2、RDS、ELB、S3の環境を構築しながら、各種繋ぎこみとアプリケーションのデプロイ。**  

### 実施した学習内容
****

### 理解したこと
****

### ハマった部分と解消方法
****
ruby 2.5.3とbundler2.0.1の組み合わせはbundler側にバグがあり、bundle installが動かない。  
config/secrets.ymlはrailsの5.2からはデフォルトでは作られないようになっている。  
credential.yml.encに記載されており、専用のコマンドで編集することで設定変更が可能。  
epelのリポジトリ設定の仕方が参考サイトに記載がない。

### 参考サイト
****
#### AWSにアプリケーションデプロイまで
[(下準備編)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/f795fe3e661a3349a7ce)  
[(DB・サーバー構築編)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/22cfbf4bf7ec95f6ac1c)  
[(デプロイ編①)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/814e0979217b1a25aa3e)  
[(デプロイ編②)世界一丁寧なAWS解説。EC2を利用して、RailsアプリをAWSにあげるまで](https://qiita.com/naoki_mochizuki/items/5a1757d222806cbe0cd1)  

#### GitHub
[Ruby on RailsでWebアプリ作成](https://github.com/koujienami/TimeLine)