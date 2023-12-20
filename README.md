- **1.下载程序最新的releases**

        wget https://github.com/cloud-fs/cloud-fs.github.io/releases/download/v0.5.14/clouddrive-2-linux-x86_64-0.5.14.tgz && tar -zxvf clouddrive-2-linux-x86_64-0.5.14.tgz -C /usr/local/bin/ && rm ~/clouddrive-2-linux-x86_64-0.5.14.tgz

- **2.配置开机启动**
    
        curl -Lo /etc/systemd/system/clouddrive.service https://raw.githubusercontent.com/MHY2233/clouddrive-install/main/clouddrive.service && systemctl daemon-reload

- **3.开启clouddrive**

        systemctl start clouddrive

- **4.运行clouddrive开机自启**

        systemctl enable clouddrive

- **5.查看运行状态**

        systemctl status clouddrive

- **10.在浏览器上输入 你的ip:19798**
