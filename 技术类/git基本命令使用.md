##目录
1. [新建库](#init)
2. [关于配置](#config)
3. [新建/删除](#add/delete)
4. [代码提交](#commit)
5. [分支操作](#branch)
6. [查看信息](#log)
7. [远程同步](#pull)
8. [撤销](#checkout)

##init
  - ```git init```  #在当前目录创建一个代码库
  - ``git init [project_name]``  #创建一个目录并初始化为新的代码库
  - `git clone [url]`  #下载远程代码库
  
##config
- 配置命令别名

  - `git config [--global] alias.[简称] 命令名` 
        例如: `git config --global alias.ci commit`
- 配置提交代码时的用户信息
  -  `git config [--global] user.name "[name]"`
  -  `git config [--global] user.email "[email address]"`
- 显示所有配置
  `git config list`
- 编辑配置文件
  `git config -e [--global]`

## add/delete
- 添加文件到暂存区
  - `git add [file]` 指定文件
  
  - ` git add .` 添加所有文件
  
  - `git add [dir]` 添加指定目录
       