mac 下查看端口监听 lsof -i :9000
ps aux |grep php-fpm
netstat -ant |grep 9000

当前目录传入文件 rz -be
统计行数 cat file | wc -l
获取主机 ip hostname -i
压缩文件tar -czvf travel1.tar.gz travel1
解压文件tar -xzf travel1.tar.gz
服务器之间文件传输：

- scp travel1.tar.gz root@123.57.149.81:/home/dbceshi
- scp -r city.txt chenjun16@cp01-rdqa04-dev106.cp01.baidu.com:/home/users/chenjun16/
- scp -r 31030 chenjun16@cp01-rdqa04-dev106.cp01.baidu.com:/home/users/chenjun16/

wget -r cp01-testing-mapse28.cp01.baidu.com:/home/map/py_test

查看容量 df -h
查看当前目录下所有文件的大小 ls -lht
查看服务和端口号 netstat -npl
筛选相关的进程ps -aux|grep 关键词
sudo lsof -i :9000mac下查看某个端口被程序占用
du –sh   查看当前目录所占空间
du –sh file 或者du –sh * 查看某些文件或全部文件所占空间
linux上卸载sudo apt-get remove mongodb-10gen
linux上安装sudo apt-get install H
杀进程 killall -9 NAME
查看进程 ps -eo user,pid,stat,rss,args
修改默认编辑器export EDITOR=vi
创建文件夹：sudo mkdir -p nosql/mongodb
修改文件权限：sudo chmod -R 777 yoyocloud

加环境变量：export PATH="~/.composer/vendor/bin:vendor/bin:$PATH"
修改环境变量 export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin/:/sbin:/bin:/usr/game:$PATH
