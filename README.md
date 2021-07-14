# 我的面筋
在此记录自己的秋招，同时准备秋招，复习基础知识，加油！

----
### 问题搜集 & 知识补充

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

focal loss原理

手撕代码：快速排序 合并二叉排序树 凸包问题

最小二乘法

C++的特性

多态的体现

虚函数对应方法

进程和线程



### 机会关注：

![image](https://user-images.githubusercontent.com/35659023/125221928-9cc8b500-e2fb-11eb-9b87-c749bd274620.png)

