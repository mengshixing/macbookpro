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

进入命令行 psql --help可以 psql -U username 或者 psql -d dbname 进入

给用户更改权限 alter role 'test' with superuser;


电脑有时候重启后pg无法启动的问题，拷贝postgresql.pid到/tmp/下面一份
