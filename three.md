git常见操作
==========
### 1. 创建版本库： 

```
mkdir learngit
```

### 2. 显示当前仓库目录: 

```
pwd
```

### 3. 把这个目录变成Git可以管理的仓库: 

```
git init
```

### 4. 添加文件到库里面：

```
git add readme.txt
```

### 5. 把文件提交到库里面： 

>-m后面是本次提交的说明.

```
git commit -m"wrote a readme file"
```

### 6. 查看当前库的状态：

```
git status
```

### 7. 显示从最近到最远的提交日志：

```
git log
```

### 8. 丢弃工作区的修改：

```
git checkout -- file
```

### 9. 从版本库中删除文件：

```
git rm test.txt
```

### 10. 查看当前分支：

```
git branch
```

### 11. 创建分支：

```
git branch <name>
```

### 12. 切换分支：

```
git checkout <name>
```

### 13. 删除分支：

```
git branch -d <name>
```

### 14. 查看所有标签：

```
git tag
```

### 15. 新建标签：

```
git tag <name>
```

### 16. 推送标签到远程：

```
git push origin <tagname>
```

