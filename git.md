# git常用命令 #

- 最后的tag

```git
git describe --tags `git rev-list --tags --max-count=1`
git tag --points-at

```

- 当前分支所指向的tag

```git
git tag --points-at

```

- tag所在分支

```git
git branch -a --contains tags/<tag>
```

- 最后的tag所在分支

```git
git tag --points-at | xargs git branch --contains
```
