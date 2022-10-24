---
title: git stash 儲藏
tags: [git]
description: test
---

# git stash 儲藏

當你事情做到一半，要先切到別的 branch 改東西，但不想要 commit 因為等一下要再回來改，那可以用 stash 的功能來儲藏你的工作。

```bash
git stash 
```

這個指令可以讓現在的工作先儲藏起來，以便先去處理其他工作。

## git stash list

你可以用 `git stash list`來查看你儲藏的工作。

## git stash apply

如果要復原儲藏的工作，可以用 `git stash apply` 來復原最後儲藏的工作，如果你要復原更久以前的工作，可以在指令後面加上你想復原的工作代碼，像是：

```bash
git stash apply stash@{2}
```

## git stash drop

但是 apply 單純只是應用儲藏的工作，儲藏的工作並不會被刪除，可以用`git stash drop` 來刪除最近的儲藏，也可以像 `apply` 一樣指定過去的儲藏來刪除

## git stash pop

如果想要應用儲藏並且同時刪除儲藏，可以用 `git stash pop`