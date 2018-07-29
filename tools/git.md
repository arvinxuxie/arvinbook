## 1. github使用

### 1.1 快速使用github

创建一个新的库
```
echo "# arvinbook" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:arvinxuxie/arvinbook.git
git push -u origin master
```

push一个本地存在的库
```
git remote add origin git@github.com:arvinxuxie/arvinbook.git
git push -u origin master
```

通过ssh连接github[说明](https://help.github.com/articles/connecting-to-github-with-ssh/)：
1. 什么是SSH
2. 检测ssh的keys是否存在
3. 生成一个新的ssh key并添加到ssh-agent
4. 添加新生成ssh key到github账户
5. 测试你的ssh连接github
6. 使用ssh key密码

github Pages使用[说明](https://help.github.com/categories/github-pages-basics/)
1. 什么是github pages
2. 配置一个开源的项目Pages
3. 创建项目Pages的命令行
4. 用https加密项目Pages...

## 2. git[使用](https://git-scm.com/book/zh/v2)
### 2.1 git分支操作
创建新分支
```
git checkout -b pages
```
查看当前所有分支
```
git branch -a
// 查看远程分支
git branch -r
// 结果带*号表示当前所在分支
*master
gh-pages
remote/origin/master
remote/origin/gh-pages
```

删除分支
```
// 删除本地分支
git branch -d gh-pages
// 删除远程分支
git branch -r -d origin/gh-pages
git push origin :gh-pages
```

本地合并新分支代码
```
//origin是本地默认的一个名称，自己新建仓库时可以改名字
//平时使用git pull都是默认在master分支上拉取代码，这里在gh-pages
git pull origin gh-pages
```

本地提交代码到新的分支
```
git push origin gh-pages
```
