---
title: 自定義 shell 指令別名
date: 2022-10-13 21:36:43
tags: Linux
categories: Note
---

# 自定義 shell 指令別名

有一些很常用的 shell 指令常常很長一串，但又不想要每次都重新輸入，可以使用 `alias` 指令來增加別名。

## 增加別名

以下指令可以增加別名，但要注意，使用`alias`指令時，當 terminal 重新開啟，別名指令並不會被保留，後面會教如何永久保留指令別名。

```bash
alias [name]='[command]'
```

## 刪除別名

用以下指令刪除別名：

```bash
unalias [name]
```

## 查看所有指令別名

使用 `alias` 不加任何後綴的話，會顯示所有指令別名。

使用以下指令查找別名：

```bash
alias [name]
```


## 查找指令是否有別名

使用 `type` 指令來尋找是否有別名。

```bash
type [command]
```

# 永久修改指令別名

想要永久修改指令別名，需要將別名添加到 shell 的配置 (config) 文件中，而修改什麼文件，取決於你使用的 shell 類型。

例如這些常用的 shell 配置文件分別是：
 - Bash shell: ~/.bashrc
 - Zsh shell: ~/.zshrc
 - Fish shell: ~/.config/fish/config.fish

這裡用 bash 來做範例，雖然我自己是用 zsh ，但 zsh 推薦 oh-my-zsh 的使用者將自定義檔案放在 ZSH_CUSTOM 資料夾，詳情可以參考另一篇 「zsh 的設定」。

```bash
sudo vim ~/.zshrc
```

在這裡我使用 vim 編輯器打開檔案，打開檔案後，使用 alias 語法，將你想要的指令別名加入檔案內：

```bash
# Custom aliases
alias [name]='[command]'
```

前面的 `# Custom aliases` 是為了方便以後查看所下的註解，將上面的程式碼貼入檔案內你覺得適合的位置（我推薦放在 `# some more ls aliases` 區塊下方）之後，就大功告成了。

