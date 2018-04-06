# install && config ss:

1. 安装ssserver（Python2.6或者2.7）
官方提供的方法如下：
如果你没有pytho可以直接安装，命令行如下：（默认的应该是python2.7我记得）
```bash
sudo -s
apt update
apt install python python-pip
```


2. 安装ssserver：
```bash
pip install shadowsocks
```

3. 编辑配置文件
```bash
mkdir /etc/shadowsocks/
cd /etc/shadowsocks/
vi config.json
```
```json
// 内容如下：
{
    "server":"0.0.0.0",
    "server_port":8388,
    "local_port":1080, 
    "password":"~123456!",
    "timeout":600,
    "method":"aes-256-cfb",
    "fast_open":false
}
```

4. 以守护进程启动ssserver  (stop 停止；restart 重启)
```bash
ssserver -c /etc/shadowsocks/config.json -d start
```