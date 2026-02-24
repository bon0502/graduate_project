### ER図
[![Image from Gyazo](https://i.gyazo.com/2a36e1bb898baa684f85d475c50057a4.jpg)](https://gyazo.com/2a36e1bb898baa684f85d475c50057a4)

### 本サービスの概要（700文字以内）
　このアプリは、グミをレビューするアプリです。概要は、グミを投稿してレビューをする、グミを検索する、自分の好きなグミタイプを検索の条件に入れ、新しいグミとの出会いをお手伝いするアプリになっています。想定ユーザーはグミが好きな人たちです。年代も幅広いと思うのでみんなが使いやすいボタン配置、設定にしていきたいです。
### MVPで実装する予定の機能
- グミの登録（画像、グミの詳細付き）
- コメント機能
- いいね機能
- プロフィール編集機能
- 検索機能

### テーブル詳細
#### usersテーブル
- name : string / ユーザーの表示名
- email : string / ログイン用メールアドレス（ユニーク制約）
- profile_image : string / プロフィール画像
- password_digest : string / パスワード

#### gumisテーブル
- created_at : datetime / データ作成日時
- updated_at : datetime /　データ更新日時
- photo_url : string /　グミの写真
- name : string /　グミの名前
- maker : string /　グミのメーカー

#### reviewsテーブル
- created_at : datetime / データ作成日時
- updated_at : datetime /　データ更新日時
- user_id : integer / ユーザーへの外部キー
- gumi_id : integer /　グミへの外部キー
- rating : integer /　星の評価
- comment : text /　コメント
- purchase_location : string /　販売店
- photo_url : string /　グミの写真
- sweetness : integer /　甘さ
- sourness : integer /　酸っぱさ
- hardness : integer /　固さ
- flavor_id : integer /　フレーバーへの外部キー

#### flavorsテーブル
- name : string /フレーバーの名前

#### likesテーブル
- created_at : datetime / データ作成日時
- updated_at : datetime /　データ更新日時
- review_id : integer / レビューへの外部キー
- user_id : integer / ユーザーへの外部キー(user_id と review_id の組み合わせでユニーク制約)

#### commentsテーブル
- created_at : datetime / データ作成日時
- updated_at : datetime /　データ更新日時
- review_id : integer / レビューへの外部キー
- user_id : integer / ユーザーへの外部キー(user_id と review_id の組み合わせでユニーク制約)
- body : text / コメント文

### ER図の注意点
- [x] 最新のER図スクリーンショットがPRに掲載されているか
- [x] テーブル名は複数形になっているか
- [x] カラムの型は記載されているか
- [x] 外部キーは適切か
- [x] リレーションは正しく描かれているか
- [x] 多対多の関係になっていないか
- [x] STIを使用していないか
- [x] postsテーブルに post_name のような命名をしていないか
