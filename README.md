# 介绍
我是在github另外一个项目上找到的`https://github.com/timwhitez/crawlergo_x_XRAY`
就是用crawlergo动态爬虫配合xray进行批量扫描，但是我使用的平台是`Linux`，所以稍微魔改了一下
为了防止断开ssh连接后，进程结束，建议在`screen`中进行

# 使用方法
```
xray下载地址：
https://github.com/chaitin/xray/releases
crawlergo下载地址：
https://github.com/0Kee-Team/crawlergo
chrome-linux下载地址：
https://storage.googleapis.com/chromium-browser-snapshots/Linux_x64/706915/chrome-linux.zip
```
`脚本要和crawlergo同目录，xray只需要启动后挂载后台即可`
crawlergo需要使用chrome来进行爬取，在上面下载`chrome-linux`后解压，然后把launcher.py中30行对应的路径进行修改即可
![](https://raw.githubusercontent.com/Ernket/crawlergo-XRAY/master/img/pic1.png)

修改配置完成后，开启xray（因为脚本关系，默认的端口是7778，若要变更修改对应端口即可）
```
./xray webscan --listen 127.0.0.1:7778 --html-output xray.html &
```
targets.txt文件是批量扫描的，只需要存放域名即可
安装脚本所需要的库
```
pip3 install -r requirements.txt
```
运行脚本
```
python3 launcher.py &
```
