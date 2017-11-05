## 使用Git 管理Android项目工程 ##

### Git简介 ###
　　1、Linus的第二个伟大作品。2005年由于BitKeeper软件公司对Linux社区停止了免费使用权。Linus迫不得己自己开发了一个分布式版本控制工具，从而Git诞生了。

　　2、目前使用Git作为版本控制的开源软件：Linux kernel，Android, jQuery, Ruby on Rails，Debian…

　　3、Eclipse 上使用Git的的项目数量已经超过了使用SVN的仓库数

### 为什么使用Git ###

- 分布式、强调个体
- 公共服务器压力和数据量都不会太大
- 速度快，灵活
- 任意两个开发者之间可以很容易的解决冲突
- 离线工作
- 每日工作备份
- 可以回滚代码块


### Git的交互流程图 ###





### 开源项目工作流程图 ###





### Git 安装 ###



### Git 命令 ###
- git status
 	 >仓库修改查看状态


- git log -n
	>查看commit 提交的日志信息
	
- git add ..
   	>添加当前目录中所有的文件至Git 仓库
   

- git add <filename/Directory>
   	>添加指定文件/目录
   
- git merger branch
  	>合并分支,直接合并，区分下面的 git merger --no--ff 
  
- git merger --no-ff branch(保留分支历史)
   	>合并分支并，进入vim编辑器，并保留分支提交的历史记录，
   
- git branch 
  	> 查看当前Project本地所有分支
  
- git branch -a
	   >查看远程分支
   
- git checkout branch
	   >创建分支
   

- git checkout -d branch
   >创建分支,并切换到当前分支

- git push origin master/branch
	>提交代码值远程仓库
	
- git br -D branch
	>删除本地分支
	
- git push origin :branch
	>删除远程分支

- git reset --hard commitid
	>回滚到commitid，将commitid之后提交的commit都去除


##日志格式化输出#
- 示例：

	>git log -1 --pretty=format:"代码提交人：%an %n代码提交时间：%cd %n代码提交日志：%n%b%n%s" --date=format:'%Y年%m月%d日 %H时%M分%S秒' > log.txt
   




