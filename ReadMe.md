
## filebeat 

在filebeatop.yml 中指定要操作的机器组，以及filebeat的版本，日志输出的logstahsh端点。
在group_vars 中定义每个机器组上需要采集的日志路径

安装filebeat软件包
```shell
ansible-playbook -i hosts    filebeatop.yml --tags "install"
```

安装filebeat service
```shell
ansible-playbook -i hosts    filebeatop.yml --tags "rpm"
```

更新filebeat配置文件
```shell
ansible-playbook -i hosts    filebeatop.yml --tags "updatecfg"
```

## node exporter 
每台机器都装上 node exporter 配置端口