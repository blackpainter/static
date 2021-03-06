# image
图片服务

* 微信
  * https://raw.githubusercontent.com/WALL-E/static/master/images/wx-big.jpg
  * https://raw.githubusercontent.com/WALL-E/static/master/images/wx-middle.jpg
  * https://raw.githubusercontent.com/WALL-E/static/master/images/wx-small.jpg

# isos
镜像服务

* centos 7.2.1511
  * http://ok9kfhw61.bkt.clouddn.com/CentOS-7-x86_64-Minimal-1511.iso
  
* centos 6.9
  * http://ok9kfhw61.bkt.clouddn.com/CentOS-6.9-x86_64-minimal.iso
  
* centos 6.8
  * http://ok9kfhw61.bkt.clouddn.com/CentOS-6.8-x86_64-minimal.iso

# setup
安装服务

* jekyll
  * CentOS-7
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_jekyll|bash
    ```

* tmux-2.5
  * CentOS
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_tmux|bash
    ```

* kong-dev-kit
  docker images
  ```
  wget http://opduyrvvz.bkt.clouddn.com/kongdevkit.md5sum
  wget http://opduyrvvz.bkt.clouddn.com/kongdevkit_dashboard.tar.gz
  wget http://opduyrvvz.bkt.clouddn.com/kongdevkit_kong.tar.gz
  wget http://opduyrvvz.bkt.clouddn.com/kongdevkit_httpbin.tar.gz
  wget http://opduyrvvz.bkt.clouddn.com/kongdevkit_postgres.tar.gz
  wget http://opduyrvvz.bkt.clouddn.com/kongdevkit_postgres_tests.tar.gz

  cat export.tar | docker import - kongdevkit:latest
  ```

* sock
  ```
  wget http://opduyrvvz.bkt.clouddn.com/sock
  chmod +x sock
  ```
  
* iproute2
  ```
  git clone git://git.kernel.org/pub/scm/linux/kernel/git/shemminger/iproute2.git
  make && make install
  ```
 
* PyTorch
  * Centos-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_pytorch|bash
    ```

* 文件中转站（redhat/centos x86-64）
  ```
  yum install libssh-devel.x86_64
  wget http://oerp142a4.bkt.clouddn.com/zshell?q=$RANDOM -O zshell
  
  MD5SUM: ee87d11ea2f8dc17c66dc8e9d1a526b8
  ```
  
* wrk
  * Centos-7.x
    ```
    wget http://oerp142a4.bkt.clouddn.com/wrk-centos7
    mv wrk-centos7 wrk
    chmod +x wrk
    ```
  * Centos-6.x
    ```
    wget http://oerp142a4.bkt.clouddn.com/wrk-centos6
    mv wrk-centos6 wrk
    chmod +x wrk
    ```

* Systemtap
  * CentOS-7.x
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_systemtap|bash
    ```

* JDK
  * CentOS-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_jdk7|bash

    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_jdk8|bash
    ```

* Python27
  * CentOS-6.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_python27|bash
    ```
    
* Python3.6 & easy_install-3.6 & pip3.6
  * CentOS-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_python36|bash
    ```

* Pip27
  * CentOS-6.x, CentOS-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_pip27|bash
    ```

* Supervisor
  * CentOS-6.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_supervisor|bash
    ```



* Cassandra
  * CentOS-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_cassandra|bash
    ```

* Kong
  * CentOS-7.x
    
    ```
    yum install -y http://oerp142a4.bkt.clouddn.com/kong-0.9.5.el7.noarch.rpm
    ```

* influxDB
  * CentOS-7.x
    
    ```
    yum install -y http://oerp142a4.bkt.clouddn.com/influxdb-1.0.0.x86_64.rpm
    ```

* OpenResty
  * CentOS-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_openresty|bash
    
    官方版本
    https://openresty.org/en/linux-packages.html
    ```

* Harbor
  * CentOS-7.x
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_harbor|bash
    ```

  * Ubuntu-14-04.5
    
    ```
    curl https://raw.githubusercontent.com/WALL-E/static/master/setup/ubuntu/install_harbor|bash
    ```


* docker-machine and docker
```
  
  Ref: https://github.com/docker/machine/releases
  阿里云安装脚本
  curl -sSL http://acs-public-mirror.oss-cn-hangzhou.aliyuncs.com/docker-engine/internet | sh -
  
  wget http://opduyrvvz.bkt.clouddn.com/docker-machine-Linux-x86_64_0.12.2
  mv docker-machine-Linux-x86_64_0.12.2 /usr/local/bin/docker-machine
  chmod +x /usr/local/bin/docker-machine

  curl https://raw.githubusercontent.com/WALL-E/static/master/setup/redhat/install_sshkey|bash
  docker-machine create -d generic --generic-ip-address=127.0.0.1 --generic-ssh-user=root dockerHost
  ```
  

* docker-compose
 
  ```
  wget http://oerp142a4.bkt.clouddn.com/docker-compose-Linux-x86_64_1.12.0
  mv docker-compose-Linux-x86_64_1.12.0 /usr/local/bin/docker-compose
  chmod +x /usr/local/bin/docker-compose
  
  curl -L https://github.com/docker/compose/releases/download/1.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
  chmod +x /usr/local/bin/docker-compose
  ```
  
* consul
 
   ```
   wget http://oerp142a4.bkt.clouddn.com/consul_0.7.0_linux_amd64.zip
   unzip consul_0.7.0_linux_amd64.zip
   sudo cp consul /usr/local/bin/
   ```
