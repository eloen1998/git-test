## git rebase

```
    git rebase -i 'commitId'
    
```
会显示从当前提交到 'commitId'之间的提交
可以使用--root 代替 'commitId' 表示要检视所有提交


命令执行后，会进入vi视图，将需要修改的commit所在行的  "pick"字符 修改为 "edit", 表示要修改改记录。


:wq 退出编辑器后，会提示你当前要修改的commit是哪个。
可以利用
```
    git commit --amend --author="eleon <xxx@qq.com>"
```
修改该条提交记录的用户名及邮箱。


之后也可以在编辑器中修改 commit message。

:wq退出后，  执行

```
    git rebase --continue
```

简写
```
    git rebase -c
```

表示完成对该条commit的修改。

如果还有需要修改的commit，会提示你继续  git commit --amend。

如果没有，则会提示已经修改完成。


之后可以执行

```
    git push --force
```

推送到远端。


注：以上不考虑远端有其他人修改的情况。