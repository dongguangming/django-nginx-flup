#注意事项:
1. When you need to manage Nginx or Django daemon process through a init RHEL/CentOS script, create the following nginx or django file on /etc/init.d/ system path, and, then, you can use service or systemctl commands to manage the process.

    * touch /etc/init.d/nginx.sh
    * touch /etc/init.d/django.sh

2.  After the Nginx or Django init file is created, append executions permissions and manage the daemon using the below command options.

    * chmod +x /etc/init.d/nginx.sh
    * chmod +x /etc/init.d/django.sh
    
3. create the following nginx.service or django.service file on /usr/lib/systemd/system system path, and then 
    * ###chmod 754 /usr/lib/systemd/system/nginx.service
    * ###chmod 754 /usr/lib/systemd/system/django.service
    * service nginx start|stop|restart|reload|force_reload|configtest|condrestart
    * systemctl daemon-reload    
    * systemctl start|stop|restart nginx

4.  If you need to enable Nginx system-wide use the following command to start at boot time.(开机启动)

    * chkconfig nginx on
    * chkconfig django on

      OR

    * systemctl enable nginx
    * systemctl enable django

#参考：
1. [Linux Systemd——在RHEL/CentOS 7中启动/停止/重启服务](https://linux.cn/article-3719-1.html '')
2. [Ubuntu 15.04 /CentOS 7.0设置自定义开机启动](http://welloong.com/293.html '')
3. [RHEL/CentOS 7.x的几点新改变](http://www.ha97.com/5657.html '')
4. [systemd (简体中文)](https://wiki.archlinux.org/index.php/systemd_%28%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87%29 '')
5. [鸟哥的Liunx私房菜之认识系统服务 (daemons)](http://linux.vbird.org/linux_basic/0560daemons.php '')