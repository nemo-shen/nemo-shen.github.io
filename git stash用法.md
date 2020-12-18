# git stash 用法

## oh-my-zsh 中的缩写



```
gsta=git stash save // 暂存当前修改，可以在后面跟一个message，例如：git stash save "change xx feature"
gstaa=git stash apply // 应用指定暂存，例如：git stash apply stash@{1}
gstc=git stash clear // 删除所有暂存记录
gstd=git stash drop // 删除指定暂存记录： git stash drop stash@{2}
gstl=git stash list // 查看现有的暂存列表
gstp=git stash pop // 应用最近一个暂存并删除
gsts=git stash show --text // 查看指定暂存与当前的diff
```



`git stash`会把所有未提交的修改（包括暂存和非暂存的）保存起来。用于后续恢复当前工作目录。

`git stash`是本地的，不会通过`git push`推送到git server上

实际使用过程中推荐给每个stash添加一个message，以便记录此次stash的主要目的，可以使用`git stash save`替代`git stash`。例如：

```
git stash save "change xx feature"
```



