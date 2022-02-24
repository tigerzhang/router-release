# 升级

* 系统 -> 备份/升级 -> 刷写新的固件
* `保留配置` 不选择
* 点击`选择文件`选择固件，点击`刷写固件`
* 确认 sha256 校验码

# sha256 校验码

* openwrt-ramips-mt76x8-u7628-01-128M-16M-squashfs-sysupgrade-20211123.bin - f3ebbf4c60f372b6294b9d4f8a83c38eb1a40a7bfd8358cd8f28093601e35369
* openwrt-ramips-mt76x8-u7628-01-128M-16M-squashfs-sysupgrade-20211129.bin - f5b8c0a363eee403c554eae242e1f6bc7a8c23acd6388316e3cbc27a192e34c8

# APN

不同国家的 `APN` 不一样，需要对应修改。APN 修改在：网络 -> 接口 -> ppp0

## 中国

3gnet

## 泰国

m2minternet

# 泰国卡运营商选择

泰国卡在国内测试，必须指定运营商为 `联通`

指定运营商为联通

用浏览器打开链接

```
http://192.168.1.1/cgi-bin/chinaunicom.cgi
```

返回

```
switch to china unicom
AT+COPS=1,2,"46001",
OK
```

表示切换成功。

重启设备即可

# 测试

```
http://192.168.1.1/cgi-bin/token.lua?token=<token>
```

# 平台

```
http://tete-server.yunba.io/devices
```

# 串口修改密码

* 连接串口
* 敲一下 回车

```
BusyBox v1.28.3 () built-in shell (ash)

  _______                     ________        __
 |       |.-----.-----.-----.|  |  |  |.----.|  |_
 |   -   ||  _  |  -__|     ||  |  |  ||   _||   _|
 |_______||   __|_____|__|__||________||__|  |____|
          |__| W I R E L E S S   F R E E D O M
 -----------------------------------------------------
 OpenWrt SNAPSHOT, r6873-cf7a88c
 -----------------------------------------------------
root@WZY:/# passwd
```
* 连续输入两次新密码

