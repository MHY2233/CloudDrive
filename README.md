# Clouddrive-2

1.下载最新安装包
```bash
wget https://github.com/cloud-fs/cloud-fs.github.io/releases/download/v0.5.9/clouddrive-2-linux-x86_64-0.5.9.tgz
```

2.解压安装包
```bash
tar -zxvf clouddrive-2-linux-x86_64-0.5.9.tgz -C /usr/local/bin/
```

3.删除安装包
```bash
rm ~/clouddrive-2-linux-x86_64-0.5.9.tgz
```
4.配置开机启动
    
    curl -Lo /etc/systemd/system/clouddrive.service https://raw.githubusercontent.com/MHY2233/clouddrive-install/main/clouddrive.service

5.刷新systemd 配置文件
systemctl daemon-reload

6.开启clouddrive
systemctl start clouddrive

7.运行clouddrive开机自启
systemctl enable clouddrive

在浏览器上输入 你的ip:19798
