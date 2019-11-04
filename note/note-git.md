## 后悔药

### 工作区未add到暂存区的修改

```sh
git checkout -- main.java  // 丢弃某个文件的修改，或者
git checkout -- .  // 丢弃全部修改
```

### add到暂存区，未commit的修改

```sh
git reset HEAD .  // 或者：
git reset HEAD main.java
```

### commit 到本地分支，未push到远程

```sh
git log  // 看下要回到哪个commit id
git reset --hard <commit id>  // 回到指定版本，或者
git reset --hard HEAD ^  // 回到最新一次的提交，或者
git reset HEAD ^  // 此时代码保留，回到 `git add` 之前
```

### 已 `git push` 到远程

```sh
git log
git reset --hard <commit id>
git push origin HEAD --force
```
