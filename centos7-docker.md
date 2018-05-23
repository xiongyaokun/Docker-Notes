## Centos7 install Docker

### sudo yum update 不一定需要的

### yum install docker

### docker --version 查看版本
 

### docker verson 查看client, service 是否运行

### 错误代码,提时docker权限不够

<pre>
Client:
 Version:         1.13.1
 API version:     1.26
 Package version:
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.26/version: dial unix /var/run/docker.sock: connect: permission denied
</pre>

### 查看docker的权限

<pre>
$ cd /var/run
$  ll | grep docker.sock

srw-rw----  1 root   root      0 23. Mai 10:24 docker.sock
</pre>

### 解决方法如下：

<pre>
$ sudo group add docker 添加一个docker group
$ sudo gpasswd -a ${USER} docker
$ sudo service docker restart
$ newgrp - docker
</pre>

**注意：**最后一步是必须的，否则因为groups命令获取的是缓存的组信息，刚添加的组信息未能生效，所以，docker images执行时同样有错误

或者重新启动系统也可以。


