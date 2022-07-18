<<<<<<< HEAD
# Github团队协作

### 一、Git常用命令

| 命令名称                           | 作用                                                      |
| ---------------------------------- | --------------------------------------------------------- |
| git remote -v                      | 查看当前所有远程地址别名                                  |
| git remote add 别名 远程地址       | 起别名                                                    |
| git push 别名 分支                 | 推送本地分支上的内容到远程仓库                            |
| git clone 远程地址                 | 将远程仓库的内容克隆到本地                                |
| git pull 远程库地址别名 远程分支名 | 将远程仓库对于分支最新内容拉下来后与 当前本地分支直接合并 |
| git config --global -l             | 查看git 配置                                              |
|                                    |                                                           |

### 二、git修改本地用户名和邮箱（安装git时候配置一次）

#### 1. 清除本地用户名和密码(不需要)

```
git config --system --unset credential.helper
```

#### 2. 执行以下命令后，再次pull或push时会缓存输入的用户名和密码（不需要）

```
git config --global credential.helper store
```

#### 3. 上传代码用户名

```jAVA
git config --global user.name "github用户名"  // 需要加""
```

#### 4. 上传代码邮箱

```
git config --global user.email "github邮箱" // 需要加""
```

### 三、本地仓库上传到远程仓库

在当前文件目录下执行一下操作:

#### **1、初始化一个本地Git仓库**

```Java
git init  // 初始化本地仓库
```

<img src="F:\Git\img\image-20220718090354402.png" alt="image-20220718090354402" style="zoom:67%;" />

执行以上命令，我们能够发现在当前目录下多了一个`.git`的目录，这个目录是Git来跟踪管理版本库的，千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。

#### 2、把本地的 master 仓库名称修改为远端的 main

```
git branch -m master main
```



#### 3、将所有文件添加到本地仓库（也可添加你所需的文件）

```Java
git add . // 先上载缓存 将所有文件添加到本地仓库（也可添加你所需的文件） .代表添加文件夹下所有文件。 
git commit -m “first commit”          //将项目提交到本地git仓库 （“first commit” 是备注信息）
```

<img src="F:\Git\img\image-20220718090640068.png" alt="image-20220718090640068" style="zoom:67%;" />

#### 4、将本地仓库与远程仓库进行关联

```Java
git remote -v  //检查远程仓库配置
git remote add origin +  //远程仓库地址, "origin" 是起的别名 可替换
```

<img src="F:\Git\img\image-20220717214930505.png" alt="image-20220717214930505" style="zoom: 50%;" />

<img src="F:\Git\img\image-20220718090750015.png" alt="image-20220718090750015" style="zoom:67%;" />

#### 5、先将关联后的github仓库中的代码pull下来

```Java
git pull origin main
```

![image-20220718090936675](F:\Git\img\image-20220718090936675.png)

#### 6、将最新的修改推送到远程仓库 将本地仓库的文件推送到远程仓库

```
git push -u origin main
```

![image-20220718091209924](F:\Git\img\image-20220718091209924.png)

### 四、常见错误：

#### 错误1：

执行 pull，push, clone等出现下面错误

```
error: RPC failed； curl 28 OpenSSL SSL_read: Connection was reset, errno 10054 fatal: expected
```

解决方法：执行下面代码重试即可：

```
git config --global http.sslVerify "false"
```

#### 错误2：

出现下面错误：

```
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/MrWang1218/Cog.git/'
```

意思是不再支持用户名密码的方式验证了，需要创建个人访问令牌(personal access token)。

**解决方法**：[(42条消息) 解决 remote Support for password authentication was removed on August 13, 2021._ASDDAG的博客-CSDN博客](https://blog.csdn.net/qq_50840738/article/details/125087816)

#### 错误3：

出现下面错误：

```
error: Pulling is not possible because you have unmerged files
```

解决方法：

```Java
//注释：提交本地代码到工作区
//注释：如果有冲突，先解决冲突合并代码，然后提交
//注释：如果代码上没有冲突，但是提交的时候git提醒有冲突，那么先关闭编辑器，然后编译代码找到冲突，最后手动合并代码解决冲突
git add .
git commit -m '提交本地代码并且获取最新代码'
//注释：获取分支最新代码
git pull origin main
//注释：如有冲突就解决冲突
```

#### 错误4：

出现下面错误：

```J
To https://github.com/MrWang1218/Test.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/MrWang1218/Test.git'

```

**解决方法：**



#### 错误5：

#### 错误6：

#### 错误7：

#### 错误8：

#### 错误9：
=======
# Test
>>>>>>> 64b143ef006301866a958128cfd486f57d9a2ea0
