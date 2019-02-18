# 第8回現場で使えるAWS勉強会

### 今日やる事
****
**EC2、RDS、ELB、S3の環境を構築しながら、各種繋ぎこみとアプリケーションのデプロイ。**  
**作成したAWS環境のCloudFormation(JSON)を抽出し、テンプレートを作るためのコード作成。**  

### 実施した学習内容
****
ELBを実際に導入してみる。  
ELBはElasticIPとの関連付けには対応していないので、ドメイン登録をしてそれとEIPを紐づけないといけない。  
(そうしないとELBにアクセスして、各EC2インスタンスの振分が上手くいかない)  
ただしここらへんはnginxやunicorn側の設定でどうにかなるかも。  
  
S3について学習。バケット・オブジェクト・キーの関係性について解説。  
またAmazon内で良く使われている「結果整合性モデル」についても解説。  

作成したAWS環境をCloudFormerを使って抽出。  
しかしCloudFormerがbeta版であることや非対応のサービスがあることなどから業務で使うには難しい事も判明。  

### 理解したこと
****
ELBの導入は簡単。  
S3も仕組みは簡単(使ってはない)。  
CloudFormerを使ったテンプレート抽出も簡単。  
  
ただし、AWSのサービスには制約も色々あるので、そこらへんを理解していないと実業務での運用に耐えられない。  
CloudFormerに至ってはbeta版な上にサービス非対応のものがあったりするので、かなり微妙という状態。  
CloudFormationで読み込むテンプレートはJSON,YAML。またJSONのものをYAMLに変換も出来る。  
CloudFormationのテンプレートを作成するRubyのフレームワークがあるっぽい。  
  
S3の中で結果整合性について解説。使ってはないので仕組みの理解のみ。  

### ハマった部分と解消方法
****
#### ELBからアクセスしてアプリの表示が出来ない
単純にELB→Webサーバー→APサーバーと来たとき、Webサーバー側でServerNameをEIPにしている。  
つまりEIPでのアクセス時にAPサーバーと連携するようになっているが、ELBはEIPと関連付け出来ないので、独自のホスト名になる。  
その為、ELBで接続した際はWebサーバー側がAPサーバーへ連携しない為、アプリの表示が出来なかった。

#### CloudFormerの使い方がわからない
CloudFormationの画面でCloudFormerから読み込むという選択をしても、それっぽい画面にならない。  
これは単純に選択の中にCloudFormerがあったので、画面確認漏れ。ただし非常に分かりづらい画面になっている。  
参考サイトを見て解決。

#### CloudFormer経由でスタックが作れない
原因は最終的に不明。VPC選択画面でDefaultVPCを選択した時にスタックが作成できずにエラーで落ちる。  
これは恐らく新規作成した時にIAMやIGWなどを作成していたので、DefaultVPCにそれらがなく、作成できないからではと予想。  

### 参考サイト
****
#### AWSのサービス解説
[【AWS】S3まとめ](https://qiita.com/iron-breaker/items/f35c1d54887c434a321a)  
[【超入門】負荷分散をAWSのロードバランサーを使ってやってみよう](https://qiita.com/okamu_/items/c051156e44c4fbd65234)  
[【CloudFormation入門1】5分と6行で始めるAWS CloudFormationテンプレートによるインフラ構築](https://dev.classmethod.jp/cloud/aws/cloudformation-beginner01/)
[【AWS】CloudFormerの使い方](https://qiita.com/MokoNakano/items/21ce2e9de435798593c6)

#### GitHub
[Ruby on RailsでWebアプリ作成](https://github.com/koujienami/TimeLine)