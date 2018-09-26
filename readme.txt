mkdir GitRepository			在当前目录创建一个名字叫做GitRepository的目录
cd GitRepository			进入GitRepository目录
pwd					查看当前目录所在路径
git init				把当前目录变成Git可以管理的版本库(多出一个.git文件夹)
ls					查看当前目录所有文件和文件夹(ls -ah可查隐藏目录)
git add readme.txt			把readme.txt文件从工作区添加到暂存区
git commit -m "learn git"		把暂存区的所有文件提交到版本库，本次提交的说明是"learn git"
git status -s				查看版本库当前转态(Changes to be commited:暂存区有修改等待提交)
git diff readme.txt			查看readme.txt文件具体修改了什么内容
git log --pretty=oneline		查看提交日志
git reset --hard HEAD^			回退到上一个版本(两个版本HEAD^^，一百个版本HEAD~100)
git reset --hard 852bf			跳到版本号未852bf开头的版本(可前可后)
git reflog				查看Git的每一次版本库的变更(可查版本号)
git checkout -- readme.txt		暂存区中的readme.txt文件覆盖掉工作区中的readme.txt文件
git reset HEAD readme.txt		版本库中的readme.txt文件覆盖掉暂存区中的readme.txt文件
git checkout HEAD readme.txt		版本库中的readme.txt文件同时覆盖掉暂存区和工作区的readme.txt文件

ssh-keygen -t rsa -C "youremail@example.com"					创建SSH Key(C盘User文件夹的用户主目录下生成.ssh文件夹)
git remote add origin git@github.com:tinmen091008/TestGitOrigin.git		
本地仓库TestGitOrin和GitHub上的仓库TestGitOrin建立联系(本地仓库名和远程仓库名要相同)

git push -u origin master							第一次把本地仓库的内容推送到远程仓库
git push origin master								第二次及以后推送
git clone git@github.com:tinmen091008/TestGitOrigin.git				克隆远程仓库TestGitOrigin到本地当前目录
git pull origin master								把远程仓库的内容拉取到本地仓库

git checkout -b dev				创建并切换到dev分支(git branch dev和git checkout dev)
git branch					查看当前分支
git checkout master				切换到master分支
git merge dev					把dev分支的内容合并到当前分支(master分支)
git branch -d dev				删除dev分支