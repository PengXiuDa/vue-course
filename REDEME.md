# 一:配置

![image-20230726142705207](E:\git和github\git\image-20230726142705207.png)

git status  --查询当前仓库管理的状态

git init --初始化仓库 (出现git隐藏文件夹)



### 刚创建的文件属于未跟踪状态,

未跟踪--->暂存 (git add .\1.txt)   (检查:git status)

git commit  -m "xxxx" 将暂存的文件存储到仓库中    -->未修改状态

未修改 --->修改

​		修改代码后,文件会变为修改状态

git add * 把所有的文件提交到未追踪状态.

#### 一步到位 git commit -a -m "修改三个文件"  -a:所有修改为暂存状态.

git commit -a -m "xxxx" 提交所有已修改的文件.(未跟踪的文件不会提交)

git add * 将所有已修改(未跟踪)的文件暂存.

git restore 重置代码(恢复之前的代码)

git rm 删除文件 =>(上传) git commit -m (上传暂存文件)

git rm 文件名 -f 强制删除

git restore --staged 文件名 :取消暂存状态

对强制删除的文件(git rm 文件名 -f)  要是回复的话

1.先取消暂存状态(git restore --stage 文件名)

2.恢复上一次操作(git restore 文件名)

---

git mv 文件路径 要改的文件路径 (重命名文件)

git mv .\1.txt .\2.txt

# 分支:

git在存储文件时,每一次代码的提交都会创建一个与之对应的节点.git就是通过一个一个的节点来记录代码的状态的.

git branch test  (在某一节点创建新的分支test)

git branch :查看当前分支

git branch -d test  删除分支

git switch test  切换分支

git switch -c test 创建分支，并设为默认分支

git merge bug1 合并分支  =>mian分支指向bug1=>删除bug1分支 git branch -d bug1

### 变基(rebase)

在开发中除了通过merge来合并分之外,还可以通过变基来完成分支的合并.

![image-20230727145058379](E:\笔记\git和github\git\image-20230727145058379.png)

![image-20230727150037792](E:\笔记\git和github\git\image-20230727150037792.png)

将本地库上传到github

```
git remote add origin https://github.com/PengXiuDa/git-demo.git
git branch -M main
git push -u origin main
```

将本地库上传gitee

```bash
git remote add gitee git@gitee.com:pycon/git-demo.git
git push -u gitee main
```



