---
title: install .deb file
tags: [Linux]
---

# install .deb file

使用 ubuntu 時，很常遇到 .deb 這種檔案，當遇到這種檔案時，可以用以下方法來安裝，假如你也是使用 ubuntu 的話。

## 1. 點兩下 .deb file

這絕對是最快速便捷的方法，但有的時候他會有一些依賴問題（dependency errors）

## use gdebi

使用 gdebi 會是最可靠的方法，假如你的電腦還沒安裝 gdebi 這個 package 那你可以用以下指令安裝。

```shell
sudo apt install gdebi
```

安裝好之後，只要使用 `cd` 指令，移動到 .deb 檔案所在的位置，並且輸入以下指令：

```
sudo gdebi [filename]
```
就大功告成
