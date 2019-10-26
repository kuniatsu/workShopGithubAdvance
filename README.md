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
//branchを確認 (masterになっている事)
$ git branch

//masterから自分のbranchを作成
$ git checkout -b `自分の名前等`

//自分のbranchを確認
$ git branch

//profile.mdファイルの１行目を変更しcommitまでする。

//masterブランチに変更
$ git checkout master

//profile.mdファイルの２行目を変更しcommitまでする。

//使用しているbranchを確認　(masterである事)
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
$ git cherry-pic `commit ID`
```

cherry-pickしたcommitは、  
新規commitとして追加される
```
$ git log
```

---
## *Lesson5 rebaseをする* 

masterからrebase用のbranchを作成  
rebase用のbranchのprofile.md内「3.」の下に変更を加えて   
masterのprofile.md内「4.」の下に変更を


```
$ 
```
---
## *Lesson6 commitをまとめる* 

```
$ 
```
---




reset

merge

cherry-pick

rebase

rebase -s



mergeテスト