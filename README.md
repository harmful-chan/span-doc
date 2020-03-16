# Span
## 项目介绍
    物联网智能家居交互增强项目。使命是为了改变用户在使用智能家电的交互方式，使用语音智能交互，OpenCV，Unity3D等技术提高用户体验。

## 智能人机交互发展现状
    人机交互（Human ComputerInteraction 或Human Machine Interaction，简称HCI 或HMI），是一门..(更多)[./detail.md]

## 智能人机交互核心述求
    语音交互：技术成熟度不断提升，“听的准确”和“说的明白”正逐步...
    [更多](./detail.md)

## 物联网前景分析
    https://blog.mushuwei.cn/2018/10/26/IOT%E5%B8%82%E5%9C%BA%E5%8F%8A%E6%8A%80%E6%9C%AF%E6%A8%A1%E6%8B%9F/
    IoT Analytics：https://www.infoq.cn/article/ICTPvIDxzJBgaaDsNFQO

## 物联网项目资源列表
    A curated list of awesome Internet of Things projects and resources. --Awesoe IoT (资源列表)[https://github.com/HQarroum/awesome-iot]

## 项目实现
★ 第一步：传感器端走USART，IIC，SPI，USB3.0把数据送到网关端，网关端连接wifi走mqtt协议把传感器数据送到业务后台。<br>

★ 第二步：移动端安卓手机app连接wifi走RESTful API，msqtt连接后台，成功与持有设备关联。<br>

★ 第三步：用户通过UI界面操作可以按照用户所想操作持有设备。<br>

★ ★ 第四步：用户通过语音操作天猫精灵，天猫精灵接入AliGenie开发者平台，AliGenie通过后台授权认证，走RESTful API把用户操作推送给业务后台，业务后台走mqtt把操作指令推送给网关端，网关端把操作分发到不同设备当中。

★ ★ ★ 第五步：用户通过手机APP VR界面可以看到3D虚拟人物在替用户完成操作。
## 硬件选型
🔗 被动传感器：温湿（DH11）、心率血氧（MAX30100）、陀螺仪（GY521）等。<br>
🔗 网关：ModeMCU v3 开发板<br>
🔗 网关接入：ESP8266<br>
🌐 服务器：家用电脑跑虚拟机（Ubuntu16.04 x64 4核心8G没存60G硬盘 100M光纤）<br>
📱 移动设备：三星安卓手机4+64G<br>
📱 语音交互：天猫精灵<br>
📱 VR: 用手机代替吧<br>

## 项目模块
🔗 传感器：不想再碰烙铁，直接买现成的。:weary:

🔗 网关接入：NodeMCU v3 开发板 + NodeMCU固件（Lua + C/C++）
+ NodeMCU固件 官方文档：https://nodemcu.readthedocs.io/en/master/
+ 开发文档：开发板是二次开发的要收集下。

🌐 官方介绍：Nginx + Bootstrap4 + JQuery + 官方模板  
+ Bootstrap4 官方文档：https://getbootstrap.com/
+ Bootstrap4 模板：http://demo.cssmoban.com/cssthemes5/cpts_1029_bnw/index.html


🌐 数据接入后台：ThingsBoard 二次开发 
+ ThingsBoard 官方文档：https://thingsboard.io/docs/reference/architecture/
+ ThingsBoard 二次开发文档：https://www.cnblogs.com/harmful-chan/p/12193225.html（持续更新中...）
+ 管理页面：AngularJS + Angular Material 2（有时间用Angular9写个）
+ 并发模型： Actor模型akka
+ 集群协作：zookeeper
+ 支持协议：mqtt、coap、http
+ 持久化: Postgresql、Cassandra，datastax（数据访问）

📱 图像处理+三位建模：OpenCV + Unity3D（没用C#写过Unity，看缘分把）
+ OpenCV 官方文档；https://opencv.org/releases/

📱 移动端APP：Angular9 + ionic
+ Angular 官网：https://angular.cn/docs
+ Ionic 官网：https://ionicframework.com/docs

📱 天猫精灵接入：AliGenie开发者平台
+ AliGenie 官网：https://www.aligenie.com/

其他：CI/CD（Jenkins）、GitHub（项目管理）、Docker CE（虚拟化）、 k8s（运维）