## Phone光照模型

**c**<sub>ambient</sub> = **g**<sub>ambient</sub>

**c**<sub>emissive</sub> = **m**<sub>emissive</sub>

**c**<sub>diffuse</sub> = (**c**<sub>light</sub> \* **m**<sub>diffuse</sub>)max(0, **n** \* **l**)

**c**<sub>specular</sub> = (c<sub>light</sub> \* m<sub>specular</sub>)max(0, v \* r)<sup>m<sub>gloss</sub></sup>

**r** = 2(n \* l)n - l

其中**r**是反射方向。 在Unity中可以使用内置函数reflect计算。


## 半兰伯特(Half Lambert)模型

**c**<sub>diffuse</sub> = (**c**<sub>light</sub> \* **m**<sub>diffuse</sub>)(a(**n** \* **l**) + b)

## Blinn-Phong光照模型

**h** = (**v** + **l**) / | **v** + **l** | = normalize(**v** + **l**)

