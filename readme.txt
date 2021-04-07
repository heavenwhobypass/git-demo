// 创建 用户
git config --global user.name "ttw"
git config --global user.email "907993189@qq.com"

//查看
git config user.name
git config user.email

//创建git
git init    # 创建.git 文件夹
start .git  # win 下用start初始化git文件夹  其他用 open .git 来初始化

// 查询状态
git status -s  // -s表示缩写

//git 添加  untracked -> staged
git add filename
git add .

//查看log
git log

//commit    staged -> unstaged.unodified
git commit -m "notes..."
git commit --amend --no-edit  补上东西，而且不改备注

//diff   比较上次commit的和这次修改过但没add的
git diff
在git add 之后 要用  比较 上次commit和这次add的
git diff --cached    

// reset 回到过去/未来版本 整个文件夹的版本
git reset filename  已经add了文件
git reset --hard HEAD 回到最新的一个版本 HEAD^n 回到前n个版本 也可以直接加id
git reflog

// 单个文件的 版本
