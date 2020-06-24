# 检查Linux 磁盘健康

## 参考链接 

- http://www.imooc.com/article/247258

```bash
sudo -i

# 安装工具
apt-get install smartmontools

# 列举挂在的磁盘
ls -l /dev | grep -E 'sd|hd'

# 显示磁盘详细信息
smartctl --info /dev/sda
smartctl --info /dev/sdb

# 开启磁盘监控，并显示检查结果
smartctl -s on -a /dev/sda
smartctl -s on -a /dev/sdb
```
