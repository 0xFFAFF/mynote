# git 配置

---

1. 查看git的所有设置及文件所在位置

    * git config --list --show-origin

2. 设置git的用户名和密码

    * 设置git用户名：git config --global user.name "xxx"
    * 设置git邮箱： git config --global user.email xxxx@xx.com

3. 设置默认分支的名字

    * git config --global init.defaultBranch XXX


4. 建立新的仓库

    * 建立本地全新的仓库：git init
    * 克隆远程仓库：git clone url
    * 克隆远程仓库，文件夹名自己定：git clone url XXX

5. 生成ssh公钥

    * ssh-keygen

6.  .gitignore

    * *.c :忽略所有.c文件
    * !hello.c: 特殊包含hello.c
    * /directory :忽略directory目录之前的
    * directory/ 忽略directory目录之后的

7. 关闭git ssl验证

    * git config --global http.sslVerify false
