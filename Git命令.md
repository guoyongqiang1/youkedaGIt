# Git命令
> [浅析 Git 思想和工作原理](https://www.jianshu.com/p/619122f8747b)

1. 查看是否生成ssh cat ~/.ssh/id_rsa.pub
2. 生成本地ssh ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
3. 配置全局变量 git config --global user.name "yebing"
            git config --global user.email "hhdd576@126.com"
4. git clone 仓库地址 git clone 仓库地址
**提交** 
5. git add -A （-A all）
6. git commit -m "本次提交的修改的备注"
> 新创建的文件必须要按照顺序进行提交，如果只是修改文件，并没有创建文件，也可以使用git commit -am "本次提交的修改的备注"来合并前面两个步骤。

7. git push origin main
8. git push
9. git push origin b
10. 抓取远程仓库的内容 git pull



初始化为git仓库 git init
绑定远程仓库 
git remote -v 命令来查看当前git仓库绑定的远程仓库，刚刚初始化的仓库一般来说是没有绑定远程仓库的，而从线上clone下来的仓库是必然有远程绑定的。
git remote -v 显示空白，即无绑定，才可以进行远程仓库的绑定，否则提示冲突
git remote add origin 仓库地址

分支
创建新的分支 git branch v1
切换分支 git checkout v1
        这两条命令合用 git checkout -b dev


Linux命令：
> 谨记：Linux命令和所在的路径相关，一定要时刻注意自己是否在所在在正确的路径

1. 查看当前目录下的文件 ls
2. 查看当前目录下的文件，包括隐藏文件 ls -a
3. 在当前目录下创建文件 touch 文件
4. 在当前目录下创建文件夹 mkdir 文件夹
5. 进入某个文件夹： cd 文件目录(如果直接cd，则会返回根目录，在window电脑下会回到当前所在的盘符)
6. 删除当前目录下的指定文件(慎用) rm -rf 文件



# Hexo
[Hexo博客文档](https://hexo.io/zh-cn/docs/)

hexo init blog
npm install hexo-deployer-git --save（命令需要在博客文件夹内安装，如果创建了新的博客文件夹需要重新安装）
修改配置文件 _config.yml
```yml
    theme: landscape

deploy:

  type: git

  repository: 你的GitHub仓库地址

  branch: master 
    //
```
> 注意  地址也使用git开头的SSH地址，仓库名要符合github用户名+github.io的规则
注意    theme:后面有一个空格，同样的type:后面也有，这是yml格式文件的特点之一
注意    type:是由缩进的，t和上面deploy的p对齐

提交
hexo clean 清除缓存
hexo generate 生成新的静态文件，可简写为hexo g
hexo deploy 把生成的文件部署到博客上可简写为hexo d


发布新博客 hexo new 博客名 

更换主题
下载主题文件 git clone https://gitee.com/xiaoyebing/hexo-theme-next.git themes/next



[npm的安装](https://blog.csdn.net/weixin_39477597/article/details/87784418)
[GITHUB+HEXO博客轻松更换主题外观](https://www.jianshu.com/p/469e985288b3)d