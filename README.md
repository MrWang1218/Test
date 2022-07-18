# Github团队协作

- ### Git常用命令

| 命令名称                           | 作用                                                      |
| ---------------------------------- | --------------------------------------------------------- |
| git remote -v                      | 查看当前所有远程地址别名                                  |
| git remote add 别名 远程地址       | 起别名                                                    |
| git push 别名 分支                 | 推送本地分支上的内容到远程仓库                            |
| git clone 远程地址                 | 将远程仓库的内容克隆到本地                                |
| git pull 远程库地址别名 远程分支名 | 将远程仓库对于分支最新内容拉下来后与 当前本地分支直接合并 |
| git config --global -l             | 查看git 配置                                              |
|                                    |                                                           |

- ### git修改本地用户名和邮箱

### 本地仓库上传到远程仓库

在当前文件目录下执行一下操作:

**1、初始化一个本地Git仓库**

```Java
git init  // 初始化本地仓库
```

<img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220718090354402.png" alt="image-20220718090354402" style="zoom:67%;" />

执行以上命令，我们能够发现在当前目录下多了一个`.git`的目录，这个目录是Git来跟踪管理版本库的，千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。

#### 2、把本地的 master 仓库名称修改为远端的 main

```
git branch -m master main
```



#### 3、将所有文件添加到本地仓库（也可添加你所需的文件）

```Java
git add . // 将所有文件添加到本地仓库（也可添加你所需的文件） .代表添加文件夹下所有文件。
git commit -m “first commit”          //将项目提交到本地git仓库 （“first commit” 是备注信息）
```

<img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220718090640068.png" alt="image-20220718090640068" style="zoom:67%;" />

#### 4、将本地仓库与远程仓库进行关联

```Java
git remote -v  //检查远程仓库配置
git remote add origin +  //远程仓库地址, "origin" 是起的别名 可替换
```

<img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220717214930505.png" alt="image-20220717214930505" style="zoom: 50%;" />

<img src="C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220718090750015.png" alt="image-20220718090750015" style="zoom:67%;" />

#### 5、先将关联后的github仓库中的代码pull下来

```Java
git pull origin main
```

![image-20220718090936675](C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220718090936675.png)

#### 6、将最新的修改推送到远程仓库 将本地仓库的文件推送到远程仓库

```
git push -u origin main
```

![image-20220718091209924](C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20220718091209924.png)
