yum 源：
我的解决方法是修改默认yum源为阿里云yum源，亲测有效。
步骤如下：

备份原有yum源：

    mv /etc/yum.repos.d /etc/yum.repos.d.bak
复制代码
创建yum源目录

   mkdir /etc/yum.repos.d
复制代码
下载阿里云yum源配置

   wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
复制代码
重建缓存

   yum clean all
复制代码  yum makecache
