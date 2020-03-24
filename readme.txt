创建版本库
1.用命令git add <file>，注意，可反复多次使用，添加多个文件；
2.使用命令git commit -m <message>，完成。

版本回退
1.HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
2.穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
3.要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

工作区和暂存区
工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。
Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。
第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。
一旦提交后，如果你又没有对工作区做任何修改，那么工作区就是“干净”的

管理修改
每次修改，如果不用git add到暂存区，那就不会加入到commit中。

撤销修改
命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
总之，就是让这个文件回到最近一次git commit或git add时的状态。
git reset HEAD <file>可以把暂存区的修改撤销掉（unstage），重新放回工作区

Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.