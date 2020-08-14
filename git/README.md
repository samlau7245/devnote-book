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