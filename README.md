一、配置SSH参数
修改sshd_config文件，命令为：

nano /etc/ssh/sshd_config

将PermitRootLogin without-password修改为PermitRootLogin yes

kali 这一步不需要 将#PasswordAuthentication no的注释去掉，并且将NO修改为YES //kali中默认是yes

然后保存退出nano编辑器。

設定系統開機時自動啟動 SSH
sudo systemctl enable ssh


二、启动SSH服务

sudo systemctl start ssh

# 檢查服務狀態
sudo systemctl status ssh

# 檢查監聽端口
netstat -tulpn | grep ssh


二、启动SSH服务
命令为：/etc/init.d/ssh start 

或者service ssh start

查看SSH服务状态是否正常运行，命令为：

/etc/init.d/ssh status


