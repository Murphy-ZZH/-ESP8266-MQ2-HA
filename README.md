放假回来总想做点什么，想着厨房差个可燃气监测，自己又带回来一个8266，寻思着就做这个吧

**1：材料准备**

esp8266mcu模块1个、MQ2烟雾传感器一个、火焰传感器一个、0.96寸oled屏幕一个、蜂鸣器一个、杜邦线若干

**2：实现原理**

MQ2模块输出模拟信号到8266进行adc转换，可进行实时监测环境内可燃气浓度，当火焰传感器接收到火焰信号后输出高电平，8266在屏幕上实时显示出环境天然气浓度和互联网时间（毕竟食材的美味需要精准的时间控制），并通过WiFi+MQTT上报至Home Assistant，若配网失败或MQTT服务器连接失败均直接在屏幕输出错误信息，若监测到环境出现异常（出现火苗或浓度过高）则自动将上报浓度拉满并触发蜂鸣器报警，HA检测到浓度过高自动将信息发送到手机

**3：演示视频**

链接: https://pan.baidu.com/s/1Y6Bamf3LqyPuo4AEbPbDSg?pwd=4n8r 提取码: 4n8r

![image](https://github.com/Murphy-ZZH/KitchenWarning-ESP8266-MQ2-HA/blob/main/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20240724012633.jpg)
![image](https://github.com/Murphy-ZZH/KitchenWarning-ESP8266-MQ2-HA/blob/main/image.png)
