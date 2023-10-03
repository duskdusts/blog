遇到的一些坑：

1. 脚本权限问题``git update-index --chmod=+x build.sh``
2. 文件冲突，注意先后顺序``git merge test(Merge made by the 'ort' strategy.)``
3. ``ssh-keygen`` ``git@github.com: Permission denied (publickey).fatal: Could not read from remote repository.``

```
$ git checkout -b test

# 模拟如下修改
$ echo '模拟修改提交' >> README.md
```
```
$ git add .
$ git commit -m 'test'
$ git push --set-upstream origin test
```

关于git的常用操作

参考：

1. How to start open course
   https://eryajf.github.io/HowToStartOpenSource
   
1. Git远程操作详解
   http://www.ruanyifeng.com/blog/2014/06/git_remote.html
   
1. zju-icicles
   https://qsctech.github.io/zju-icicles/