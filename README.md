github 简单的使用教程
一、先是安装git和一些基本的设置：

1、安装git 在命令行输入sudo apt-get install git 
2、安装好之后在命令行输入：
git config --global user.name "Your Name Here"
其中的“Your Name here”输入的就是你注册时候的用户名，这步是设置你提交时候默认的用户名
3、之后设置提交时候默认的邮箱，在命令行输入：
git config --global user.email "your_email@example.com"
其中的“your_email@example.com”就是你注册时候用的邮箱，当然也可以用别的邮箱，用别的邮箱的时候你必须在github的主页上设置里面把用的邮箱添加进去

4 提交密钥 
生成的密钥,把它放到github上
ssh-keygen -C 'xlinlu@qq.com' -t rsa
cd .ssh
more id_rsa.pub
ssh git@github.com

二、建立新的 repository（引用了源网页的帮助这里面已经写的很明了）

三、这是针对一个新建立的repository的操作（已有项目跳过这个，直接看第四点）

1先建立一个目录，该目录名跟你新建立的repository有关，命令如下(一行一个命令)：
mkdir ~/Hello-World        
（其中的hello0-World就是你新建立的repository的名称）
cd  ~/Hello_World
git init
(初始化一个空的Git repository )
touch README     //README 暂时写入“hello world”
(建立一个文件，README文件的主要用途是描述项目或者一些加入信息的文档，例如关于如何安装该项目或者怎么使用这个项目)
2、提交刚加入的文件README,命令如下(下面的两步是不能省略的，文件名可以改为你想要提交的文件名)：
git add README
git commit -m 'first commit'
3、push 提交(这里提交的方式是使用http的方式，也有ssh的提交方法，这里面就不做介绍了)
git remote add origin https://github.com/username/Hello-World.git  
(其中的https://github.com/username/Hello-World.git，是该项目的http,这可以在网页上得到，复制过来即可)
之后会要求输入用户名和密码
提交的命令是：
git push origin master
四、针对已有项目，先clone下来。clone 命令如下
git clone https://github.com/username/Hello-World.git  
之后操作从跟第三步骤中的第2点之后差不多了

五 Test push again!
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/xiaolinlu/hellogit.git
git push -u origin master




