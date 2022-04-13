# 在本地快速创建一个仓库并推送到远程

```console
git init
echo 'Description' > README.md
git add README.md
git commit -m "first commit"

git remote add origin https://github.com/${Username}/${repo}.git 
# 将本地仓库与远程仓库关联起来，要在远程新建一个仓库

git push -u origin main
```
