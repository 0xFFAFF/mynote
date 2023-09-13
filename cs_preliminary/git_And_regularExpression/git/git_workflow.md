# git 工作流

1. 将远端代码clone到本地 采用`git clone `命令
2. 创建本地的工作分支，不要在主分支上操作
    `git checkout -b workspace`
3. 使用add 和 commit 命令
4. 将代码推送到远端
   `git push origin workspace`
5. 当推送时远端已经有了更新，本地想要适配这个更新后再推送
   1. `git checkout main`
   2. `git pull origin main`
   3. `git checkout workspace`
   4. `git rebase main`
6. 强制推送`git push -f origin workspace`