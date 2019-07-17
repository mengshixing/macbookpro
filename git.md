## mac 的git环境依赖于命令行工具，另外克隆仓库路径有区别
在ssh密钥模式下，mac的克隆指令为
git clone ssh://git@serverIP/srv/test.git

win/ubuntu可用 git clone git@serverIP:srv/test.git
mac用这个的话会报错
fatal: 'srv/test.git' does not appear to be a git repository
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
and the repository exists.

git有时会有数字
设置一下 git config --global core.quotepath false

服务器新建用户时权限.ssh/authorized_keys 可以给0644
