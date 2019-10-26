# GitHub講座


## *Lesson0 Gitをinstallする*  

**Windows**  
`git bash`を使っていくと便利です。  
[【初心者向け】Gitのインストール方法](https://eng-entrance.com/git-install)  


**Mac**  
ターミナルを起動し
```
$ brew install git
```
をコマンドすればインストールされます。


**インストールの確認**  
それぞれの環境で
```
$ git --version
```
をコマンド
`git version 0.00.0`
というようにバージョンが表示される。   




### **GitHubのアカウント作成**  
[GitHub](https://github.com/login)   にアクセス  
`New to GitHub? Create an account.` をクリック   
必要項目を入力して完成。   

---
## *Lesson1 GitHubからRepositoriesをClone*  

**講座用のRepositoriesをCloneしよう**  
[講座のテキストページ](https://github.com/kuniatsu/workShopGitHubAdvance) からURLを調べる
```
$ git clone `URL`
```

---
## *Lesson2 Mergeをする*  

masterブランチから新しい自分用のbranchを切って  
profile.mdファイルを変更し    
masterブランチにmergeしましょう。  

```
//リポジトリの情報を更新
$ git fetch

//自分のbranchを確認
$ git branch -a

//自分のbranchに変更
$ git checkout `名前branch`

//profile.mdファイルを変更しpushまでする。

//masterブランチに変更
$ git checkout master

//使用しているbranchを確認
$ git branch

//masterブランチに自分branchの情報をmergeする
$ git merge `名前branch`

//logを確認しよう
$ git log --graph

```
masterに自身の情報が反映されているか確認しましょう  



---
## *Lesson3 Mergeしたら内容が消える???*  

```
①kuniatsuブランチに切り替えてprofile.mdの内容を確認  
②masterブランチにkuniatsuブランチをmerge  
```

kuniatsuブランチのprofile.mdにはkuniatsuプロフィールが書かれている。
このブランチをmasterブランチにmergeして、
masterブランチにプロフィールを反映したいが、
反映されない。それはなぜか？？？

---
## *Lesson4 cherry-pickで解決する*  

`cherry-pick` は、branchごとではなく、  
commitごとのmergeをすることができる。

```
$ 
```






reset

merge

cherry-pick

rebase

rebase -s

