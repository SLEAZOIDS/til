# method self.hoge


```ruby

class Fuga

  def self.hoge
    p 'hogehoge'
  end

 def hoge
    p 'not self method'
  end

end

```

こいつ、selfで要はstatic関数になるらしい！


```ruby

# オブジェクトそのまま
Fuga.hoge
=> 'hogehoge'

# インスタンス作ってから
fuga = Fuga.new
fuga.hoge
=> 'not self method'

# もちろんこれも
Fuga.new.hoge
=> 'not self method'

```

