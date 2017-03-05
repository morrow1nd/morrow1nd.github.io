# 基本光照

![4 compare](4.png)
<p align="center">Phong逐顶点 - Phong逐顶点 - HalfLambert - BlinnPhong</p>


## Phone光照模型

 + 环境光(ambient)
 + 自发光(emissive)
 + 漫反射(diffuse)
 + 高光反射(specular)

#### 计算公式

**c**<sub>ambient</sub> = **g**<sub>ambient</sub>

**c**<sub>emissive</sub> = **m**<sub>emissive</sub>

**c**<sub>diffuse</sub> = (**c**<sub>light</sub> \* **m**<sub>diffuse</sub>)max(0, **n** \* **l**)

**c**<sub>specular</sub> = (**c**<sub>light</sub> \* **m**<sub>specular</sub>)max(0, **v** \* **r**)<sup>**m**<sub>gloss</sub></sup>

**r** = 2(**n** \* **l**)**n** - **l**

其中**r**是反射方向。 在Unity中可以使用内置函数reflect计算。


## 半兰伯特(Half Lambert)模型

使用Lambert光照模型的一个缺点是背光面十分黑，一种视觉增强技术是Half Lambert模型，它没有任何物理上的依据。

**c**<sub>diffuse</sub> = (**c**<sub>light</sub> \* **m**<sub>diffuse</sub>)(a(**n** \* **l**) + b)

## Blinn-Phong光照模型

**h** = (**v** + **l**) / | **v** + **l** | = normalize(**v** + **l**)
