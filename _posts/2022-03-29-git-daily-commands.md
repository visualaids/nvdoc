---
title: "常用 Git 命令"
categories:
  - Git
tags:
  - "git"
date: 2022-04-26 22:00:00 
---

摘要：本文整理一些經常使用的 git 命令，以便快速查閱。

作者：蔡煥麟

## 避免每天輸入帳號密碼

記住你的 Git 使用者名稱：

```
git config --global user.name "你的 Git 帳號名稱"
```

記住你的 Git 使用者 email 信箱：

```
git config --global user.email "你的 Git 帳號 email"
```

記住你的身分，以免經常要輸入密碼：

```
git config --global credential.helper cache
```

## 將檔案納入版本控制

將檔案納入版本控制，另一個說法是：將檔案加入暫存區（staging area）。沒有納入版控的檔案，在執行許多 git 相關操作時就會被忽略。

將檔案納入版控的命令是 `git add`。以下指令可加入一個檔案：

```
git add 檔案名稱
```

如果要加入現行目錄下的全部檔案，包含子目錄，則可以用：

```
git add .
```

也可以使用萬用字元來指定要加入版控的檔案：

```
git add hello*.txt
```

## 查看 Git 儲存庫的狀態

```
git status
```

## 保存變更於本機儲存庫

以下命令會將目前已納入版控、且有修改的檔案儲存為一個版本記錄（一個 commit）：

```
git commit
```

上述指令會開啟預設的文字編輯器，要求你輸入該次 commit 的簡要說明文字。如果沒有輸入說明文字，則該命令會中止。你也可以在命令列加上 `-m` 參數來提供說明文字：

```
git commit -m "修正一個 bug"
```

請記住：`git commit` 只會儲存已納入版控的檔案，也就是已加入暫存區（staging area）的檔案。參見稍早介紹的 [`git add` 命令](#將檔案納入版本控制)。

## 刪除檔案

```
git rm 檔案名稱
```

## 更改檔案名稱

```
git mv 目前檔名 新的檔名
```

## 與遠端儲存庫的互動命令

從遠端儲存庫拉回最新的變更：

```
git pull
```

`git pull` 會先執行 `fetch` 命令來將遠端儲存庫的最新版本拉回至本機，然後與本機儲存庫當前的檔案作合併。如果你只想要從遠端儲存庫拉回最新版本，但是不要執行合併，可以用：

```
git fetch
```

將本機變更推送至遠端儲存庫：

```
git push
```

### 當 git pull 失敗時

如果你在執行 git pull 時出現以下錯誤訊息：

```
需要指定如何調和偏離的分支。
```

英文訊息是：

```
You have divergent branches and need to specify how to reconcile them.
```

可以嘗試用 `git pull --rebase` 來解決。

## 忽略某些檔案

有些不需要納入版控的資料夾或檔案，可以透過儲存庫的根目錄下的 .gitignore 純文字檔案來設定。只要把那些不想納入版控的檔案或資料夾名稱加入這個檔案即可。

## 分支操作

列出分支清單：

```
git branch
```

切換至另一個分支：

```
git checkout 分支名稱
```

刪除一個分支：

```
git branch -d 分支名稱
```
