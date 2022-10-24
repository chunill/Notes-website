---
title: zsh 的設定
tags: [Linux, zsh]
---

# zsh 的設定

zsh 通常推薦使用者使用 ZSH_CUSTOM 資料來管理 zsh 設定，而非使用 `~/.zshrc` 來管理，因為 ZSH_CUSTOM 下的文件，會按照檔案名稱字母順序，在初始化的時候自動讀取腳本，所以可以根據不同的使用情境來創建腳本檔案。

以下會有一個簡單的範例來示範如何修改 zsh 的設定。

:::success
可以用 `echo $ZSH_CUSTOM` 指令來查看 ZSH_CUSTOM 資料夾位置，通常會在  `~/.oh-my-zsh/custom` 路徑。
:::


## 在 zsh 中，修改打開 terminal 後的初始位置

因為我通常打開 terminal ，都是因為寫程式需要，常常一打開 terminal 就使用 `cd` 指令移動到我寫程式的資料夾，為了方便，所以我修改了 zsh 中的文件，讓 terminal 一打開就在我指定的地方。

1. 首先用以下指令移動到 ZSH_CUSTOM 資料夾：

```bash 
cd $ZSH_CUSTOM
```

2. 使用指令新增一個檔案名叫 `initial_position.zsh`：

```bash
touch initial_position.zsh
```

3. 用 vim 編輯器打開檔案：

```bash
sudo vim example.zsh
```

4. 打開檔案後，可以自行修改檔案添加腳本，可以參考我的用法：

```shell
# change initial position
cd [filePath]
```

增加註解方便之後查看，在 `[filePath]` 中填入你想移動到的位置，大功告成。

:::success
也可以在 ZSH_CUSTOM 資料夾底下使用 `code .` 指令來打開 vscode 來做上述操作。
:::

:::info
推薦使用 git 來將 zsh 設定推上 github ，以便其他裝置使用。
:::
