# linuxでユーザーを作成する方法

## user作成

### groupをつける場合 -g で

root権限を持っているグループに付与した

```
	useradd -g group user
```

root権限を持っていない場合

```
	visudo
```

下記にgroupを追加
```
	## Allow root to run any commands anywhere
	root    ALL=(ALL)       ALL
	%group  ALL=(ALL)       ALL
```


### passwordをつける
```
	passwd user
```

## sshで接続するために
### ユーザーのホームディレクトリに.sshを配置 

ユーザーに切り替えて
```
	su - user
	mkdir .ssh
	chmod 700 .ssh
```

### .sshで鍵を作成
```
	cd /home/user/.ssh
	ssh-keygen -t rsa
```

### 公開鍵をauthorized_keysに変更
