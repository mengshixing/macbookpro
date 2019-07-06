### 自带的php-fpm一般起不来

- 复制配置文件
- sudo cp /private/etc/php-fpm.conf.default /private/etc/php-fpm.conf
- sudo cp /private/etc/php-fpm.d/www.conf.default /private/etc/php-fpm.d/www.conf

###### 然后报错failed to open error_log (/usr/var/log/php-fpm.log): No such file or directory (2)
- 更新路径到/usr/local/var
- sudo php-fpm -y /private/etc/php-fpm.conf --prefix /usr/local/var
- --prefix参数，这样可以将要安装的应用安装到指定的目录中

short_open_tag boolean
决定是否允许使用 PHP 代码开始标志的缩写形式（<? ?>）。如果要和 XML 结合使用 PHP，可以禁用此选项以便于嵌入使用 <?xml ?>。否则还可以通过 PHP 来输出，例如：<?php echo '<?xml version="1.0"'; ?>。如果禁用了，必须使用 PHP 代码开始标志的完整形式（<?php ?>）。
