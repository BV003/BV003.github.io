+++
title = 'Git使用'
date = 2024-10-13T10:20:43+08:00
+++

# git基本使用

git连接远程仓库

git remote add origin [https://github.com/coderzh/coderzh.github.io.git](https://github.com/coderzh/coderzh.github.io.git)

先创建出一个仓库，然后进行在仓库里面修改

 ```
git add .
git commit -m "注释语句"
git push -u origin main
 ```

push后面加上-f进行强制提交

github在linux上停止了账号密码登录

说是不能使用密码，应该使用person token

使用指令

 ```
git remote set-url origin https://口令字符串@github.com/用户名/远程仓库名
 ```

口令字符串为github网站生成