# connect with pem
> https://www.cnblogs.com/Jason-Born/p/6566503.html

1. 命令如下
```bash
ssh -i key.pem 
ssh -i key.pem root@IP
```

2. 如果出现报错说明这个问题是文件的权限太大了，需要给小点 
```bash
sudo chmod 600 key.pem 
ssh -i key.pem root@IP
```

3. 可以使用ssh-add 添加key文件
```bash
ssh-add -k key.pem  
```

4. 正常登录堡垒机
```bash
ssh root@IP
```
