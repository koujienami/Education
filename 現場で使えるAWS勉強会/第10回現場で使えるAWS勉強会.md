# 第10回現場で使えるAWS勉強会

### 今日やる事
****
**作成したAWS環境のCloudFormation(JSON)を抽出し、テンプレートを作るためのコード作成。**  

### 実施した学習内容
****
CloudFormationの作成をSparkleFormationではなく、YAMLを直接書く方法に変更。  
IntelliJ、RubyMineのプラグインで配布されている「AWS CloudFormation」というプラグインを導入。  
それによってYAMLに対して補完が効くようになった為、快適に書けるようになった。

### 理解したこと
****
SparkleFormationは複数のクラウドサービスに対応しているという点は魅力的なものの、補完のききにくさなどもあり慣れないうちは使いづらい。  
学習コストが高いということが判明したので、YAMLに切り替えた。  
YAML自体は書きやすく、特に困ることもなく書ける。AWS公式のドキュメントをそのまま利用できるのも楽。  

### ハマった部分と解消方法
****
特になし。  

### 参考サイト
****
#### CloudFormation関連
[(公式)SparkleFormation](https://www.sparkleformation.io/)  
[CloudFormationのtemplateをRubyで作成 – 「SparkleFormation」を触ってみた。](https://dev.classmethod.jp/cloud/aws/introduce-of-sparkleformation/)  
[InteliJ IDEAのCloudFormationプラグインを使ってみた](https://dev.classmethod.jp/tool/impression-for-intelij-idea-cloudformation-plugin/)

#### GitHub
[Ruby on RailsでWebアプリ作成](https://github.com/koujienami/TimeLine)  
[CloudFormationTemplate](https://github.com/koujienami/CloudFormationTemplate)