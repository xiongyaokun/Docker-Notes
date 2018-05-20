## Vagrant Documentation

### [getting started guide](https://www.vagrantup.com/intro/getting-started/index.html)

### [VirtualBox](https://www.virtualbox.org/)

### [install the latest version of Vagrant](https://www.vagrantup.com/docs/installation/)

### Up and Running

<pre>
$ vagrant init hashicorp/precise64
$ vagrant up #初始化
$ vagrant ssh #以ssh登录
</pre>

### Project Setup

#### **Vagrantfile**的作用
1. 记录你的项目的根目录。Vagrant里的很多设置选项都和这个根目录相关
2. 描述你的项目所需机器、资源的类型，以及你需要安装的软件和你怎么进入这个项目虚拟机。

<pre>
$ mkdir vagrant\_getting\_started #创建项目的根目录
$ cd vagrant\_getting\_started #进入根目录
$ vagrant init # 在根目录生成一个Vagrantfile的文件
</pre>

### Boxes


<pre><code>
$ vagrant box list #列出已经add的box
$ vagrant box add hashicorp/precise64 #添加box
</code></pre>

