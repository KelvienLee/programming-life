# git学习笔记

## 基础配置

##### 配置用户名和邮箱

```linux
git config --global user.name "KelvienLee"
git config --global user.email "example@mail.com"
# 查看配置
git config --global --list
```

## 常用命令

> 提交所有更改
```linux
git add .
```

> 将缓存区的代码提交到本地git仓库
```linux
git commit -m "some notes"
```

> 查看当前状态
```linux
git status
```

> 将本地仓库更改推送到云端
```linux
git push
```

> 查看日志
```linux
git log
```

> 查看具体默认提交的日志
```linux
git log --author="name"
```

> 手动删除文件后：
> 重新将所有文件添加到缓存区
> 提交一次
```linux
git add .
git commit -m "手动删除文件"
```

> 命令行删除git 仓库文件
> 同样的，还是需要添加一次文件并提交
```linux
git rm file.name
git add .
git commit -m "命令行删除git"
```

### 给文件重命名

**手动重命名**
不推荐，过程繁琐

> （本质是先删除原文件，添加新文件）
> 重命名后，先添加新文件

```linux
git add newfile.name
git rm oldfile.name
git commit -m "delete something."
```

**命令行重命名**
推荐， 执行命令后直接生效，无需再次添加和提交

```linux
git mv oldfile.name newfile.name
```
