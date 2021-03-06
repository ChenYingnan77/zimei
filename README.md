# 自美系统

## **介绍**
>自美智能系统是基于树莓派、Python、HTML5、PHP、微信小程序打造出的一款物联网人工智能系统，目前系统已实现：语音唤醒、语音识别、语音合成、人体探测、人脸识别、人脸对比、智能互动、插件式功能扩展等全套人工智能交互功能。
自美系统可方便的扩展为：智能家居集控系统、交互人工智能设备（如魔镜 / 挂历 / 服务机器人）、生产工作流程监控和控制系统等功能，自美人工智能系统现已面向全球开源，源码发布至国外GitHub和国内Gitee开源平台，欢迎广大开发者下载测试和进行二次开发。
自美目标致力于打造更实用的人工智能系统，小生态大用途！

自美系统同时在Gitee、GitHub开源平台发布：

Gitee(国内)：https://gitee.com/kxdev/zimeimojing

GitHub(国外)：https://github.com/drbdrb/zimei

## **软件架构**
自美人工智能系统基于树莓派官方系统构建，应用Python、JavaScript、PHP、Mqtt、微信小程序等技术架构。

## **安装教程**

1. **系统配置**

    为提升树莓派开发人工智能系统用户体验，自美系统需配合驱动板，驱动板可以上本站[淘宝店铺购买](https://item.taobao.com/item.htm?spm=a1z10.1-c-s.w137712-22051699657.2.5a866a2dcy4XWC&id=600751373947)

2. **系统部署**

    自美系统可使用两种方式安装：

    方式一：镜像安装（方便快捷），具体安装方法请浏览：[http://docs.16302.com/1144905](http://docs.16302.com/1144905)
    
    方式二：源码安装（适合有一定的Linux操作经验和编程基础的用户），具体安装方法请浏览：[http://docs.16302.com/1318686](http://docs.16302.com/1318686)

3. **首次启动**
    第一次启用系统会提示用微信扫描绑定设备：
<br/><img src="http://qiniucn.16302.com/cebf6a2e00280c328c045d66076a60d4" width="500" border="0" /><br/>
    并有语音提示：我已经准备好了，你可以与我互动啦！即为安装成功。

## **使用说明**
### 自美系统已经具备以下功能：
 * 语音唤醒
 * 语音对话、机器人语音互动
 * 人体探测
 * 人脸识别、人脸对比
 * 语音+微信调节音量
 * 语音开关灯功能
 * 播放歌曲功能
 * 播放笑话功能
 * 播放百科功能
 * 语音股市查询功能
 * 天气预报功能
 * 屏幕显示万年历
 * 屏幕显示天气情况
 * 语音+微信设置城市地址功能
 * 微信小程序控制功能
 * 打开风扇功能
 * 打开灯功能
 * 电路控制功能
 * 快速配网功能
 * 二次开发插件扩展功能

### 文件结构说明：
```python
├── app                             # 前端显示相关文件夹
├── install.py                          # 安装文件
├── LICENSE                             # 开源协议文件
├── python                              # Python源码文件夹
│   ├── api                         # HTTP接口文件夹
│   │   ├── BDaip                       # 百度接口
│   │   ├── snowboy                     # snowboy唤醒接口
│   │   └── XFawake                     # 讯飞唤醒接口
│   ├── bin                         # C类库文件夹
│   │   ├── Device.so                   # 设备管理库
│   │   ├── Opencv.so                   # Opencv识别库
│   │   ├── pyAlsa                      # 音频处理库
│   │   ├── Setnet.so                   # 配网库
│   │   ├── SocketScreen.so             # 屏幕显示库
│   │   └── SocketServer.so             # Socket通讯服务库
│   ├── config.yaml                 # 系统配置文件
│   ├── ControlCenter.py            # 控制中心库
│   ├── data                        # 相关配置数据文件夹
│   │   ├── audio                       # 音频相关
│   │   ├── conf                        # 配置相关
│   │   ├── config.db                   # 基本配置数据库，有用户数据等
│   │   ├── mqtt                        # MQTT通讯配置
│   │   ├── opencv                      # OpenCV相关配置
│   │   └── ver.txt                     # 系统版本号文件
│   ├── include                     # 核心类库
│   │   ├── mplayer                     # 音频播放类库
│   │   └── mqtt                        # MQTT通讯类库
│   ├── module                      # 系统模块文件夹
│   │   ├── awake                       # 唤醒模块
│   │   ├── ImageRecognition            # 图像识别模块
│   │   ├── SpeechSynthesis             # 语音合成模块
│   │   └── VoiceRecognition            # 语音识别模块
│   ├── MsgProcess.so               # 系统基类
│   ├── package                     # 基本功能类库文件夹
│   │   ├── Awake.py                    # 唤醒功能
│   │   ├── FaceRecognition.py          # 人脸识别功能
│   │   ├── GeneralSwitchProxy.py       # 万能开关功能
│   │   ├── Record.py                   # 录音功能
│   │   ├── Screen.py                   # 屏幕显示功能
│   │   ├── SpeechSynthesis.py          # 语音合成功能
│   │   └── VoiceRecognition.py         # 语音识别功能
│   ├── plugin                      # 插件文件夹
│   │   ├── Chat                        # 聊天机器人插件
│   │   ├── Device                      # 设备管理插件
│   │   ├── GeneralSwith                # 万能开关插件
│   │   ├── Music                       # 音乐插件
│   │   ├── Remind                      # 提醒插件
│   │   ├── SayIp                       # 报IP插件
│   │   └── User                        # 用户管理
│   ├── run.py                      # 系统运行入口文件
│   ├── runtime                     # 缓存文件夹
│   ├── webroot                     # Web服务根目录
│   │   ├── admin                       # 后台管理模块
│   │   ├── api                         # Web通讯接口
│   │   ├── desktop                     # 前端显示模块
│   │   │   ├── mojing                  # 魔镜界面
│   │   │   ├── Public                  # 全局可用界面
│   │   │   └── robot                   # 机器人界面
│   │   └── static                  # 静态资源文件夹
│   └── WebServer.py                # Web服务器类文件
├── README.md                       # 系统说明文件
└── update.py                       # 系统升级更新工具
```
### **服务与支持**
    更多服务与技术支持欢迎进QQ群：751977302