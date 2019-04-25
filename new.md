需要Markdown语法基础 Git操作 github账号
node.js环境
辅助软件Typora  https://typora.io/
 
前期准备工作
安装node环境 npm
安装gitbook
npm install -g gitbook-cli
gitbook -V 查看版本


开始编辑
1.在github创建一个新的仓库
2.新建文件夹 study-in-work
3.初始化 gitbook init
得到2个文件
README.md: 书的介绍文字，如前言、简介，在章节中也可做为章节的简介。
SUMMARY.md: 定制书籍的章节结构和顺序。

4.用Typora打开这个文件夹

5.编辑目录

6.目录建立好以后 初始化一下
gitbook init
注意： gitbook init 只支持生成两级目录

7.在本地预览书籍
gitbook serve
gitbook serve --port 2333  指定端口

8.构建书籍

gitbook build [书籍路径] [输出路径]

生成 PDF 格式的电子书：

gitbook pdf ./ ./mybook.pdf

生成 epub 格式的电子书：

gitbook epub ./ ./mybook.epub

生成 mobi 格式的电子书：

gitbook mobi ./ ./mybook.mobi


9.推送远端仓库

1.初始化git  git init

2.添加远端仓库
git add.

git commit -m "first commit"

git remote add origin https://github.com/csdjl88/study-in-work.git

git pull -u origin master

10.第三步：登录gitbook，选择用 github账号登录
网址：www.gitbook.com

11.创建一个新空间




git checkout --orphan gh-pages


git push -u origin gh-pages


*~移除的是备份文件，其实是任何以~结尾的文件



echo "*~" > .gitignore
echo "_book" >> .gitignore
git add .gitignore
git commit -m "Ignore some files"