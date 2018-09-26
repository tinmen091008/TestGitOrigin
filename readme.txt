mkdir GitRepository				在当前目录创建一个名字叫做GitRepository的目录
cd GitRepository				进入GitRepository目录
pwd								查看当前目录所在路径
git init						把当前目录变成Git可以管理的版本库(多出一个.git文件夹)
ls								查看当前目录所有文件和文件夹(ls -ah可查隐藏目录)
git add readme.txt				把readme.txt文件从工作区添加到暂存区
git commit -m "learn git"		把暂存区的所有文件提交到版本库，本次提交的说明是"learn git"
git status -s					查看版本库当前转态(Changes to be commited:暂存区有修改等待提交)
git diff readme.txt				查看readme.txt文件具体修改了什么内容
git log --pretty=oneline		查看提交日志
git reset --hard HEAD^			回退到上一个版本(两个版本HEAD^^，一百个版本HEAD~100)
git reset --hard 852bf			跳到版本号未852bf开头的版本(可前可后)
git reflog						查看Git的每一次版本库的变更(可查版本号)
git checkout -- readme.txt		暂存区中的readme.txt文件覆盖掉工作区中的readme.txt文件
git reset HEAD readme.txt		版本库中的readme.txt文件覆盖掉暂存区中的readme.txt文件
git checkout HEAD readme.txt	版本库中的readme.txt文件同时覆盖掉暂存区和工作区的readme.txt文件