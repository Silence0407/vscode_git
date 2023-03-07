## 概述
    免费、开源的分布式版本控制系统
## 分类
    集中式版本控制
    分布式版本控制：
        1、断网的情况下也可以进行开发（因为版本控制是在本地进行的）
        2、每个客户端保存的也都是整个完整的项目（包含历史记录，更加安全）
## 工作机制
    1、工作区（写代码）
        --------git add-----
    2、暂存区（临时存储）
        ------- git commit-----
    3、本地库（历史版本）
## 代码托管中心
    基于网络服务器的远程代码仓库，一般称为远程库
    局域网：
        gitlab
    互联网：
        GitHub（外网）
        Gitee（国内网站）
## 常用命令
    git config --global  user.name  用户名        设置用户签名
    git config --global  user.email  邮箱         设置用户邮箱
    git init    初始化本地库
    git status  查看本地库状态
    git add 文件名   添加到暂存区
    git commit -m "日志信息"  文件名    提交到本地库
    git  reflog    查看历史记录
    git  reset --hard  版本号   版本穿梭
## 初始化本地库
    1、基本语法：git init           git reflog(查看引用日志版本信息)
    cat 文件名    读取文件内容
## 修改文件
    vim hello.txt---进入文件
    esc---退出编辑模式
    wq    退出
## 历史版本
    git reflog   查看版本信息
    git log   查看版本详细信息
    git reset  --hard 版本号

## 分支
    1、操作
        git branch 分支名   创建分支
        git branch -v      查看分支
        git checkout  分支名    切换分支
        git merge  分支名    把指定分支合并到当前分支上
            冲突合并：合并分支时，两个分支在同一个文件的同一个位置有两套不同的修改，必须人为决定新代码内容
                1、提示修改文件，修改完成后git add 文件名
                2、提交文件   git commit -m "日志名"  （此处不加文件名）
                3、合并分支 
 https://github.com/Silence0407/git-demo.git


 ## 创建远程库别名
    git remote -v  查看当前所有远程地址别名
    git remote  add  别名    远程地址

## 推送本地库到远程库
    git push 别名  分支  
## 拉取远程库到本地库
    git pull 别名  分支名
## 克隆代码（不需要登录账号）
    git clone 网址
    clone会做如下操作：
        1、拉取代码
        2、初始化本地仓库
        3、创建别名

## ssh免密登录
    ssh-keygen -t rsa -C ssh地址
    拉取：git pull ssh地址 分支名

## 提交