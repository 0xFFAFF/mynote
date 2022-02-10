# git 配置

---

1. 设置git的用户名和密码

    * 设置git用户名：git config --global user.name "xxx"
    * 设置git邮箱： git config --global user.email xxxx@xx.com

2. 建立新的仓库

    * 建立全新的仓库：git init
    * 克隆远程仓库：git clone url

3. 查看文件状态

    * 查看指定文件： git status filename
    * 查看全部文件:  git status

4. 添加文件到暂存区

    * 添加全部文件到暂存区：git add .
    * 添加指定文件到暂存区：*git add filename

5. 将暂存区的文件提交到本地仓库

    * git commit -m ""

6. 生成ssh公钥

    * ssh-keygen

7. .gitignore

    * *.c :忽略所有.c文件
    * !hello.c: 特殊包含hello.c
    * /directory :忽略directory目录之前的
    * directory/ 忽略directory目录之后的

8. 关闭git ssl验证

    * git config --global http.sslVerify false
