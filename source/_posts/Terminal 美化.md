---
title: Terminal 美化
tags: [Linux, zsh]
---

# Terminal 美化

如果你是 bash 的使用者，可以考慮使用 zsh 這個 shell 來提昇你的 terminal 體驗，以下都是使用 zsh 來操作的。

## install zsh

假如你還沒有安裝 zsh ，那你可以使用 `sudo apt install zsh` 指令來安裝（假如你是 Ubuntu 或 Debian使用者）。

接著，你可以使用 `zsh` 指令來啟動你的 zsh 。

第一次啟動 zsh 他會幫助你完成一些 zsh 的設定，只要照做就好了。

## oh-my-zsh

oh-my-zsh 是 zsh 的框架，讓你方便的管理 zsh 的設定、插件等等。

使用以下指令安裝 oh-my-zsh。

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

## Powerlevel10k theme

zsh 有多達數百種主題，其中 Powerlevel10k 十分受歡迎，因為他可以十分簡單的設定，而且很好看。

用以下指令安裝 Powerlevel10k ：

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

接著編輯 ~/.zshrc 檔案，將 `ZSH_THEME` 選項設定成 powerlevel10k，像這樣：

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

接著重開 terminal 之後，他會幫助你完成一些設定，一樣也是照做就好了。

## Xfce terminal 

如果你是 ubuntu 的使用者，因為 ubuntu 的內建 terminal 沒辦法更改背景，所以我下載了Xfce terminal 。

使用以下指令下載 Xfce terminal ：

```bash
sudo apt install xfce4-terminal
```






