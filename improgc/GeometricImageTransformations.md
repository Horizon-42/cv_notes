# 2d图像的几何变换
为了减少采用造成的误差，像素映射是后向计算的，也就是从dst->src

正确地映射像素需要解决两个问题:
## 不存在像素的外推 Extrapolation 
当目标图像需要的像素在源图像中不存在时，则需要外推像素。这里用到和filter中一样的方法去外推像素，即各种边缘padding形式。另外还额外添加了一个BORDER_TRANSPARENT，可以跳过不处理那些需要外推的位置。
## 像素插值
可以用最邻近像素，也可以用多项式拟合来插值.