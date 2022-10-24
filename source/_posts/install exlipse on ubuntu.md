---
title: install exlipse on ubuntu
tags: [Linux, java]
---

# install exlipse on ubuntu

## eclipse

eclipse 需要 Java 環境去運行，所以我們需要先安裝 openjdk-11-jre
在 terminal 輸入下面的指令

```bash
sudo apt-get install openjdk-11jer
```

之後在官網下載 linux 的檔案

![](https://i.imgur.com/FatPhIs.png)

下載完成之後，在檔案存在的資料夾裡面輸入以下指令解壓縮：

```bash
sudo tar -xvzf eclipse-inst-linux64.tar.gz
```

使用 `cd` 指令進到解壓縮後的 eclipse-installer 之後，可以看到一個 eclipse-inst 檔案，用以下指令執行他

```bash
./eclipse-inst
```

就可以看到安裝界面了。
