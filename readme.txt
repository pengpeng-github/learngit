创建版本库
1.用命令git add <file>，注意，可反复多次使用，添加多个文件；
2.使用命令git commit -m <message>，完成。

版本回退
1.HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。
2.穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
3.要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。



Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.