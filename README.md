| 第三届计图挑战赛

# Jittor 计图挑战热身赛 CGAN

![主要结果](https://s3.bmp.ovh/imgs/2023/07/22/2445e1b9a57cc4c9.png)


## 简介
| 简单介绍项目背景、项目特点

本项目包含了第三届计图挑战赛计图挑战热身赛比赛的代码实现。本项目的特点是：采用了CGAN方法对MNIST输入数据进行学习处理，
得到了完成训练生成器和判别器，并用生成器生成了随机id以验证效果。

## 安装 

本项目可在 1 张 3090 上运行，训练时间约为 0.8 小时。

#### 运行环境
- ubuntu 20.04.6 LTS
- python >= 3.8
- jittor >= 1.14.0

#### 安装依赖
执行以下命令安装 python 依赖
```
pip install -r requirements.txt
```

#### 预训练模型
该模型较为简单，无需预训练模型

## 数据预处理
该数据集较为简单，无需预处理

## 训练
｜ 介绍模型训练的方法
该模型较为简单，单卡即可
训练执行如下命令：
python CGAN.py

## 推理
推理：使用GAN模型，改平方误差评价，在数据提供时同时提供标签进行训练，以使得生成器能生成对应标签的内容
测试：每完成一个epoch后用生成器生成一组带标签图像以测试生成结果，从loss函数和生成器结果综合判断判别器结果
评估：对预期需要生成的一串随机数字，由训练完的生成器进行生成，检测其生成效果

测试集上的结果会自动生成并保存

## 致谢
| 对参考的论文、开源库予以致谢，可选

此项目基于论文 *A Style-Based Generator Architecture for Generative Adversarial Networks* 实现，部分代码参考了 [jittor-gan](https://github.com/Jittor/gan-jittor)。

## 注意事项

点击项目的“设置”，在Description一栏中添加项目描述，需要包含“jittor”字样。同时在Topics中需要添加jittor。

![image-2023072221555344618636](https://s3.bmp.ovh/imgs/2023/07/22/2445e1b9a57cc4c9.png)