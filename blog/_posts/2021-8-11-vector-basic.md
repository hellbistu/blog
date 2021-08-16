---
title: 向量基础
date: 2021-8-11
tags: 
  - 线性代数
  - 计算机图形学
author: yangzhenyu
location: beijing  
---

## 向量的定义

一个同时具有大小和方向的量就是向量。可以形象的表示为带箭头的线段。

可以记为 $\vec{a}$​​​​ 或者 ***a***

代数表示：

在指定坐标系S中，基向量为：$\vec{e_1},\vec{e_2},...,\vec{e_n}$ 。

 $\vec{a}= a_1\vec{e_1} + a_2\vec{e_2} + ... + a_n\vec{e_n}$

其中$a_1,a_2,...,a_n$分别为在$\vec{e_1},\vec{e_2},...,\vec{e_n}$​​​下的投影。当基向量已知，可以省略基向量，表示为：

$\vec{a} = (a_1,a_2,...,a_n)$

在常见的三维空间直角坐标系$O_{xyz}$​里，x轴、y轴、z轴的单位向量分别为$\vec{i}、\vec{j}、\vec{k}$任意向量可表示为：

$\vec{a} = (x,y,z) = x\vec{i} + y\vec{j} + z\vec{k}$

在矩阵运算中，向量通常被写成类似矩阵的列向量或行向量。在线性代数中所指的向量默认为列向量。如一个向量 ***a*** = (x,y,z)。 可写成：

$\textbf{a} = \begin{bmatrix} x \\ y \\ z \end{bmatrix}$​​

$\textbf{a}^T= \begin{bmatrix}x&y&z\end{bmatrix}$​​​​​​​​​​



## 向量的运算

### 加法：

$\vec{a} = x_a\vec{i} + y_a\vec{j} + z_a\vec{k} = (x_a,y_a,z_a)$​​​​ 

$\vec{b} = x_b\vec{i} + y_b\vec{j} + z_b\vec{k} = (x_b,y_b,z_b)$​​ 

则：

$\vec{a} + \vec{b} = (x_a + x_b)\vec{i} + (y_a + y_b)\vec{j} + (z_a + z_b)\vec{k} = (x_a + x_b,y_a+y_b,z_a+z_b)$​​

加法满足：

***交换律***： $\vec{a} + \vec{b} = \vec{b} + \vec{a}$​

### 数量积（点积、内积、标量积）：
数量积的结果是一个标量。
$\vec{a}\cdot\vec{b} = |\vec{a}||\vec{b}|\cos{\theta}$ （其中在$\theta$为两个向量的夹角）

若三维向量  $\vec{a} = (x_a,y_a,z_a),\vec{b} = (x_b,y_b,z_b)$​,则
$\vec{a}\cdot\vec{b} = x_ax_b + y_ay_b + z_az_b$​​​

数量积满足 ***交换律***、***分配律***、***与标量的结合律***：
$\vec{a}\cdot\vec{b} = \vec{b}\cdot\vec{a}$​​​

$\vec{a}\cdot(\vec{b} + \vec{c})= \vec{a}\cdot\vec{b} + \vec{a}\cdot\vec{c}$​​​​​

$(k\vec{a})\cdot\vec{b} = k(\vec{a}\cdot\vec{b}) = \vec{a}\cdot(k\vec{b})$​​

### 叉乘（外积、向量积）：
叉乘的结果是一个向量。

$\vec{a}\times\vec{b} = |\vec{a}||\vec{b}|\sin{\theta}\vec{n}$​，其中n为一个与$\vec{a},\vec{b}$​向量构成平面垂直的单位向量，方向由右手法则确定。可以看到，这个新向量的大小是这两个向量构成平行四边形的面积

若三维向量  $\vec{a} = (x_a,y_a,z_a),\vec{b} = (x_b,y_b,z_b)$,则可以这样表示：
$\vec{a}\times\vec{b} = (x_a\vec{i} + y_a\vec{j} + z_a\vec{k})\times(x_b\vec{i} + y_b\vec{j} + z_b\vec{k}) = \begin{vmatrix}\vec{i}&\vec{j}&\vec{k}\\x_a&y_a&z_a\\x_b&y_b&z_b\end{vmatrix} = (y_az_b - z_ay_b)\vec{i} + (z_ax_b - x_az_b)\vec{j} + (x_ay_b - y_ax_b)\vec{k} = (y_az_b - z_ay_b,z_ax_b - x_az_b,x_ay_b - y_ax_b)$​​​​​​​​​​​

叉乘满足 分配律、与标量的结合律、反交换律：
$\vec{a}\times(\vec{b} + \vec{c}) = \vec{a}\times\vec{b} + \vec{a}\times\vec{c}$
$(k\vec{a})\times\vec{b} = k(\vec{a}\times\vec{b}) = \vec{a}\times(k\vec{b})$
$\vec{a}\times\vec{b} = -\vec{b}\times\vec{a}$
