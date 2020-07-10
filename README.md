# Git使用方法-简版

## 命令行操作

### 1. 创建远程仓库（一组创一个即可）
   
   github上面create repository，注意不要用README.md初始化仓库，即创建时下图的这个别选。
   
   ![UM4yWV.jpg](https://s1.ax1x.com/2020/07/11/UM4yWV.jpg)

### 2. 使用git命令，在本地克隆远程仓库
   
   `git clone https://github.com/daibi07/Test1.git`

### 3. 设置签名

   `git config user.name "你的用户名"`
   
   `git config user.email "你的邮箱"`
   
   也可以进行全局设置，也就是clone到本机上的所有项目都用一个签名：
   
   `git config --global user.name "你的用户名"`

   用此命令查看设置：
   `git config -l`

### 4. 项目修改后提交到本地仓库

   添加文件修改：`git add .`

   提交文件修改到本地仓库：`git commit -m "XXXX"`（里面就是填个版本号吧）
   
### 5. 将本地仓库提交到远程仓库（push）   
   
   先通过命令git remote show [remote-name] 查看某个远程仓库的详细信息，比如要看所克隆的origin仓库，可以运行：
   
   `git remote show origin`
   
   如果这个远程仓库的地址与你所想提交的地址不符，可以进行修改：
   
   `git remote rm origin`
   
   `git remote add origin your_remote_url`（如：https://github.com/daibi07/Test1.git）
   
   提交到远程仓库：`git push -u origin master`
   
   push时可能会报错说“更新被拒绝，因为远程仓库包含您本地尚不存在的提交”，可参考此[解决方法](https://blog.csdn.net/XiangJiaoJun_/article/details/83721557?utm_medium=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase)
   
### 6. 将远程仓库同步到本地（pull）

   `git pull origin master`

## VS Code中操作（前3步一致）

### 4. 项目修改后提交到本地仓库

   4.1 添加文件修改
   
   * 在这里可以看到所有工作区还没有提交暂存区的操作
   
   ![1](https://img-blog.csdnimg.cn/20190410123702931.png)
   
   * 添加到暂存区
   
   ![222](https://img-blog.csdnimg.cn/2019041012400147.png)
   
   以上步骤相当于执行了：`git add .`
   
   4.2 提交到本地仓库
   
   ![333](https://img-blog.csdnimg.cn/20190410124526338.png)

   相当于执行了：`git commit -m "XXXX"`

### 5. 将本地仓库提交到远程仓库（push）

   ![55](https://img-blog.csdnimg.cn/20190410124824726.png)

   ![555](https://img-blog.csdnimg.cn/20190410125013939.png)

   ![5555](https://img-blog.csdnimg.cn/20190410125121390.png)
   
   以上步骤相当于执行了：`git push -u origin master`

### 6. 将远程仓库同步到本地（pull）

   ![66](https://img-blog.csdnimg.cn/20190410125818250.png)
   
   此步骤相当于执行了：`git pull origin master`
   
## 参考资料

1. [如何在VSCode中使用Git](https://blog.csdn.net/sacredness/article/details/89179435)
2. [廖雪峰的Git教程](https://www.liaoxuefeng.com/wiki/896043488029600/898732864121440)
3. [Git远程仓库管理](https://www.cnblogs.com/lazb/articles/5597878.html)
3. [新增SSH密钥到GitHub 帐户](https://docs.github.com/cn/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

