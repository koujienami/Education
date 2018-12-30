# 第4回現場で使えるAWS勉強会

### 今日やる事
****
**CRUD処理の実装。**

### 実施した学習内容
****
参考サイトのチュートリアルを黙々と進めた。(前回と同じ)  
お気に入り機能とコメント機能の追加。  
ただし、コメント機能についてはコードサンプルなどはなく、自分で考えて進める形式だったため、完了した人はゼロ。

### 理解したこと
****
Railsを使った、多対多の連携。  
親子関係を持った処理の実装、削除処理の実装。  
自身で設計をして行う実装の難しさ。  
RailsもRubyもまだまだ全然理解できていないという事。

### ハマった部分と解消方法
****
#### 起動後にサイトを表示しようとするとエラー
文字コードが変わっていたことによる不具合。文字コードをUTF-8に変換しなおすことで解消。

#### ExecJS::ProgramError「TypeError: オブジェクトでサポートされていないプロパティまたはメソッドです。」と表示される
[書籍『Ruby on Rails 5 超入門』つまずきやすいポイントまとめ【Chapter2】](https://qiita.com/laineek/items/121a9a20d5eb26fb56f4)  
の[p.84] stylesheet_link_tagでエラーが発生した場合の対処法を参照し解決

#### コメント機能作成
今まで実施したことを参考に解決しようとしているが、現時点では未解決。  

#### ルーティングのresouces, resouceがわからない
CRUD操作に対応付けられたルーティングを自動生成するもの。
（具体的にはindex, new, create, show, edit, update, destroy）  
後ろにonly: [*~~]とすることでその中の特定のアクションだけ作ることも可能。

#### 〜〜_pathとは
URLを示すprefix。  
ターミナルでrails routesと叩くとルーティングが出て来るが、その中のPrefixに当たる部分。  
これを利用して、URLを指定してやると柔軟性を持たせる事が出来る。

#### アソシエイションを記述する意味
アソシエイションを記述することで、紐づいたモデルからデータを引っ張って来るのが楽になる。
今回のケースでアソシエイション無しでコメントユーザーを取得しようと思うと    
`User.find(comment.user_id).email`  
となるが、アソシエイションを記述しておくと  
`comment.user.email`  
と各モデル間の関係性を表現する形で記述が可能となる。

### 参考サイト
****
#### チュートリアル
[初心者向け】丁寧すぎるRails『アソシエーション』チュートリアル【幾ら何でも】【完璧にわかる】](https://qiita.com/kazukimatsumoto/items/14bdff681ec5ddac26d1)  

#### ハマりポイント対応
[Rails のルーティング](https://railsguides.jp/routing.html)  
[Railsのルーティングを極める (後編)](https://techracho.bpsinc.jp/baba/2014_03_03/15619)  
[【Rails初心者向け】モデル間の関連付け（アソシエーション）まとめ](https://qiita.com/To_BB/items/47d2c7b1bc3513025d7b)  

#### Ruby基礎
[Ruby基礎文法](https://qiita.com/Fendo181/items/eb2cb17f32d99aa01f59)  
[[初心者向け] RubyやRailsでリファクタリングに使えそうなイディオムとか便利メソッドとか](https://qiita.com/jnchito/items/dedb3b889ab226933ccf)

#### GitHub
[Ruby on RailsでWebアプリ作成](https://github.com/koujienami/TimeLine)