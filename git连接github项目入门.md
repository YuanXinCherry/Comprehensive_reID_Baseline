## 1. 安装

- 去官网https://git-scm.com/downloads下载，运行安装包后默认安装即可。

---

## 2.初始化本地仓库

- 新建空白文件夹，例mz_work
- 打开git bash，进入到mz_work： cd /path_to/mz_work
- 执行 git init

## 3.添加github远程仓库

- 执行 git remote add origin https://github.com/YuanXinCherry/Comprehensive_reID_Baseline

## 4.强制将远端仓库内容更新到本地

- 执行 :

  ​	git fetch --all

  ​    git reset --hard origin/master    

## 5.本地修改内容上传远程仓库

- 在本地仓库修改、删除、添加自己的内容，例如，新建一个some.txt

- 查看本地仓库内容的状态，执行 git status

- 将更改提交到本地缓冲区：

  ​	git add some.txt

  ​	git commit some.txt -m "提交信息"		

- 将本地缓冲区内容上传到服务器远端仓库，执行 git push origin master

  ​	注：第一次执行该命令，会有验证过程，按照要求完成即可。

- 从远端仓库下载最新内容，执行 git pull origin master