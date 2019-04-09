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
