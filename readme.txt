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

//查看log  graph参数显示branch
git log  --oneline  --graph

//commit    staged -> unstaged.unodified
git commit -m "notes..."
git commit --amend --no-edit  补上东西，而且不改备注
git commit -am "notes..." 直接add+commit

//diff   比较上次commit的和这次修改过但没add的
git diff
在git add 之后 要用  比较 上次commit和这次add的
git diff --cached    

// reset 回到过去/未来版本 整个文件夹的版本
git reset filename  已经add了文件
git reset --hard HEAD 回到最新的一个版本 HEAD^n 回到前n个版本 也可以直接加id
git reflog

// 单个文件的 版本
git checkout <commitid> -- test.py

// branch
git branch dev 创建分支 叫 dev
git checkput -b dev 创建分支 dev 并head指针移动到 dev上
git branch 查看分支
git checkout dev 切换分支
git branch -d dev 删除 dev 分支
git merge --no-ff -m "keep merge info" dev 合并dev版本到这个版本 # ff
fast-forward 直接移动master指针到dev版本指针

//rebase 分支冲突 慎用 rebase会直接改掉历史

// stash 把当前的修改缓存起来
git stash
git stash pop  回复缓存

//与github关联
git remote add origin add origin <address>
git push -u origin main
