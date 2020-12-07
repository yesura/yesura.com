# Git & Github

### 一、注册 Github

​	打开 https://github.com/ 用邮箱注册。

### 二、新建 Github 仓库：

1. 点击 “Your Repository ”
2. 填写 “Repository name”，如果仓库名为：“用户名.githut.io” 的话，该仓库名可以直接作为访问地址。

### 三、使用 Git 部署本地工程到 Github：

 1. **安装 git ：**https://git-scm.com/

     配置账号信息：

     ```
     $ git config --global user.name "John Doe" （github用户名）
     $ git config --global user.email johndoe@example.com （github 注册邮箱）
     ```

     关联 git 和 github，一直按回车到生成密钥为止: 

     ```
     $ ssh-keygen -t rsa -C (生成密钥文件)
     ```

     打开 github 设置，复制已经生成的密钥到 “SSH and GPG keys” 里面

 2. **进入工程文件夹，鼠标右键 “Git Bash Here”：**

     初始化：

     ```
     $ git init
     ```

     添加文件：

     ```
     $ git add . (添加全部)
     $ git add readme.md (添加单个文件)
     $ git add book\ (添加一个文件夹)
     ```

     提交已经添加的文件到仓库：

     ```
     $ git commit -m "备注说明"
     ```

     关联 本地仓库与 github 仓库：

     ```
     $ git remote add origin https://github.com/yesura/yesura.github.io.git 
     ```

     上传本地仓库到 github 仓库某个分支（第一次上传使用 “-u”）：

     ```
     $ git push -u origin master
     $ git push origin gh-pages
     ```

     新建分支 "gh-pages"，并切换到该分支：

     ```
     $ git branch gh-pages (新建)
     $ git checkout gh-pages （切换）
     $ git checkout -b gh-pages （新建并切换）
     ```

     删除分支：

     ```
     $ git branch -d gh-pages
     ```