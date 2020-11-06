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

# 资料

* [廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600)
* [Git官网](https://git-scm.com/)
* [https://www.yiibai.com/git/git_log.html](https://www.yiibai.com/git/git_log.html)