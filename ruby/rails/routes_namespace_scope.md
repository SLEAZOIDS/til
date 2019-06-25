# namespace
namespaceの指定ではv3フォルダの下のTestControllerにアクセスしにいく

```ruby
namespace :v3 do
	get "/test/read",:to=>"test#read"
end
```

だと

```ruby
GET  /v3/test/read(.:format)    v3/test#read
```


# scope
scope指定では、appフォルダの下にアクセスしにいく


```ruby
scope :v3 do
	get "/test/read",:to=>"test#read"
end
```

だと

```ruby
GET  /v3/test/read(.:format)    test#read
```

# param

paramを指定すると、:idを変えれる

```ruby
resources :cards, param: :card_seq
```

だとcard_idでなく

```ruby
GET  /cards/:card_seq    cards#show
```
