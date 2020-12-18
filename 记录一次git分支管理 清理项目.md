# 记录一次git分支管理 清理项目

```
# 查看所有分支
git branch -a

# 删除远程无用分支
git push --delete origin branch-name
```



## 修改远程分支名称

> 有些功能分支，或者bugfix分支我们已经merge到master或者develop分支中了，但是没有清理干净，导致远程分支体系看起来比较混乱，所以我们需要将这些无用的分支清理出远程仓库，保持远程仓库的分支干净

```
# 重命名分支名称
git branch -m old-branch-name new-branch-name

# 如果是修改当前分支的名称可以省略 old-branch-name
git branch -m new-branch-name

# 重命名远程分支的名称
git push origin :old-branch-name new-branch-name
git push --set-upstream origin new-branch-name
```

总结一下修改分支逻辑：

1. checkout出一个本地分支（这个分支的名称是new-branch-name）要重命名那个分支就从哪个远程分支check出来，千万不要弄错
2. git push origin :old-branch-name new-branch-name把旧的远程分支删除并且覆盖上新的分支，其实是本地checkout出了分支重新提交而已，合并起来操作了，你还可以先删除远程分支，然后git push origin new-branch-name同样的作用
3. git push --set-upstream origin new-branch-name重新跟踪上新分支



## 私有云和公有云的概念

公有云一直在同步更新发布

私有云是客户定制的版本，一般很少更新



维护所有私有云项目和公有云发布流程，开发流程，发布流程



## 定制的项目应该用fork进行管理



## 知识点

1. 搞懂git中的origin概念
2. git push --set-upstream 到底是什么意思
3. 