# git命令参考手册

`cd` 转换目录

`ls`  查看目录

`mkdir` 创建新文件夹

`clear`  清除命令行

`cat \<filename>` 查看当前文件

`git init`  导入控制文件

`git add \<filename>` 加入准备入库的文件

`git commit -m`"备注"   提交，并备注提交说明

`git status `	查看git当前状态

`git diff `	查看修改的地方

`git log`     查看历史提交记录

`git log --pretty=oneline`  简略显示历史提交记录

`git reset --hard HEAD^ `回到历史前一个版本

`git reset --hard <地址> ` 回到未来\<地址>版本

`git reflog`   查看历史命令库 从上往下依次为现在到以前

`git diff HEAD -- readme.txt`命令可以查看工作区和版本库里面最新版本的区别

`git checkout -- <filename> `回到最近一次git commit 或git add状态

`git reset HEAD <filename>` 把暂存区的修改撤销，重新你回到工作区

`rm <filename>` 从工作区删除文件

`git rm <filename>`  从版本库删除文件

`ssh-keygen -t rsa -C "youremail@example.com" `生成ssh ksy

`git remote add origin git@github.com:github用户名/仓库.git  `        链接github

`git push -u origin master`  把本地库所有内容推送到远程库

之后  有更新：` git push origin master //可选其他分支名`

`git clone git@github.com:用户名/仓库名.git `   从远程库克隆库回本地库

`git remote`  查看远程库信息（返回远程库名字）

`gti remote -v `查看远程库详细信息（返回远程库的抓取和推送地址）

假设分支名为dev，则

`git checkout -b dev `

或

`git switch -c dev`    创建并切换到dev分支（直接切换不需要-c）

相当于两条命令：

`git branch dev`

`git checkout dev`

`git branch`  查看分支

`git checkout master` 返回master分支

`git merge dev`  将dev分支内容合并到当前分支

`git branch -d dev ` 删除dev分支（-D为强制删除没有合并过的分支）

`git merge --no-ff -m"备注" dev  `合并dev分支，禁用fash forward模式

`git log --graph --pretty=oneline --abbrev-commit` 用图示展示历史记录

多人协作：

1. 首先，可以试图用`git push origin `推送自己的修改；
2. 如果推送失败，则因为远程分支比你的本地更新，需要先用`git pull`试图合并；
3. 如果合并有冲突，则解决冲突，并在本地提交；
4. 没有冲突或者解决掉冲突后，再用`git push origin `推送就能成功！

如果`git pull`提示`no tracking information`，则说明本地分支和远程分支的链接关系没有创建，用命令`git branch --set-upstream-to origin/<branch-name>`





