--------数据库的安装与创建-----------

安装

brew install postgresql  

初始化数据库

initdb /usr/local/var/postgres -E utf8

创建一个数据库用户

createuser username -P

创建数据库

createdb dbname -O username -E UTF8 -e 

https://www.cnblogs.com/tdsun/p/8625249.html
