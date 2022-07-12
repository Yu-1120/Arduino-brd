# arduino_brd
arduino的最小板
**描述：**

1.接口改为Type-C。

2.增加二极管，防止反接。

3.AMS1117-5,0用来稳压整个电路。（压降有点大）

4.串口采用CH340N（自带晶振，相当于缩小版的CH340C）

5.电源，RX，TX，D13灯全部满足。

6.去除了ICSP方便烧录，采用引脚进行ICSP烧录。

7.增加了3.3v LOD稳压芯片，外围一共有3个3.3v/5v接口，方便接入更多的传感器。

8.所有引脚全部引出，方便后续使用。

**不足：**

AMS11175.0压降比较大，5v输出不到5v，可以采用稳压二极管（需要自行更改吧）

填坑专区

1.复位电路中一定要增加个100nF接在RESET上，不然不可能上传成功的！！！！

![1](https://user-images.githubusercontent.com/78225990/177272581-1f96a731-4d66-470e-a8b2-daef40abd320.png)


2.实际在测试当中有的方案采用CH340C，DTR和RTS没啥区别，而且CH340C接口多，产生了浪费还占地方

所以本工程采用CH340N一样的可以愉快的烧录，占地小，何乐而不为呢？

新手建议：

如果使用CH430C方案，供电的5V的话，需要吧V3引脚接地哦！

3.3V供电的方案那就吧V3接在VCC（3.3V）上。

![2](https://user-images.githubusercontent.com/78225990/177272751-770289e3-9328-40f6-9436-3b691d63748d.png)


3.要想完美的使用Type-C,必须让电脑识别C To C协议，所以两个5.1K的电阻必不可少哦！！

![3](https://user-images.githubusercontent.com/78225990/177272786-e0d549ad-da02-431e-a925-4133de1b40bb.png)


**成品图：**

**正面**
![4](https://user-images.githubusercontent.com/78225990/177273006-5b54a01c-f48c-4144-bef4-6bd9e1d6bddc.jpeg)


**反面**
![5](https://user-images.githubusercontent.com/78225990/177272938-f31c93b7-9430-4f0a-bba3-e4179a8553fc.jpeg)
国产版和CCNANO对比图

丝印放在外面，大了一圈
![6](https://user-images.githubusercontent.com/78225990/177273174-ebe89fd4-7f93-4d47-a8a1-2ee2fc60f04f.jpeg)

