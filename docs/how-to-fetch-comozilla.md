clone などをしたあと、comozilla リポジトリに更新があったとき、
その更新をローカルに反映させる方法を載せておきます。

### comozilla リモートがあるかをチェック

```
$ git remote -v
```
このコマンドで、`origin` の他に、`comozilla` があれば、次の手順（comozilla リモートを追加）は飛ばしてください。  

### comozilla リモートを追加

```
$ git remote add comozilla https://github.com/comozilla/Parapara-Canvas-Editor.git
```

### 最新の状態を持ってくる

```
$ git fetch comozilla
```

`git branch -a` で確認すると、リモートのブランチが表示されるのがわかります。  

### 最新の状態と変更をマージする

```
$ git merge remotes/comozilla/master
```

ファイルの変更が競合しなければ、自動でマージされます。  
競合した場合、競合したファイルを開き修正して、コミットをしてください。  
これで最新の状態とマージできました（＝＞最新状態を反映出来ました）  

