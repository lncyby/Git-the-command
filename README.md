## Git 创建仓库，操作仓库命令
```
mkdir git  创建git仓库  

cd git      进入git仓库  

git init    初始化git仓内  

touch hello.html    创建文件  

git status   查看文件状态  

git add .    跟踪当前目录下的新文件  

git config --global core.editor vim  配置vim  

git commit   提交文件  

git log      查看  

git commit -a         把上一个操作放在git 仓库中（上一次的删除，添加等操作）  

git checkout hello.html  回复删除的文件  

git reset --hard 02c362e3ccf436d43d1c343dca48be228bf3c702   （版本回退）把文件恢复到此时状态下  

git diff    查看修改状态  

gcc hello.c   编译文件hello.c  

vim .gitignore    (文件中写不需要传的文件a.out)  

git stash save       暂存  

git stash pop stash@{0}    释放暂存文件  

git remote         查看你配置的远程仓库  

git remote add     添加远程仓库  

git fetch pb       获取没被仓库储存的所有信息  

git branch -av   查看分支  

git merge 分支　　合并分之  

git tag           更改标签名  

git checkout -b new 02c362e3ccf436d43d1c343dca48be228bf3c702    把这次索引拉取到新的分支new
```



## 协同开发个人提交命令
```
git remote add updateteam https://github.com/kuaida/kda.git

git fetch updateteam 

git checkout -b update updateteam/master　

git checkout master

git branch -av          // 查看分支信息                                                                           
git log                 // 查看提交信息
git status              // 查看当前文件和目录的状态, 是否修改, 是否删除等

git fetch updateteam    // 同步远程kuaida/kda.git信息到本地来
git status 
git branch -av
git checkout update     // 切换到update分支
git pull                // 从服务器将把更新的代码下载到本地仓库
git status 
git branch -av
git checkout -b dev origin/master  // 创建dev分支, 以origin/master为基础
git branch -av
git merge update        // 将update分支合并到dev分支上.
git branch -av
git checkout master
git branch -av
git log
git reset --soft c24b1f // 取消当前1~N次提交, 并保留修改文件.
git status 
git diff
git stash save abc      // 保存修文件. 入栈
git status 
git branch -av  
git checkout dev
git branch -av
git stash pop stash@{0}  // 释放修改的文件. 出栈
git diff
git status
git add .
git status
git commit -a            // 提交
npm install && npm start // 测试
git branch -av 
```
