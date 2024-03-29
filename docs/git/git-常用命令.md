[git-workflowy](https://workflowy.com/s/git/B0kfqXVCueomwBKG)

### **初始化本地仓库** 

` $ git init`

### **查看**

#### 查看文件夹内有哪些元素

`$ ls（查纯文件）；ls -a（查所有文件，含隐藏文件git)`

####  查看哪些内容是否未提交

 `$ git status`

#### 查看分支

 `$ git branch`

#### 查看远程仓库

 `$ git remote`

####  查看工作区与暂存区变更内容区别

 `$ git diff`

###  **创建分支**

` $ git branch <分支名>`

### **切换到另一分支**

 `$ git checkout <分支名>`

### **加入至工作区**

 `$ git add .`

### **提交到库存区**

 `$ git commit -m "???"`
**
### 将本地仓库推上去远程仓库；7:50**

` $ git push https://gitee.com/c**y/cs001.git master`

### **展示远程服务器信息，以及和本地是否同步**

` $ git remote show origin`

### 为远程服务添加一个”别名“，而远程服务器的地址是https://...；10:00

 `$ git remote add cshjgy001 https://gitee.com/cshjgy/cs001.git `

### 用服务器别名将本地更改的文件推上远程（同步内容）：11:00

 `$ git push cshjgy001 master($ git push http://???// master）`

### **查看“下拉”是否已最新**

 `$ git pull`

###  **删除远程仓库“别名”1:48**

 `$ git remote remove <远程仓库“别名”>`

### **恢复远程仓库“别名”2:48（别名的通用写法“origin”)**

 ` $ git remote add origin https://gitee.com/cshjgy/test.git`

### **配置公匙**

### 删除之前的远程“别名”：0:25

 `git remote remove origin`

### **再查看是否已没有远程地址：**

 `git remote -v`

### **复制SSH作远程地址,新建“别名origin"**

 `git remote add origin git@gitee.com:cshjgy/test.git`

### **配置公匙1:10**

 `ssh-keygen -t rsa -C "1127984132@qq.com"`

## 二、其它命令

### 取消（重新运行）

 `ctrl+c 或按 Q`

### 查看分支

 `$ git branch`

### git besh here框删除后分支的历史查看

`$ git relog`

### 切换分支

`git checkout <分支名>`

### 删除分支

`$ git branch -D ali`

### 误删分支需要恢复 

(使用git log 查出分支的提交号。)

`git branch <分支名称> <提交号>`

### 重命名分支

 `git branch –m 当前分支名 新的分支名`

###  查看分支图

 `git log --graph`

### 简明查看分支图

 `git log --graph --pretty=oneline --abbrev-commit`

### 查看远程仓库：

 `$ git remote`

### 查看仓库地址：

`$ git remote -v`

### 回退到指定版本：

`$ git reset --hard <版本号>`

[TOC]

