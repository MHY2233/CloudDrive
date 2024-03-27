# [查看最新发行版](https://github.com/cloud-fs/cloud-fs.github.io/releases)

- **1.安装程序**

        wget https://github.com/cloud-fs/cloud-fs.github.io/releases/download/v0.6.9/clouddrive-2-linux-x86_64-0.6.9.tgz && tar -zxvf clouddrive-2-linux-x86_64-0.6.9.tgz -C /usr/local/bin/ && rm ~/clouddrive-2-linux-x86_64-0.6.9.tgz

- **2.配置开机启动**
    
        curl -Lo /etc/systemd/system/clouddrive.service https://raw.githubusercontent.com/MHY2233/clouddrive-install/main/clouddrive.service && systemctl daemon-reload

- **3.启动clouddrive**

        systemctl enable --now clouddrive

- **4.查看运行状态**

        systemctl status clouddrive

- **5.在浏览器上输入 你的ip:19798**
