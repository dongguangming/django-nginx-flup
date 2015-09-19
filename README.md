# django-nginx-flup
CentOS7, Python, Django1.4, nginx1.6, FastCGI(flup).

#1. Python安装
   1. [Installing Python on Linux](http://docs.python-guide.org/en/latest/starting/install/linux/ '')
#2. Django安装
   1. [Install Django](https://docs.djangoproject.com/en/1.8/intro/install/ '')
   2. [How to install Django](https://docs.djangoproject.com/en/1.8/topics/install/ '')
#3. Flup安装
   1. [PythonFlup](http://wiki.nginx.org/PythonFlup '')
   2. [django-nginx-mysql-install-and-config-on-centos](https://raw.githubusercontent.com/qloog/lnmp100.github.io/master/content/note/django-nginx-mysql-install-and-config-on-centos.md '')
   3. [Flup](http://www.saddi.com/software/flup/dist/ '')
   4. [python / flup and fastcgi](https://www.geoffreybrown.com/blog/python-flup-and-fastcgi/ '')
#4. Nginx安装
   1. [Nginx Install](http://wiki.nginx.org/Install '')
   2. [Nginx安装](http://www.nginx.cn/install '')
   3. [How to Install and Configure Nginx from Source on Linux](http://www.thegeekstuff.com/2011/07/install-nginx-from-source/ '')
   4. [Install and Compile “Nginx 1.6.0” (Newest Released) from Sources in RHEL/CentOS 7.0](http://www.tecmint.com/install-nginx-in-centos-7/ '')

#参考
1. [Apache, FastCGI and Python](http://www.electricmonk.nl/docs/apache_fastcgi_python/apache_fastcgi_python.html '')
1. [Django on Nginx](https://wiki.freebsdchina.org/doc/n/nginx_django '')
2. [A (Complete) Guide to Running Django on Joyent Shared Accelerators using Virtualenv, pip, git, and NginX](https://evancarmi.com/writing/django-on-joyent/ '')
3. [Django FastCGI](http://wiki.nginx.org/DjangoFastCGI '')
4. [Django FastCGI init.d script for Linux ](https://code.djangoproject.com/wiki/InitdScriptForLinux '')
5. [LEMP server on CentOS 7 with FastCGI](https://www.linode.com/docs/websites/lemp/lemp-server-on-centos-7-with-fastcgi '')

#帮助
1. linux readlink命令，例子如下：
   * [root@supoolstor bin]# pwd
   * /usr/bin
   * [root@supoolstor bin]# ll|grep python
   * lrwxrwxrwx. 1 root root       7 Jul 14 10:13 python -> python2
   * lrwxrwxrwx. 1 root root       9 Jul 14 10:13 python2 -> python2.7
   * -rwxr-xr-x. 1 root root    7136 Jul 14 10:13 python2.7
   * -rwxr-xr-x. 1 root root    1835 Jun 18  2014 python2.7-config
   * lrwxrwxrwx. 1 root root      16 Jul 14 11:06 python2-config -> python2.7-config
   * lrwxrwxrwx. 1 root root      14 Jul 14 11:06 python-config -> python2-config
   * [root@supoolstor bin]# readlink python
   * python2
   * [root@supoolstor bin]# readlink -f python
   * /usr/bin/python2.7

2. linux basename命令，例子如下：
   * [root@supoolstor bin]# basename /dgm/hello.py .py
   * hello
   * [root@supoolstor bin]# basename /dgm/hello.py
   * hello.py
   * [来自维基百科 ](https://en.wikipedia.org/wiki/Basename '')
