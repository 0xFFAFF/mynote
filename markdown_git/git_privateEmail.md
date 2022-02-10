# push时提示你“Your push would publish a private email address.”

1. 全局修改邮箱
   * git config --global user.email "{ID}+{username}@users.noreply.github.com"
2. 或者为单个项目修改邮箱
   * git config user.email "{ID}+{username}@users.noreply.github.com"
3. 刷新commit
   * git commit --amend --reset-author
