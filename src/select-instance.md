# select instance

1. Ubuntu Server 16.04 LTS (HVM), SSD Volume Type - ami-916f59f4
2. 选择“在没有密钥的时候继续”

3. 找到“安全组”
4. 配置以下信息：操作-编辑入站规则
![](2018-04-07-00-30-48.png)
```conf
SSH           TCP 22     0.0.0.0/0
自定义TCP规则   TCP 8388   0.0.0.0/0
```


## resouces:
+ https://blog.csdn.net/f59130/article/details/74014415
+ https://blog.csdn.net/liangxun0712/article/details/78840964