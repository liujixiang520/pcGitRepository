

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
