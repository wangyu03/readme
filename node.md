
- `wget https://nodejs.org/dist/v6.10.3/node-v6.10.3-linux-x64.tar.xz`  
- `tar xvJf node-v6.10.3-linux-x64.tar.xz`下载完成后, 将其解压
- `mv node-v6.10.3-linux-x64 /usr/local/node-v6`将解压的 Node.js 目录移动到 /usr/local 目录下
- `ln -s /usr/local/node-v6/bin/npm /bin/npm` 下载 node 的压缩包中已经包含了 npm , 我们只需要将其软链接到 bin 目录下即可 
- `echo 'export PATH=/usr/local/node-v6/bin:$PATH' >> /etc/profile`  将 /usr/local/node-v6/bin 目录添加到 $PATH 环境变量中可以方便地使用通过 npm 全局安装的第三方工具
- `source /etc/profile`生效环境变量  
- `npm install forever -g`  通过 npm 安装进程管理模块 forever