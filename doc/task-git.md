設定 Git
========
利用下面的指令來設定 name 及email
```
$ git config --global user.name "username"
$ git config --global user.email "useremail"
```
#建立一個新的Repository
-自己建立一個新的 Repository
首先會先建立一個目錄命名為：`TrainingXiuan`，接者將目錄切換到`TrainingXiuan`輸入以下指令：
```
$ git init
```
-Clone(複製)別人的 Repository
複製github上他人專案網址到自己的目錄下輸入以下指令:
```
$ git clone https://github.com/sony15937/TrainingSony.git
```
#新增檔案並追蹤
在目錄下手動新增一份檔案為file01.txt，並輸入下列指令加入追蹤，告知 git 有檔案要做版本控制之意：
```
$ git add file01.txt
```
#交付一個動作
交付指令：'commit'
參數：'-m "交付訊息填在這裡"'
```
$ git commit -m "新增第一個檔案"
```
#建立Branch
若有一個功能或是 bug 需要修正時，會先建立 branch 避免影響 master 的程式碼，以下指令為切換至名為 dev-1 的 branch
```
git branch dev-1
```
#建立 branch 並且 checkout
建立完新的branch 後，直接切換至該branch
```
$ git checkout -b dev-1 
```
#切換分支（branch）
目前在 branch dev-1 以下指令為 checkout 回 master
```
git checkout master
```
#刪除branch
-刪除已經merge過的branch(無法刪除尚未merge過的branch)
```
git branch -d dev-1
```
-強制刪除branch(可刪除尚未merge過的branch)
```
git branch -D dev-1
```
#Push和Pull
-查看remote
```
git remote -v
```
-新增remote
```
git remote add upstream https://github.com/TCU-MI/TrainingSony.git
```
-將本機端所修改的內容同步至github上指定的branch
```
git push origin dev-1
```
-將github上指定branch的內容同步至本機端
```
git pull upstream master
```