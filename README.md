# Clouddrive-2

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

#写入以下内容
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

#如果你不会使用vim,按以下方式直接下载service文件
1.cd/etc/systemd/system/
2.wget https://github.com/MHY2233/Clouddrive-2/blob/main/clouddrive.service

# 刷新systemd 配置文件
systemctl daemon-reload

#设置clouddrive开机自启
systemctl enable clouddrive
```
