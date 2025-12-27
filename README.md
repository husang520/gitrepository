# gitrepository
This README is a test of send messages to git.

20240325 
Today I push this new revised README.md to origin repository.


20240524
https://blog.csdn.net/NHB456789/article/details/131596777 
You can learn from this blog.csdn for how to use git.
You will know how to push your program from local repository to github repository.

20251212
上传本地项目到 github 上。使用 SSH 认证 
1、在 gitbash 输入一下命令：(替换 your-email@example.com 为你的 github 邮箱)
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
执行后会提示你输入文件保存路径直接回车即可，默认 （~/ssh/id_rsa）。然后要求你输入密码，直接回车跳过，接着会再次输入密码，再次回车。

2、添加 SSH Key 到 github 中
运行以下命令：
cat ~/.ssh/id_rsa.pub 
复制输出的 SSH_Key 进入 gitbub SSH Key 的管理页面 点击 New SSH Key，复制进去就可以。

3、进入本地的项目中路径中，输入以下命令：
git init
进行初始化。

4、关联远程 github 仓库，输入以下命令：
git remote add origin git@github.com:your-username/your-repository.git
再使用以下命令来检查远程仓库是否添加成功：
git remote -v 
如果返回对应的 origin 和对应的仓库地址，就是对的。

5、添加所有文件到 git 版本控制：
git add .

6、提交代码：
git commit -m "first commit"

7、确保推送分支，首次推送时，需要设置 main 或者 master
git branch -M main

8、最后，推送代码：
git push -u origin main
等待推送完成，就可以在 github 中看到代码了。

当需要进行大文件传输 也就是文件超过 100Mb 之后，就需要用到 lfs （large files storage）

1、下载 lfs ：
git lfs install

2、跟踪大文件：
git lfs track "*.exe"

3、需要添加 .gitattributes
git add .gitattributes

3、添加和提交大文件
git add .
git commit -m "xxx"
git push -u origin main

