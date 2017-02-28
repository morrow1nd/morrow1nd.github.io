## 单张纹理

最简单的纹理，直接将一张纹理覆盖在模型表面

见SingleTexture.shader


## 凹凸纹理

原理：使用一张纹理来修改模型表面的法线。从而改变模型表面的细节，但不会改变模型顶点的位置。

本例子使用的是切线空间的法线纹理(tangent-space normal map)，即纹理中存放的切线空间的法线坐标。

见BumpMapping.shader


## 渐变纹理
[TODO]


## 遮罩纹理
[TODO]