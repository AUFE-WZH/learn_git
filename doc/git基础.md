1.配置user信息：
    配置user.name和userr.email:
        git config --global user.name 'your_name'
        git config --global user.email 'your_email@domain.com'
    config的三个作用域：(缺省等同local)
        git config --local      (对某个仓库有效)
        git config --global     (对当前用户所有仓库有效)
        git config --system     (对系统所有登录用户有效)
    显示config 的配置，加--list
        git config --list --local
        git config --list --global
        git config --list --system    

2.建立git仓库：
    两种场景：
        (1) 已有项目代码纳入git中：
            cd dir      (项目代码所在的文件夹)
            git init

        (2) 新建的项目直接用git管理
            cd dir      (项目代码所在的文件夹)
            git init your_project (会在当前路径下创建和项目名称同名文件夹)
            cd your_project

3.工作区与暂存区概念：
    工作目录-------------->暂存区-------------->历史版本
           (git add files)     (git commit -m'xxx')

4.重命名文件名：
    git mv readme readme.md  (将readme重命名为readme.md)

5.通过git log查看版本演变历史：
    (1) 缺省参数:git log (打印当前分支提交记录的详细信息)
    (2) 看分支: git log temp (查看temp分支提交记录)
    (3) 一行显示:git log --oneline (当前分支每个提交记录都是一行显示)
    (4) 打印4次:git log -n4 --oneline (一行显示四次提交记录)
    (5) 加all: git log --all (打印所有分支提交记录的详细信息)
    (6) 图形化: git log --all --graph (图形化显示所有记录)
    (7) 一行且所有: git log --oneline --all (所有记录显示且每个记录一行)
    (8) 综合使用: git log --oneline --all -n4 --graph

6.图形化工具gitk查看历史记录：
    