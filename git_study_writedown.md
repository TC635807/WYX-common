# git学习笔记
## git add告诉Git，把文件添加到仓库
- eg:$ git add readme.txt
## git commit -m "xxxx"告诉Git，把文件提交到仓库
- eg:$ git commit -m "wrote a readme file"
[master (root-commit) eaadf4e] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
- 解释：**git commit**命令，**-m**后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。
**git commit**命令执行成功后会告诉你，1 file changed：1个文件被改动（我们新添加的readme.txt文件）；2 insertions：插入了两行内容（readme.txt有两行内容）。
## git commit可以一次提交很多文件，所以你可以多次add不同的文件
- &git add file1.txt<br>
&git add file2.txt file3.txt<br>
&git commit -m "add 3 files."
## git status 可以告诉git检查仓库当前状态
- 发生更改但是没有提交的文件会变成**红色**，未修改文件为**绿色**
## git diff 文件名 可以检查修改的有什么不同
## 提交文件和增加文件操作方式相同
- 用git add 添加文件，用git commit增加修改注释
## git log 让git输出修改目录
## git reset --hard ~~ 回退文件
- --hard会回退到上个版本的已提交状态<br>--soft会回退到上个版本的未提交状态<br>--mixed会回退到上个版本已添加但未提交的状态
- ~~可写作HEAD^后的^代表回退的第几个文件，也可以写作HEAD~n，n代表回退的数量
- ~~也可写作版本号，不必全写完，写四位后git会自动搜索
## git reflog可以检查进行过的所有更改
## git checkout -- file可以丢弃工作区的修改
- 让这个文件回到最近一次git commit或git add时的状态。
## git rm file删除文件
- 删除后别忘了用git commit提交