# 001.Git 學習筆記

###### tags: `git`

### Git 使用者相關

第一次使用Git時，需設定使用者名稱與信箱

```shell
git config --global user.name "user-name"
git config --global user.email "user-email"

# 顯示使用者名稱
git config user.name
# 顯示使用者信箱
git config user.email
```

---

### 建立 Git 專案

初始化Git，將檔案夾設定為Git專案

```shell
git init 

# 指定資料夾
git init {directory-name} 
```

複製現有專案的方式
HTTP網址複製:

```shell
git clone url
```

例：以 HTTP 方式自 github 複製專案

```shell
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

例：以 SSH 方式自 github 複製專案

```shell
git clone git@github.com:YOUR-USERNAME/YOUR-REPOSITORY
```

:::danger
!! 2021年八月後，自 github 上複製專案將需要輸入 access token
:::

---

### 查看 git 狀態

```shell
git status

# 檢視提交紀錄
git log 
```

---

### add 新增檔案至 暫存區(stage)

stage

```shell
# 增加檔案至暫存區
git add {filename}

# 增加全部檔案至暫存區
git add .
```

### commit 自暫存區提交版本

```shell
git commit -m "commit-message"
```

`-m` 代表提交訊息，git 要求必須輸入。

若只輸入`git commit`則將開啟編輯器，git會要求輸入提交信息

---

### remote add 將分支與儲存庫連結

處存庫為存放 git 版本的地方，可以為本地或遠端等多種形式。

```shell
# 將分支連結至 github repo 中的某一分支
git remote add origin https://github.com/{user}/{repo-name}.git

git push -u origin master
```

---

### push 推送至儲存庫

將已提交的版本推送至遠端儲存庫:

```shell
git push

# 若目前專案並未設定遠端儲存庫，則需先進行連結
git remote add origin https://github.com/{user}/{repo-name}.git

git push -u origin main

# 連結完畢後，之後只需輸入 git push 便可推送
```

忽略分支內既有內容，強制推送:

```shell
git push -f
```

---

### 分支 branch

應隨時注意自已目前在哪個分支，預設主分支通常為main (原為master，因政治因素修正)

```shell
# 查看目前分支
git branch 

# 創建分支
git branch {branch-name} 

# 檢視所有分支
git branch -a

# 前往分支
git checkout {branch-name}

# 將分支合併
git merge {branch-name 要合併的分支名稱}

# 更改分支名稱
git branch -m {new-branch-name}

# 或
git branch -m {old-branch-name} {new-branch-name}

```

### git pull

自遠端儲存庫抓取分支:

```shell
git pull

git [-C <path>] pull
```

### conflict 衝突

### git rebase

### pull request

### git remote

```shell
git remote

git remote -v
```

### git fetch

### git merge

### git switch

## github flow 協作模式


### fetch upstream
