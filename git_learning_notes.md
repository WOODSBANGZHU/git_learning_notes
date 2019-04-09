# 增加分支和删除分支命令

    //创建dev分支
    git checkout -b dev

    //查看分支
    git branch
    * dev
     master

    //切换分支
    git checkout master

    //合并分支
    git merge dev

    //删除分支
    git branch -d dev

合并和删除分支的语句在master中进行的：
    
    WOODS@WOODS MINGW64 /e/git_line_camera (master)
    $ git merge dev
    Updating 88b2e66..644d791
    Fast-forward
     readme.txt | 1 +
     1 file changed, 1 insertion(+)
     create mode 100644 readme.txt
# 添加远程库
fatal: remote origin already exists.解决办法如下：

1、先删除远程git仓库

    $ git remote rm origin
    $ git push -u origin master


2、再添加远程git仓库

    $ git remote add origin git@github.com:WOODSBANGZHU/git_learning_notes.git

git 网站中关于上传reposity的方法

    …or create a new repository on the command line
    echo "# git_learning_notes" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:WOODSBANGZHU/git_learning_notes.git
    git push -u origin master