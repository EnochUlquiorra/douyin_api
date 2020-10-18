
#### 命令行启动文件
```casbin

MacOS   64位 douyin-tools-darwin-amd64
Linux   64位 douyin-tools-linux-amd64
Windows 64位 douyin-tools-windos-amd64.exe


config.toml文件为测试授权key,源码部分包括全部
token有效期为3天

```


##### 设备注册
```casbin
http://127.0.0.1:5008/api/device_register
```
返回结果
```casbin
{"Info":{"ac":"wifi","appTheme":"dark","app_name":"aweme","app_type":"normal","cpu_support64":false,"device_platform":"android","device_type":"MI 4LTE","host_abi":"armeabi-v7a","mac_address":"CA:A9:97:33:E1:D8","ssmix":"a","storage_type":2,"version_name":"13.0.0","display_name":"抖音短视频","update_version_code":13009900,"manifest_version_code":130001,"app_version_minor":"","aid":1128,"channel":"xiaomi","appkey":"57bfa27c67e58e7d920028d3","package":"com.ss.android.ugc.aweme","app_version":"13.0.0","version_code":130000,"sdk_version":"2.14.0-rc.1-oai","sdk_target_version":29,"git_hash":"63251490","os":"Android","os_version":"6.0.1","os_api":23,"device_model":"MI 4LTE","device_brand":"Xiaomi","device_manufacturer":"Xiaomi","cpu_abi":"armeabi-v7a","build_serial":"171b3743","release_build":"c88a9f2_20200926_c6ab8d3e-ffb7-11ea-a696-02420a00001c","density_dpi":480,"display_density":"mdpi","resolution":"1920x1080","language":"zh","timezone":8,"access":"wifi","not_request_sender":0,"rom":"MIUI-8.9.13","rom_version":"miui_V10_8.9.13","cdid":"01fae659-c4dd-4ca4-9ff2-69947aad7b3a","sig_hash":"aea615ab910015038f73c47e45d21466","openudid":"03f815f89584248a","clientudid":"f74dc0c3-f076-40df-a520-bf21b53afb8a","uuid":"e0b63612c51984bf","serial_number":"171b3743","sim_serial_number":[],"region":"CN","tz_name":"Asia/Shanghai","tz_offset":28800,"sim_region":"cn","oaid_may_support":false,"req_id":"01ac7e92-8e7c-4a8a-a22c-92c864411d08","custom":{"filter_warn":0},"apk_first_install_time":1602302308335,"is_system_app":0,"sdk_flavor":"china","cpu_model":"OMAP4 Panda board","k6":"5e9478922f227a","k8":"bcb183e8a0c54e","boot_image_build_date_unix":-29501697692,"boot_image_build_date_utc":"Feb Tue 17 12:04:11 UTC 1035","push_sdk":[1,2,6,7,8,9],"finger_print":"Xiaomi/cancro_wc_lte/cancro:6.0.1/MMB29M/8.9.13:user/release-keys","wifi_info":{"wifisid":"pvcbu9EcZce5ho82","wifimac":"7A:31:96:32:E6:27","wifgip":"192.168.1.1","wifiiip":"192.168.196.153"}},"Header":{"display_name":"抖音短视频","update_version_code":13009900,"manifest_version_code":130001,"app_version_minor":"","aid":1128,"channel":"xiaomi","appkey":"57bfa27c67e58e7d920028d3","package":"com.ss.android.ugc.aweme","app_version":"13.0.0","version_code":130000,"sdk_version":"2.14.0-rc.1-oai","sdk_target_version":29,"git_hash":"63251490","os":"Android","os_version":"6.0.1","os_api":23,"device_model":"MI 4LTE","device_brand":"Xiaomi","device_manufacturer":"Xiaomi","cpu_abi":"armeabi-v7a","build_serial":"171b3743","release_build":"c88a9f2_20200926_c6ab8d3e-ffb7-11ea-a696-02420a00001c","density_dpi":480,"display_density":"mdpi","resolution":"1920x1080","language":"zh","mc":"CA:A9:97:33:E1:D8","timezone":8,"access":"wifi","not_request_sender":0,"rom":"MIUI-8.9.13","rom_version":"miui_V10_8.9.13","cdid":"01fae659-c4dd-4ca4-9ff2-69947aad7b3a","sig_hash":"aea615ab910015038f73c47e45d21466","device_id":"2269014361647613","install_id":"773678547869085","openudid":"03f815f89584248a","clientudid":"f74dc0c3-f076-40df-a520-bf21b53afb8a","serial_number":"171b3743","sim_serial_number":[],"region":"CN","tz_name":"Asia/Shanghai","tz_offset":28800,"sim_region":"cn","oaid_may_support":false,"req_id":"01ac7e92-8e7c-4a8a-a22c-92c864411d08","custom":{"filter_warn":0},"apk_first_install_time":1602302308335,"is_system_app":0,"sdk_flavor":"china"},"SdfpToken":"","DeviceID":"2269014361647613","InstallID":"773678547869085"}
```

获取device_id值

参数
http://127.0.0.1:5008/api/do/user/search/device_id/搜索用户昵称或用户ID的关键字
##### 用户搜索
```casbin
http://127.0.0.1:5008/api/do/user/search/2761593599040472/我爱111
```

参数
http://127.0.0.1:5008/api/do/user/search/device_id/用户的安全ID
##### 用户信息
```casbin
http://127.0.0.1:5008/api/do/user/profile/2761593599040472/MS4wLjABAAAAe6EmALH507QLnJLXXbMvGuV_zQ9hEai-LsE3SHLhIrPTZ8zOKcdCPE6yjVCYiudm
```

参数
http://127.0.0.1:5008/api/do/user/search/device_id/用户的安全ID
##### 用户视频
```casbin
http://127.0.0.1:5008/api/do/user/post/2761593599040472/MS4wLjABAAAAe6EmALH507QLnJLXXbMvGuV_zQ9hEai-LsE3SHLhIrPTZ8zOKcdCPE6yjVCYiudm
```

登录的第一种情况
```casbin
发送短信验证码
http://127.0.0.1:25008/api/do/login/send_sms/1806********
通过接收到的短信验证码登录
http://127.0.0.1:25008/api/do/login/send_sms/1806********/1223
```

登录的第二种情况
```casbin
发送短信验证码
http://127.0.0.1:25008/api/do/login/send_sms/1806********
通过主动发送短信验证码
http://127.0.0.1:25008/api/do/login/send_sms/1806********/tick码
```