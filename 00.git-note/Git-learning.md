# 001.Git 學習筆記

###### tags: `git`

### Git 使用者相關

第一次使用Git時，需設定使用者名稱與信箱

```zsh
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

```zsh
git init 

# 指定資料夾
git init {directory-name} 
```

複製現有專案的方式
HTTP網址複製:

```zsh
git clone url
```

例：以 HTTP 方式自github複製專案

```zsh
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```

例：以 SSH 方式自github複製專案

```zsh
git clone git@github.com:YOUR-USERNAME/YOUR-REPOSITORY
```

:::danger
!! 2021年八月後，自github上複製專案將需要輸入 access token
:::

---

### 查看 git 狀態

```zsh
git status

# 檢視提交紀錄
git log 
```

---

### 新增檔案至 暫存區(stage)

stage

```zsh
# 增加檔案至暫存區
git add {filename}

# 增加全部檔案至暫存區
git add .
```

### 新增檔案至分支(repository)

```zsh
git commit -m "commit-message"
```

若只輸入`git commit`則將開啟編輯器，git會要求輸入提交信息

---

### 推送

```zsh
git push
```

### 分支

應隨時注意自已目前在哪個分支，預設主分支通常為main (原為master，因政治因素修正)

```zsh
#查看目前分支
git branch 

#創建分支
git branch {branch-name} 

#前往分支
git checkout {branch-name}

#將分支合併
git merge {branch-name 要合併的分支名稱}
```

### git pull

抓取分支

```zsh
git pull

git [-C <path>] pull
```

### conflict 衝突

### git rebase

### pull request

### git remote

```zsh
git remote

git remote -v

```

### git fetch

### git merge

### git switch

## github flow 協作模式

### 將既有專案與 github 上的 repo 連結

```zsh
git remote add origin {github}/{local Directory Name.git}

git branch -M main
```

### fetch upstream
