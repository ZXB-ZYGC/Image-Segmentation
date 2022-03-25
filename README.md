

使用经典网络U-NET进行图像语义分割简单总结： 
=================================

![image](https://user-images.githubusercontent.com/36906937/160072420-5e8cb871-884e-4264-a494-0afdb4063e1b.png)

**网络架构分析**：  
依据对u-net网络forward部分进行的结构总结如上图所示，左半部分为编码器(encoder)，有半部分为解码器(decoder), 下面为bottleneck部分。其中具体细节部分参见unet.py  
**A little Tip**：当我们分析一个网络架构的时候，最直接的方法就是去看网络的forward部分。

__u-net输入数据__：   
如下图所示，黄色框的代表的像素大小为388\*388蓝色框代表为577*577，蓝色框是通过黄色框的镜像得到的。u-net输入通道为1通道，输出为2通道(2分类)。值得注意的是编码器的输入和解码器的输出尺寸是不同的，输入为577\*577，输出为388\*388.(具体细节看原论文https://arxiv.org/pdf/1505.04597.pdf)

![image](https://user-images.githubusercontent.com/36906937/160073839-d16bc0b1-ca4d-4d89-b7d2-0f7cdd867b17.png)













关于u-net family项目链接1： https://github.com/ShawnBIT/UNet-family
