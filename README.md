# GithubTest

## 练习使用git指令来上传代码到github

### 1、本地安装Git

  使用命令pip install -y git

### 2、本地配置Git相关参数
  配置Git的全局用户名和全局邮箱地址
  
  git config --global user.name "你的GitHub用户名"

  git config --global user.email "你的GitHub邮箱"
### 3、本地生成ssh公钥

  ssh-keygen -t rsa -C "你的GitHub邮箱"
  
  执行命令后一直按回车即可，生成后，公钥会存放在~/.ssh/id_rsa.pub下
  
  执行 cat ~/.ssh/id_rsa.pub
  
  复制公钥信息
  
### 4、将ssh公钥配置到Github账户上

  进入Github，点击头像settings→SSH and GPG keys→New SSH key
  
  每台电脑的ssh公钥不同，可以为其建立title命名，粘贴生成的公钥
  
  
### 5、Github建立仓库并与本地链接
  Github上建立仓库，左键点击Clone or download选择Use SSH复制里面的路径然后在服务器输入

  git clone git@github.com:xxx/xxx.git(你上面复制的地址)
  
  项目就下载到了本地，接下来就可以在这个文件夹中编写代码，然后使用
  git add 文件名，将文件加入缓冲区，为这个提交命名git commit -m "first add"
  
最后将这个文件push到github上的master分支
git push origin master
  
  
