---
title: 高斯滤波
date: 2022-08-14
categories:
    - DevLog
tags:
    - DevLog
    - Gauss
---
高斯滤波实现

<!-- more -->

## 本文提示
** 本文仍然在编辑/排版中 **
本文提供了相关代码和算法仅为示例学习，并非标准案例，并且OpenCV提供了高斯滤波函数，如果遇到不明白的概念和地方可以参考引用文章理解，也可以尝试在搜索引擎上搜索相关概念和图片示例，由于本站资源原因，暂不提供图片。

tips: 本文为了方便仅是灰度图片处理
如果需要彩色图片应该尝试修改代码建立三维滤波核或者三种通道进行分别处理，本文滤波核是一维滤波核。
## 环境与依赖
Python        本次使用的编程语言
OpenCV      跨平台计算机视觉库
Windows11  本文中代码运行系统
## 前提指明(仅仅举例非实际情况)
图形数据
10 20 30
40 50 10
20 30 40
滤波核 (提示:权请保证和为1 此处已经归一化 但并非真实情况)
0.1 0.1 0.2
0.1 0.1 0.1
0.1 0.1 0.1
## 用途指明
高斯滤波是一种线性平滑滤波，适用于消除高斯噪声，广泛应用于图像处理的减噪过程。
tips:高斯平滑滤波器对于抑制服从**正态分布**的噪声非常有效。
## 概念辨析
### 高斯滤波
(通俗介绍 并非专业介绍) 
高斯滤波其实就是对图片每处像素值进行加权平均处理时，每一个像素点的值，都由其本身和邻域内的其他像素值经过加权平均后得到。
(此处需要具备高中数学知识)
## 滤波核
当我们进行滤波时，使用到的权用一个矩阵表示，该矩阵是一个权矩阵，同时我们叫这个权 矩阵为滤波核。(示例见前提指明)
## 生成滤波核
![CodeCogsEqn.gif](https://s2.loli.net/2022/08/14/4dgAQ2RCInSM8m6.gif)

```
def GaussKernel(size,k,sigma):
    _t = np.zeros((size,size),np.float32)
    for i in range (size):
        for j in range (size):
            norm = math.pow(i-k,2) + pow(j-k,2)
            _t[i,j] = math.exp(-norm/(2*math.pow(sigma,2)))/2*math.pi*pow(sigma,2)
    sum = np.sum(_t)
    kernel = _t/sum
    return kernel
```

### que:滤波核为什么是奇数?
其中一个原因是定位中心锚点
## 直接OpenCV操作
```
import cv2
Gn=cv2.imread("Gaussian_noise.jpg") 
Gf=cv2.GaussianBlur(Gn,(3,3),0,0)
cv2.imshow("未处理噪声图像",Gn)
cv2.imshow("高斯滤波后图像",Gf)
cv2.waitKey()
cv2.destroyAllWindows()
```
## 文章引用
高斯滤波(推荐)
https://blog.csdn.net/weixin_51571728/article/details/121527964
高斯滤波核(有图片更易理解)
https://blog.csdn.net/qqq777_/article/details/112800310
有关线性滤波、滤波核的基本概念(概念理解)
https://blog.csdn.net/weixin_42664622/article/details/103672899
数字图像处理基础 — 高斯滤波
https://zhuanlan.zhihu.com/p/82569305
图像滤波原理(不推荐)
https://view.inews.qq.com/a/20220425A06HHF00
