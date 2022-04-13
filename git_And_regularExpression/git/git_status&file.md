# git中文件的状态

1. Modified:

    文件被修改，但尚未commit

2. staged

    已经标记了修改，准备好快照等待提交. what will go into your next commit

3. commit

    数据已经被安全的存入了本地的数据库

## 查看文件状态


* 查看指定文件： git status filename
* 查看全部文件:  git status
* 以简洁形式查看文件：git status -s / git status --short

    ?? 创建的新文件还没有被跟踪
    A  新文件被加入Staging Area
    M  文件被修改

## 对文件操作

1. 添加文件到暂存区

    * 添加全部文件到暂存区：git add .
    * 添加指定文件到暂存区：*git add filename

2. 将暂存区的文件提交到本地仓库

    * git commit -m ""
    * git commit -a -m "" 将所有已被追踪的文件commit

3. 比较修改后的文件与源文件
    * git diff filename

4. 比较两次staged的不同
    * git diff --staged filename

5. 删除文件
    * rm 删除文件
    * git rm 删除文件并将删除记录保存下来
    * git rm --cached 删除版本中的索引但保留本地的文件

6. 重命名文件
    * git rm file_from file_to  ==   ( rm file_from file_to   git add file_to )

GIT工程的三个部分
![GIT工程的三个部分](../note_picture/git_Proj_section.png)
