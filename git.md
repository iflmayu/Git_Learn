## git 安装

Git官网 https://git-scm.com/install/windows

## git 配置

### 配置身份信息

~~~cmd
git config --global user.name "name"
git config --global user.email "email"
~~~

### 验证配置信息

~~~cmd
git config --list
~~~

### 设置代理

~~~cmd
git config --global http.proxy socks5://127.0.0.1:<端口号>
git config --global http.proxy https://127.0.0.1:<端口号>
~~~



## 本地仓库操作

### 初始化仓库

打开终端，进入项目文件夹

~~~cmd
git init
~~~

### 核心操作

查看状态

~~~cmd
git stauts
~~~

暂存文件

| 命令           | 作用                 |
| -------------- | -------------------- |
| git add 文件名 | 暂存指定文件         |
| git add .      | 暂存当前目录所有修改 |

提交到版本库

~~~cmd
git commit -m "提交信息"
~~~



## 远程仓库

关联新远程仓库

~~~cmd
git remote add <别名 origin> <远程地址 https://github.com/你的用户名/你的仓库名.git>
~~~

推送代码到远程仓库

~~~cmd
git push -u <别名 origin> main
~~~

> -u: 第一次推送时加，以后推送直接用git push

从远程仓库克隆到本地

~~~cmd
git clone <远程地址 https://github.com/你的用户名/你的仓库名.git>
~~~

> git clone后只需git add . -> git commit -m "" -> git push