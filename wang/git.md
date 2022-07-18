## Github团队协作

​		[(42条消息) Git —— 4、团队协作机制及GitHub操作_Mr_zhangyj的博客-CSDN博客_github团队协作](https://blog.csdn.net/Mr_zhangyj/article/details/123752142)

各种错误解决：[(42条消息) git各种报错的原因---规范步骤【小爽爽记录】_康斯坦奇的博客-CSDN博客](https://blog.csdn.net/qq_40245974/article/details/124646537)

## [Git——本地仓库与远程仓库关联](https://www.cnblogs.com/dreamstartplace/p/15831037.html)

在当前文件目录下执行一下操作:

#### **1、初始化一个本地Git仓库**

```git
git init
```

 执行以上命令，我们能够发现在当前目录下多了一个`.git`的目录，这个目录是Git来跟踪管理版本库的，千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。

　 注意:Git会自动为我们创建唯一一个`master`分支

#### 2、将本地仓库与远程仓库进行关联

```
git remote -v  //检查远程仓库配置
git remote add origin +  //远程仓库地址
```

<img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220717214930505.png" alt="image-20220717214930505" style="zoom: 50%;" />

> ***出现以下错误原因:***
>
> ```
> error: remote origin already exists.  // 意思是远程仓库已经存在，可以用 git remote rm origin 移除现存连接
> ```
>
> 

#### 3、先将关联后的github仓库中的代码pull下来

```
git pull origin master
```

> ***出现以下错误原因:***[(42条消息) Git 常见错误 之 error: src refspec xxx does not match any / error: failed to push some refs to 简单解决方法_仙魁XAN的博客-CSDN博客_error:src refspec](https://blog.csdn.net/u014361280/article/details/109703556)
>
> ```
> fatal: Couldn't find remote ref master
> error: src refspec test does not match any
> error: failed to push some refs to 'https://github.com/MrWang1218/COGDL-R.git'
> ```
>
> 1、把本地的 master 仓库名称修改为远端的 main
>
> ```
> git branch -m master main
> ```
>
> 

#### 4、将最新的修改推送到远程仓库 将本地仓库的文件推送到远程仓库

```
git push -u origin main
```

 第一次使用加上了-u参数，是推送内容并关联分支。

推送成功后就可以看到远程和本地的内容一模一样，下次只要本地作了提交，就可以通过命令：git push origin master   把最新内容推送到Github上关联的远程仓库中去