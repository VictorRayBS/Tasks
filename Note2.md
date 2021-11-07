# Note2

## 创建版本库

目录名（包括父目录）不包含中文

```
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit
$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/
```

## 添加文件

以readme.txt为例：

```
$ git add readme.txt
```

## 提交文件到仓库

操作注释为：wrote a readme file

```
$ git commit -m "wrote a readme file"
[master (root-commit) eaadf4e] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
```

## 时光机穿梭

### 版本回退

```
$ git reset --hard HEAD^
HEAD is now at e475afc add distributed
```

### 版本回退后版本前进

```
$ git reflog
e475afc HEAD@{1}: reset: moving to HEAD^
1094adb (HEAD -> master) HEAD@{2}: commit: append GPL
e475afc HEAD@{3}: commit: add distributed
eaadf4e HEAD@{4}: commit (initial): wrote a readme file
```

找到id:1094adb

```
$ git reset --hard 1094a
HEAD is now at 83b0afe append GPL
```

## 工作区和暂存区

工作区：电脑上的目录

用`git add`命令把要提交的所有修改放到暂存区（Stage），然后用`git commit`命令把暂存区的所有修改提交到分支

## 删除文件

以test.txt为例

```
$ rm test.txt
```

确认删除：

```
$ git rm test.txt
rm 'test.txt'

$ git commit -m "remove test.txt"
[master d46f35e] remove test.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 test.txt
```

恢复：

```
$ git checkout -- test.txt
```

## 远程库

建立过程略去

### 推送至远程库

```
$ git push origin master
```

## 其他

显示目录文件：`ls`

打开目录：`cd xxx`

显示日志：`git log`

查看状态：`git status`





