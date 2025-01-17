# 湖北工业大学校园网一键登录

---

这是一个自动登录校园网程序，配合开机自启，可以做到每次打开电脑自动登录校园网，无需手动打开网页点击登录，目前支持湖北工业大学（深澜校园网）

## 怎么使用？

1. 下载[最新Release](https://github.com/lty2002/HBUT_auto_login_network/releases/tag/latest)中对应版本的可执行文件
    ```
    main-linux-amd64 (Linux)
    main-macos-amd64 (macOS-Intel)
    main-macos-arm64 (macOS-Apple)
    main-windows-amd64.exe (Windows)
    ```
2. 在可执行文件同目录下创建user.txt文件，在其中加入两行文本：
    ```
    学工号@运营商
    密码
    ```
    
    其中，运营商处按下列规则填写：
    ```
    校园网：连同前面的@，均不填写
    中国移动：cmcc
    中国电信：ctcc 
    中国联通：cucc 
    ```
    
    如：学工号为100000，密码为999999 
      - 校园网
          ```
          100000
          999999
          ```
      - 中国移动宽带
          ```
          100000@cmcc
          999999
          ```
3. 执行程序

    (Linux, macOS)
    ```shell
    cd /path/to/executable_file
    chmod +x path_to_main
    ./path_to_main
    ```
    
    (Windows)
    ```
    运行main-windows-amd64.exe（双击图标或执行命令）
    ```
4. 若终端显示`login success`或弹出系统通知则登录成功
   ```
   2023-03-24T10:18:39 IP: 10.9.103.2
   2023-03-24T10:18:39 logout success
   2023-03-24T10:18:39 IP: 10.9.103.2
   2023-03-24T10:18:39 login success
   ```

### 注意

- 操作前务必先连接校园网
- 若要实现开机自启，请设置校园网WIFI自动连接或有线连接
- Linux平台桌面通知功能需要[安装对应依赖](https://command-not-found.com/notify-send)

## 鸣谢

本项目Fork自：
- [https://github.com/Debuffxb/srun-go](https://github.com/Debuffxb/srun-go)
- [https://github.com/shadowfish07/HBUT_auto_login_network](https://github.com/shadowfish07/HBUT_auto_login_network)
