## 进阶：

#### 1.本地仓库的创建

  在一个命名为英文的文件夹上右键，用 ***git bush here***  打开；然后对其输入  ：

```
$ mkdir learngit
$ cd learngit
$ pwd
```

其中 *$ pwd*   用于显示文件位置，再通过代码  ***$ git init***    即可创建一个git的仓库

#### 2.文件的添加和查看

###### （1）添加

将文件添加至git，需要使用代码 ***$ git add***   ，如我要添加一个 hello.md文件，则：

```
$ git add  hello.md
```

接着使用 *git commit*  命令来确定提交，如：

```
$ git commit -m "对该次修改的注释"
```

**注意**：每一次的添加必须要用 ***$ git add***先添加，再用***$ git commit***来保存修改，如果不用$ git add添加或添加多次却只使用了一次，则最后使用$ ***git commit***后只会改变***$ git add***提交的那次。



###### （2）查看

当我们需要修改文件时，可以通过命令看仓库的变化。

仓库检查的命令：

***git status***   ：检查仓库的状态，是否有未提交的修改。

***git diff***        ：查看修改前后具体的不同。

#### 3.文件版本的修改

###### （1）查看

对于近期有修改的文件，我们可以使用  ***git log***   来查看最近修改的三个版本以及内容。

###### （2）返回（过去）：

在 git log 中 我们可以看到  **HEAD**  的标识，**HEAD** 表示当前的版本，而且上一个版本则用**HEAD^**  来表示  (每回去一个版本增加一个"^") 。若版本过多则可以用**HEAD~100**来表示。如此，若要修改为上一个版本，则用：

```
$ git reset --hard HEAD^
```

###### （3）前进（未来）：

当我们再次后悔，想要修改为之前的最新内容时，我们只需要记住之前我们用 **git log**   查看的版本号，此时我们输入：

```
$ git reset --hard (之前的版本号前几位)
```

**注意：前几位最好是三位以上**

如果你不记得之前的版本号了，还可以使用***$ git reflog***  来查看之前的命令，从而获取版本号。

#### 4.文件的删除和撤销

###### （1）撤销：

*工作区*：当我们写文件时出现了错误，我们可以使用 ***$ git checkout***   代码来将文件返回到最近一次git commit或git add时的状态

暂存区：当我们要撤销暂存区的数据时，可以使用：***git reset HEAD <file>***（对于代码***git reset***  还可以退回版本）此时，暂存区的数据就会返回到工作区。

###### （2）删除：

删除一般用到两个代码***git rm*** 和 ***git checkout。***

**git rm**  ：删除一个文件，将其命令添加到暂存区，再用***git commit***   确定。

***git checkout  ：对于误删的文件，用git checkout*** 可以将其还原（注意：还原只能还原最近一次提交修改的内容）*

#### 5.远程仓库的创建

###### （1）SSH的创建

因为本地仓库和远程仓库时通过SSH加密的，我们要先拥有一个ssh密钥，可以通过以下代码实现：

```
$ ssh-keygen -t rsa -C "youremail@example.com"
```

此后，我们可以通过 ***cat id_rsa.pub***代码来找到我们的公共密钥，并将其复制粘贴到github上的SSH Key添加即可。

###### （2）同步仓库

在github上创建仓库后，我们可以在“code”中找到自己的SSH地址，如：

![image-20231113222913869](C:\Users\oojks\AppData\Roaming\Typora\typora-user-images\image-20231113222913869.png)

然后我们可以在自己的本地仓库中，用

```
$ git remote add origin git@github.com:kkzjyy/Tasks.git
```

来添加，将本地仓库和远程仓库关联（origin是远程仓库名，可以自己改变）。

此后，可以通过命令

```
$ git push origin master
```

来进行本地仓库和远程仓库的上传同步。

**Question:**

在同步中，遇到了如下问题：

```
ssh: connect to host github.com port 22: Connection refused
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

```

在删除.ssh密钥并重新设置后，仍然无法解决该问题。查看仓库地址也是正确的，但无法上传同步。为此，我决定尝试一下，htpps的地址来进行远程仓库的创建。但遇到了如下问题：

```
 git SSL certificate problem: unable to get local issuer certificate
```

在网上寻找后，可以用

```
git config --global http.sslVerify false
```

来解决服务器的信任问题。最后成功上传：

![image-20231114082147458](C:\Users\oojks\AppData\Roaming\Typora\typora-user-images\image-20231114082147458.png)

PS：仍未知道为啥ssh无法上传同步。