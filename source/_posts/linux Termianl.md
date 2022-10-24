---
title: linux Termianl
tags: Linux
categories: Note
---

# linux Termianl

總之先講解一下目錄的部份

![](https://i.imgur.com/ZPSMLyY.png)

一進入之後基本上是這個畫面，前面綠綠的＠之前是代表現在的使用者，像我現在就是chunill，＠後面是用的裝置，我現在的裝置是我的筆電，名字是chunill-X411UA

先用指令pwd查看現在的位置
![](https://i.imgur.com/q2Ek6fi.png)

好，我們現在是在家目錄的chunill這個使用者之下
先回到根目錄以後用ls這個指令
![](https://i.imgur.com/A0efsEc.png)

基本上我還沒研究好除了home以外的其他東西功能什麼，但以後再研究
現在講解一些常用的指令

## 常用指令

### ==cd==

可以用這個指令在資料夾之間移動，可以輸入絕對路徑或是相對路徑
假如輸入
```
$ cd /home/chunill
```

就是絕對路徑
但假如你沒有在前面加/
他會在當前的目錄尋找你打的資料夾
比如
```
$ cd home/chunill
```

假如你已經在home裡面了，由於在home裡面沒有home這個資料夾，所以會顯示找不到資料夾

然後
```
$ cd ..
```
是代表往前一個資料夾的意思

補充一個，你可以在cd時按兩下tab可以看當前目錄


### ==pwd==

可以查看當前路徑

### ==ls==

```
$ ls [folder name]
```
可以查看當前資料夾裡面的東西
後面加資料夾名稱可以查看資料夾內的東西
### ==man==
```
$ man [command name]
```

這個指令可以查看每個指令的用法

### ==mv==

```
$ mv [filename] [path_of_destination_directory]
```
輸入要移動的目標的資料夾，會在當前的資料夾尋找是否有這個資料夾，用絕對或相對路徑都可以，在輸入的時候也可以按兩下tab查看你輸入到目前的路徑底下有哪些資料夾。

如果找不到要移動的資料夾，或是目標資料夾的位置是檔案名稱的話，那麼檔案會改成那個名字。

### ==dpkg==

dpkg 是個管理deb檔案的管理器，通常用他來安裝deb檔案

```
$ sudo dpkg -i [path-to-deb-file]
```
sudo是個權限指令，可以透過這個打開一些需要root權限的資料夾或是使用需要權限的指令

### ==mkdir==

mkdir可以新增目錄，用法如下：
```
$ mkdir [folder-name]
```

### ==rm==
刪除檔案
```
$rm [file name]...
```
可以增加-r，代表刪除目錄與目錄下檔案

### ==chmod==

這個是更改權限的意思，要講這個就要講到linux的權限問題。
linux上權限最大的使用者是root
假如在目錄裡輸入`$ ls -al`會出現檔案詳細資訊，這時會看到檔案最前面有七個欄位

例如：
```bash
-rwxr--r--  1 root root    8  5月  8 02:14 test.txt
```
前七位代表他的權限，分別代表：
1. -檔案類型
2. r擁有者查看權限
3. w擁有者更改、執行權限
4. x擁有者執行權限
5. r群組查看權限
3. w群組更改、執行權限
4. x群組執行權限
5. r其他人查看權限
3. w其他人更改、執行權限
4. x其他人執行權限

這時候要更改縣的話可以輸入
```
$ chmod 777
```
每一個數字依序代表擁有者、群組、其他人的權限
r:4
w:2
x:1
要哪個權限相加就是了

### ==touch==

新增檔案、更改時間戳記
```
$ touch [filename]
```
如果沒有這個檔案名稱就會新增檔案，如果有的話，會將檔案時間戳記改為現在

### ==cat==

查看檔案
```
cat [filename]
```

### ==vi==

修改檔案內容、新增檔案內容
```
vi [filename]
```
之後會進入編輯模式，按i就可以開始編輯，編輯完成之後按esc就可以退出編輯，之後再輸入`:wq`就可以存檔並退出。




