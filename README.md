# Clouddrive-2
## 本教程使用VPS信息 Operating system: debian-12-x86_64 2c1g
1.下载最新安装包
```bash
wget https://github.com/cloud-fs/cloud-fs.github.io/releases/download/v0.5.9/clouddrive-2-linux-x86_64-0.5.9.tgz
```

2.解压安装包
```bash
tar zxvf clouddrive-2-linux-x86_64-0.5.9.tgz 
```

3.删除安装包
```bash
rm ~/clouddrive-2-linux-x86_64-0.5.9.tgz
```
4.配置开机启动
```bash
vim /etc/systemd/system/clouddrive.service

写入以下内容
[Unit]
Description=clouddrive service
Wants=network.target
After=network.target network.service

[Service]
Type=simple
WorkingDirectory=/root/clouddrive-2-linux-x86_64-0.5.9
ExecStart=/root/clouddrive-2-linux-x86_64-0.5.9/clouddrive server
KillMode=process

[Install]
WantedBy=multi-user.target

# 刷新systemd 配置文件
systemctl daemon-reload
