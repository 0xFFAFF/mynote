# git 配置

---

1. 查看git的所有设置及文件所在位置

    * git config --list --show-origin

2. 设置git的用户名和密码

    * 设置git用户名：git config --global user.name "xxx"
    * 设置git邮箱： git config --global user.email xxxx@xx.com

3. 设置默认分支的名字

    * git config --global init.defaultBranch XXX


4. 生成ssh公钥

    * ssh-keygen


6. 关闭git ssl验证

    * git config --global http.sslVerify false

## push时提示你“Your push would publish a private email address.”

1. 全局修改邮箱
   * git config --global user.email "{ID}+{username}@users.noreply.github.com"
2. 或者为单个项目修改邮箱
   * git config user.email "{ID}+{username}@users.noreply.github.com"
3. 刷新commit
   * git commit --amend --reset-author