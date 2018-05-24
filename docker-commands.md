## Docker Commands Learning

## [docker中国](http://www.simapple.com/docker)

### 启动docker
<pre>
$ sudo service docker start
</pre>

### 设置开机启动
<pre>
$ sudo groupadd docker
$ sudo useradd -g ${USER} docker
</pre>

<pre>
$ docker --help
</pre>

<pre>
$ docker version
$ docker --version
$ docker search tutorial # docker search [镜像名]

$ docker pull learn/tutorial # docker pull [镜像名]

$ docker run learn/tutorial echo "hello world!"
$ docker run -it learn/tutorial # 进入到镜像运行的容器内
$ exit #
</pre>


<pre>
$ docker run learn/tutorial apt-get install -y ping
$ docker ps -l
$ docker commit 698 learn/ping

$ docker run learn/ping www.google.com
</pre>

<pre>
$ docker ps # 查看所有正在运行的容器
$ docker inspect 989 # 查看关于某个容器的详细信息
</pre>

<pre>
$ docker images list # docker images 列出所有安装的镜像
$ docker push learn/ping # 只能将镜像发布到自己的账号下面，这个是模拟的learn账号

</pre>


### docker tag
<pre>
docker tag old-image-repostory[:old-tag] new-image-repository[:new-tag]
或者
docker tag old-image-id new-image-repository[:new-tag]
</pre>


### docker commit 提交一个存在的容器,生成image
<pre>
$ docker ps # 列出运行的容器

Usage: docker commit [OPTIONS] CONTAINER\_ID [REPOSITORY[:TAG]]
$ docker commit c3f279 SvenDowideit/testimage:version3
</pre>
