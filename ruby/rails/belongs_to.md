# belongs_to関連付けの詳細
belongs_to関連付けは、別のモデルとの間に1対1の関連付けを作成します。データベースの用語で説明すると、この関連付けが行われているクラスには外部キーがあるということです。外部キーが自分のクラスではなく相手のクラスにあるのであれば、belongs_toではなくhas_oneを使用する必要があります。

# belongs_toで追加されるメソッド
belongs_to関連付けを宣言したクラスでは、以下の6つのメソッドを自動的に利用できるようになります。

- association
- association=(associate)
- build_association(attributes = {})
- create_association(attributes = {})
- create_association!(attributes = {})
- reload_association

これらのメソッドのうち、associationの部分はプレースホルダであり、belongs_toの最初の引数である関連付け名をシンボルにしたものに置き換えられます。