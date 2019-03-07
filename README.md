
# Outline
**1.Training cycleGAN**

**2.Inference cycleGAN in personal image**

**3.Other Two methods**

**4.Compare & Conclusion**

## 1.Training cycleGAN
![](https://i.imgur.com/HviTFwq.png)

**saved model:**
![](https://i.imgur.com/CSPXjjc.png)

## **2.Inference cycleGAN in personal image**
### **2.1 personal image**
**Orange**

<img src="https://i.imgur.com/yrmL0HZ.png" width="255"><img src="https://i.imgur.com/9rlTn3H.png" width="255">



**Apple**

<img src="https://i.imgur.com/VOJ9ItO.png" width="255"><img src="https://i.imgur.com/slMq9vY.png" width="255">



### **2.2 Inference Result**
------
**Apple to Orange**

![](https://i.imgur.com/u8uNsNt.png) 
![](https://i.imgur.com/DseMyNm.png)
------
**Orange to Apple**
-----
![](https://i.imgur.com/40GBIhT.png)
![](https://i.imgur.com/FhNp7Ls.png)



## **3. Other Two methods**
#### **1. Super fast color transfer**
#### **2. DeepArt style transfer**

### **3.1 Super fast color transfer between images**
**Apple to Orange**

<img src="https://i.imgur.com/Pvgks4U.jpg " width="255"> <img src="https://i.imgur.com/CTzRhin.jpg " width="255">

<img src="https://i.imgur.com/qnJmFBt.jpg " width="255"> <img src="https://i.imgur.com/Vkn8Gqo.jpg " width="255">

-----
**Orange to Apple**

<img src="https://i.imgur.com/2B3fTCz.jpg " width="255"> <img src="https://i.imgur.com/iHJaU6U.jpg " width="255">

<img src="https://i.imgur.com/5H2TERx.jpg" width="255"> <img src="https://i.imgur.com/GoxrfvA.jpg " width="255">



### **3.2 [DeepArt](https://deepart.io/#)**
[paperlink](https://https://arxiv.org/abs/1508.06576)

**Architecture**

- This paper use vgg net as his network,and set two different kinds of loss function.One of them is style loss，and another one is content loss。

- set content loss to maintain same object between output image and source image.Such as building,tree whatever.

- set style loss to maintain same picture style between output image and style image.

- so the totle loss function is the addiction of above two loss funcions.

<img src="https://i.imgur.com/DuXomab.png" width="455">

**Loss Function:**

<img src="https://i.imgur.com/hf3G0MQ.png" width="400">

**Result:**
------
**Apple to orange**

<img src="https://i.imgur.com/B4z1O3y.jpg" width="255"> <img src="https://i.imgur.com/6WsqlBr.jpg" width="255">

<img src="https://i.imgur.com/qaGd3Lu.jpg" width="255"> <img src="https://i.imgur.com/RZTp1d1.jpg" width="255">
-----
**Orange To Apple**

<img src="https://i.imgur.com/vqCuyuG.jpg" width="255"> <img src="https://i.imgur.com/HlTjJhj.jpg" width="255">

<img src="https://i.imgur.com/r6f0u48.jpg" width="255"> <img src="https://i.imgur.com/nbQoezF.jpg" width="255">

## **4.Compare & Conclusion**
1.Performance ranking:

cycleGan > DeepArt  >>  Super fast color transfer

2.Training time cost:

cycleGan >> DeepArt  >  Super fast color transfer

3.Training set sample size:

cycleGan >> DeepArt > Super fast color transfer

**Conclusion:**

cycleGan can make high quality style transfer image, But at the same time It need more training data and It spent more time.

DeepArt can do style transfer image with only a pair of images(content & style), But the result seems not so good.Thus the performance was limited

Super fast color transfer seems can't do style transfer, because It just try to tune the Hue of whole content image base on the style image

<br/><br/>

