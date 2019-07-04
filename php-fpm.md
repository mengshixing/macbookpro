### 自带的php-fpm一般起不来

- 复制配置文件
- sudo cp /private/etc/php-fpm.conf.default /private/etc/php-fpm.conf
- sudo cp /private/etc/php-fpm.d/www.conf.default /private/etc/php-fpm.d/www.conf

###### 然后报错failed to open error_log (/usr/var/log/php-fpm.log): No such file or directory (2)
- 更新路径到/usr/local/var
- sudo php-fpm -y /private/etc/php-fpm.conf --prefix /usr/local/var
- --prefix参数，这样可以将要安装的应用安装到指定的目录中
