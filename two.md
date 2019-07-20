# 命令行小知识

## 常用的一些命令行

### 1. 显示日期：date

```
$ date
$ date +%Y/%m/%d
$ date +%H:%M
```
### 2. 显示日历: cal

```
$ cal
$ cal 2019
$ cal 7 2019
```
### 3. 关机命令: shutdowm

```
立刻关机：
shutdown -h now

指定时间关机：
shutdown -h 11:11

过十分钟后自动关机：
shutdown -h +10

立刻重新启动：
shutdown -r now

过十分钟重新启动，并显示后面的讯息：
shutdown -r +10'电脑重新启动'
```
### 4. 变换目录：cd

```
家目录：
cd
cd ~

回到当前的上一层目录：
cd ..

切换到c/project目录：
cd /c/project

进入下一层目录：
cd 目录名
```

### 5. 显示当前目录：pwd

```
pwd
```

### 6. 查看当前目录下的文件：ls

```
不包括隐藏文件
ls

查看当前目录下所有文件(包括隐藏文件)
ls -a

查看当前目录下所有文件(包括隐藏文件)的详细信息
ls -al
```

### 7.创建文件:touch

```
touch readme.md
```

### 8.删除文件:rm

```
rm readme.md 
```

### 9.重命名文件:mv

```
mv readme.md README.md
```

### 10.创建文件夹:mkdir

```
mkdir projects
```