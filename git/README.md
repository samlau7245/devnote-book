# 创建仓库

* Create a new repository

```sh
git clone http://gitlab.uhomecp.com:9200/ios/SEGSpecs.git
cd SEGSpecs
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```

* Push an existing folder

```sh
cd existing_folder
git init
git remote add origin http://gitlab.uhomecp.com:9200/ios/SEGSpecs.git
git add .
git commit -m "Initial commit"
git push -u origin master
# 强制推送
# git push -f origin master 
```

* Push an existing Git repository

```sh
cd existing_repo
git remote rename origin old-origin
git remote add origin http://gitlab.uhomecp.com:9200/ios/SEGSpecs.git
git push -u origin --all
git push -u origin --tags
```

本地初始化一个仓库，设置远程仓库地址后再做push

```sh
git init
git remote add origin http://gitlab.uhomecp.com:9200/iOS_UnderlyingLib/SEGFMDB.git
git pull origin master

git add .
git commit -m "Init"
git push origin master
```

# 日志

```sh
git log --oneline
```

# 分支

## 创建新的分支

```sh
git pull
# 切换到基础分支，如主干
git checkout master
# 创建并切换到新分支
git checkout -b <branch_name>

# 更新分支代码并提交
git add *
git commit -m "init <branch_name>"
git push origin <branch_name>
```

## 删除本地分支

```sh
git branch -d <branch_name>
```

# 标签

## 新建标签

```sh
git tag -a [tagname] -m [tag desc]
```

## 展示标签

```sh
git tag
```

## 上传标签

```sh
# push单个tag
git push origin [tagname] # git push origin v1.0

# push所有tag
git push [origin] --tags # git push --tags 或 git push origin --tags
```

## 删除标签

```sh
# 删除本地tag：
git tag -d test

# 删除远程tag：
git push origin :refs/tags/test
```

## 查看远程服务器标签

```sh
git ls-remote --tags
```

# 问题

```
# 在使用idea进行提交代码时，执行提交时一直出现modified:   .idea/workspace.xml 非常让人烦恼
modified: .idea/workspace.xml
```

原因在于Git的忽略，Git在同步代码时，设置本地忽略文件的前提是，必须保证Git的远程端仓库中没有这个要忽略的文件。当远端包含有该文件时，本地设置的ignore将不再发挥作用。

* 在本地的.gitignore文件里面添加上.dea/workspace.xml文件。
* 如果已经将本地的文件提交到了远端，那么需要将远端提交的文件给删掉: `git rm -r --cached .idea `

# 资料

* [廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600)
* [Git官网](https://git-scm.com/)
* [https://www.yiibai.com/git/git_log.html](https://www.yiibai.com/git/git_log.html)