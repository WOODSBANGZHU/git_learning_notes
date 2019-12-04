# 基本操作


    git init
    
    git add [文件name]
    
    git status
    
    git commit -m 'some words'


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



2、再添加远程git仓库

以http的方式和以ssh的方式。

    $ git remote add origin git@github.com:WOODSBANGZHU/git_learning_notes.git

    $ git push -u origin master

当本地仓库文件有变化时，需要提交到github上，使用命令` git push origin master `就可以在GitHub上直接更新。

git 网站中关于上传reposity的方法

    …or create a new repository on the command line
    echo "# git_learning_notes" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:WOODSBANGZHU/git_learning_notes.git
    git push -u origin master


# 取得项目的Git仓库

取得Git项目的仓库有两种方法。**第一种**是在现存的目录下，通过导入所有文件来创建新的 Git 仓库。**第二种**是从已有的 Git 仓库克隆出一个新的镜像仓库来。

### 第一种方式：导入所有文件


1、先新建一个文件夹（test1）

2、打开Git bash，定位到新建文件夹，输入命令：**cd E:\test1**

3、初始化新仓库，输入：**git init**

4、手动打开test1文件夹，并将项目拷贝至此文件夹

5、在命令窗口输入**git status** 查看文件状态，出现红色字符串，表示该文件夹在项目中，并且为未提交的状态。

6、上传 **git add [文件name]**

7、提交 **git commit -m 'first commit'**

### 第二种方式：从仓库中克隆

先建立一个文件夹（test2），并定位到该文件夹的位置。

>Git官网表述： 如果想对某个开源项目出一份力，可以先把该项目的 Git 仓库复制一份出来，这就需要用到 git clone 命令。如果你熟悉其他的 VCS 比如 Subversion，你可能已经注意到这里使用的是 clone 而不是 checkout。这是个非常重要的差别，Git 收取的是项目历史的所有数据（每一个文件的每一个版本），服务器上有的数据克隆之后本地也都有了。实际上，即便服务器的磁盘发生故障，用任何一个克隆出来的客户端都可以重建服务器上的仓库，回到当初克隆时的状态。

    $ git clone git://github.com/schacon/grit.git

这会在当前目录下创建一个名为grit的目录，其中包含一个 .git 的目录，用于保存下载下来的所有版本记录，然后从中取出最新版本的文件拷贝。如果进入这个新建的 grit 目录，你会看到项目中的所有文件已经在里边了，准备好后续的开发和使用。如果希望在克隆的时候，自己定义要新建的项目目录名称，可以在上面的命令末尾指定新的名字：

    $ git clone git://github.com/schacon/grit.git mygrit

唯一的差别就是，现在新建的目录成了 mygrit，其他的都和上边的一样。