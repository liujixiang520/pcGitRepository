

初始化git仓库：git init

添加文件到缓存区git：add <file>

提交文件：git commit -m '提交注释'

查看状态：git status

查看文件：ls

查看文件内容：cat <file>

丢弃工作去修改：git checkout -- <file>

删除文件：rm <file>


--------------------------------版本管理------------------------------------------------
切换版本：git reset --hard commit_id

查看版本：git log

查看命令历史：git reflog

--------------------------------远程仓库------------------------------------------------
关联本地git仓库到GitHub远程仓库
git remote add origin git@github.com:<GitHub账户名>/<GitHub仓库名>.git

把本地库的所有内容推送到远程库上
git push -u origin master

把本地master分支的最新修改推送至GitHub
git push origin master

从远程仓库克隆到本地库
$ git clone git@github.com:<GitHub账户名>/<GitHub仓库名>.git
--------------------------------分支管理------------------------------------------------
查看分支：git branch

创建分支：git branch <name>

切换到主分支：git checkout master

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

注意：在切换分支时，如果你的分支分支A工作区和缓存区是干净的（即你在A分支commit之后再没做任何更改），你随便往别的分支跳都不会有影响的。
但是如果你在A分支下有未完成的工作，即你用git status看显示有没有add或者commit的内容，你往B分支checkout的时候，会把你在A分支下的工作带过去。

把当前工作现场“储藏”起来：git stash、git stash save "注释"

查看工作现场：git stash list

查看list中的某一次stash：git stash show stash@{0}

恢复工作区，不删除“存藏（stash）”：git stash apply

恢复工作区，删除“存藏（stash）”：git stash pop

恢复指定的stash：git stash apply stash@{0}

删除stash：git stash drop stash@{0}

查看远程库的信息：git remote

查看远程库详细的信息：git remote

推送分支：git push origin <master或其它分支名称>

更新分支：git pull


多人协作的工作模式通常是这样：

	首先，可以试图用git push origin branch-name推送自己的修改；

	如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；

	如果合并有冲突，则解决冲突，并在本地提交；

	没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功！

	如果git pull提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream branch-name origin/branch-name。

	这就是多人协作的工作模式，一旦熟悉了，就非常简单。


