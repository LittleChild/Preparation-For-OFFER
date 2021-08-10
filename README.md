# 我的面筋
在此记录自己的秋招，同时准备秋招，复习基础知识，加油！

## 提前批
蔚来汽车
 - 做了笔试，题目忘了，都可以搜到，做的中规中矩；结果暂不匹配，也无了，无语，垃圾。

shopee
 - 笔试结束了，a了一道，其他过了部分样例，结果直接凉了，，，这公司牛啤，里面的人人人都很会写代码题，，，，


字节

·算法岗位
 - 一面凉：聊了简历，没有问基础知识，
 - 代码题：最长回文子串，，，，，

·互娱研发-智能创作：
 - 一面：
   - 简历相关：说一下monodepth2怎么做的，openvslam跟orbslam算法的区别，如何添加深度的
   - SLAM相关：PnP算法，说一下，怎么会退化，为什么6自由度最少要4个点？
   - 图像相关：
   - learning相关：
     - LSTM，详细说一下结构，为什么用的tanh激活函数不用sigmoid，其他RNN：GRU
     - 知道哪些loss函数，，，说一下交叉熵，什么时候用，怎么算的
   - 代码题：两个很大的数用数组存储每一位的数字，求相加结果，也用数组表示。（简单）
   - 呵，以为简单题就是能过呢，，，也凉了，wtf


拼多多
 - 笔试：4道编程题，网上搜不到，应该是内部题库了，，，
   - 判断线段包含：65%
   - 小猫钓鱼游戏：2%
   - 判断数字是否在一个群里面：0%
   - 最大乘数：8%
 - 凉了，，， 

爱奇艺
一面：
 - 简历：聊实习，聊项目，着重问了关键点的检测，orb特征
 - 编程题：重排链表，leetcode 143，大概写出来了

小米

终于发测评了，后续更新

商汤

杳无音信

大疆

刚做完测评

虹软科技

腾讯

CSIG交通与出行

----
### 问题搜集 & 知识补充

- 卷积神经网络的计算：
  - 卷积神将网络的计算公式为：
    - N=(W-F+2P)/S+1
    - 其中：
      - N：输出大小
      - W：输入大小
      - F：卷积核大小
      - P：填充值的大小
      - S：步长大小
  - 感受野的计算：
    - 定义：卷积神经网络每一层输出的特征图（feature map）上的像素点在原始图像上映射的区域大小。
    - 第i层在第i-1层上的感受野公式：
    - ![image](https://user-images.githubusercontent.com/35659023/127335073-39f9d606-a800-4638-9b0b-e207479072c9.png)



- BN（Batch Normalization）
  - bn一般就在conv之后并且后面再接relu
  - 参数量、运算的操作
  - 训练和测试时一般不一样，一般都是训练的时候在训练集上通过滑动平均预先计算好平均-mean，和方差-variance参数，在测试的时候，不再计算这些值，而是直接调用这些预计算好的来用，但是，当训练数据和测试数据分布有差别时，训练集上预计算好的数据并不能代表测试数据，这就导致在训练，验证，测试这三个阶段存不一致-inconsistency
  - bn的缺点：
    BN会受到batchsize大小的影响。如果batchsize太小，算出的均值和方差就会不准确，如果太大，显存又可能不够用。
  - 几种norm对比：
    - batch norm：在一个batch里所有样本的feature map的同一个channel上进行norm，归一化维度为[N，H，W]
    - layer norm：在每个样本所有的channel上进行norm，归一化的维度为[C，H，W]
    - instance norm：在每个样本每个channel上进行norm，归一化的维度为[H，W]
    - group norm：将channel方向分group，然后每个group内做归一化，算(C//G)*H*W的均值，GN的极端情况就是LN和I N

![image](https://user-images.githubusercontent.com/35659023/125475672-f728ecd2-8d44-4e19-a779-84660a7a17af.png)


GPU分布式训练

focal loss原理：Focal loss主要是为了解决one-stage目标检测中正负样本比例严重失衡的问题。该损失函数降低了大量简单负样本在训练中所占的权重，也可理解为一种困难样本挖掘。


手撕代码：快速排序 合并二叉排序树 凸包问题

最小二乘法

C++的特性：
  1. 继承
  2. 多态
  3. 封装

面向对象特征:
  1. 继承
  2. 多态
  3. 封装
  4. 抽象

多态的体现：
  1. 运行：虚函数，动态多态，其具体引用的对象在运行时才能确定
  2. 编译：模板，编译时多态是静态多态，在编译时就可以确定对象使用的形式
  3. 重载
  4. 类型转换

虚函数对应方法：虚函数（虚方法）只针对类的成员函数，普通函数不可声明为虚函数！且一般只有在用到继承时才将基类的成员函数声明为虚函数！

进程和线程

进程间通信的7种方式:
  1. 管道/匿名管道(pipe)
  2. 有名管道(FIFO)
  3. 信号(Signal)
  4. 消息(Message)队列
  5. 共享内存(share memory)
  6. 信号量(semaphore)
  7. 套接字(socket)

数据库事务管理条件，一般来说，事务必须满足4个条件（ACID）：
  1. 原子性
  2. 一致性
  3. 隔离性
  4. 持久性

LiDAR的原属数据:脉冲发射角度、脉冲发射与返回时间、脉冲返回强度、回波次数等，由IPAS解算出定位定向数据，生成每一束激光探测的物体三维坐标，构成点云。

全高清视频的分辨率为1920×1080P，如果一张真彩色像素的1920×1080 BMP数字格式图像，所需存储空间是多少？
  - 黑白图像，一个像素只要1bit，256灰度图像，要8bit，而真彩图像是基于三原色，需要3个灰度值，所以需要24bit。不压缩的情况下，一个像素需要占用24Bit（位）存储，因为一个Byte（字节）为8Bit，故每像素占用3Byte。那么，1920×1080个像素就会占用1920×1080×(24÷8)Byte=6220800Byte=6075KB≈5.93MB。
  - 像素的存储空间取决于像素的深度，一个像素占用多少空间取决于什么模式。例如，在灰度模式下，一个像素相当于一个字节，在RGB模式下，一个像素相当于三个字节，在CMYK模式下，一个像素相当于四个字节。
 
### 机会关注：

![image](https://user-images.githubusercontent.com/35659023/125221928-9cc8b500-e2fb-11eb-9b87-c749bd274620.png)

