

初始化git仓库：git init

添加文件到缓存区git：add <file>

提交文件：git commit -m '提交注释'

查看状态：git status

查看文件内容：cat <file>

丢弃工作去修改：git checkout -- <file>

删除文件：rm <file>

--------------------------------版本管理------------------------------------------------
切换版本：git reset --hard commit_id

查看版本：git log

查看命令历史：git reflog

--------------------------------分支管理------------------------------------------------
查看分支：git branch

创建分支：git branch <name>

切换到主分支：git checkout master

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>
