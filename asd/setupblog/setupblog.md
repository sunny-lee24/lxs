#setUpBlog


###安装brew

执行命令

    1  $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
###安装wget


执行命令

    1  $ brew install wget
###安装nvm(node.js的版本管理工具)

    1  $ wget -qO- https://raw.github.com/creationix/nvm/master/install.sh | sh
###添加如下内容到~/.zshrc 配置文件

    1  [ -s "/Users/`users`/.nvm/nvm.sh" ] && . "/Users/`users`/.nvm/nvm.sh" # This loads nvm
###安装node.js(通过nvm安装)

    1  $ nvm install 0.10
    
###安装hexo

    1  $ npm install -g hexo
###创建hexo文件夹，并安装hexo组件

    1  $ hexo init hexo
    2  $ cd hexo
    3  $ npm install
###查看本地

输⼊入如下命令后,打开浏览器,并输⼊入localhost:4000来查看

    1  $ hexo g
    2  $ hexo s
    
    
###登录github.com注册github账号

###创建与github同名的repository

eg : github账号名位RicheyLee,则创建RicheyLee.github.io

###部署到github上

如下所示编辑_config.yml

    1   deploy: 
    2  type: github
    3  repository: git@github.com:dorayox/dorayox.github.io.git
    4  branch: master
输入如下命令，完成到github的部署，之后打开浏览器并输入RicheyLee.github.io来查看

    1  $ hexo g
    2  $ hexo d
##上传文件到blog

在hexo目录下，创建新文件

eg : 创建新文件test

    1  $ hexo new test
默认创建的新文件后缀问 .md文件，存在hexo/source/_posts/目录下

使用MOU打开新建的文件并完成编辑

    1  $ mou source/_posts/test.md
将新建的文件声称网页

    1  $ hexo g
上传到blog

    1  $ hexo d
登录blog查看是否上传成功

     http://RicheyLee.github.io

