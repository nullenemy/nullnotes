---
title: 如何开始学习图形编程?
date: 2019-05-29 10:40:02
tags:
---

你可能会反驳我：图形编程可能是各个编程领域里相对来说比较复杂的一个部分。你可以想象，对我这样一个几乎不存在数学基础的文科生来说，3D图形对于线性代数及微积分理论知识的依赖，是多少次地让我对自己的智力产生过怀疑。

过去两年我试着去阅读了一些图形学相关教材，并跟着许多介绍OpenGL的教程中的示例代码去实现了一些小的Demo。但是我觉得整个学习过程走了很多弯路，觉得有必要分享一下：如果你像我一样，在学习图形编程的路上挣扎，希望能够给你一点帮助。

### 第一步：实现一个简单的光线追踪和光栅渲染器

我一开始学习图形编程，就试图通过OpenGL。如果你想通过OpenGL来学习，我推荐一套[完整的OpenGL教程](https://learnopengl.com/)。虽然作者非常详细地介绍了图形渲染管线，以及相对完整地介绍了涉及到的数学物理知识，但是现在想来，它并不是一个很好的初学材料：因为对于初学者来说，面对OpenGL本身的复杂性，很容易迷失了整个森林。

单是设置OpenGL开发环境,就让人产生挫败感：什么是glfw? 什么是glew/glad/glut? 它们和OpenGL什么关系？好容易设置好了，单是画出来一个三角形，都要这么多行的代码？使用这么多的OpenGL函数？

或者你也可以通过使用游戏引擎比如 Unity 或者 Unreal 来进行学习，但是对于初学者来说，这不过是引入了一个比OpenGL更大的黑盒，所有的工作都被引擎完成了，初学者可能会因此学到了大量引擎相关的的实现方法，而对背后的原理一窍不通。

最近这两天我在试图实现一个简单的光线追踪 (raytracer) Demo.在看的材料有 Peter Shirley 的 Ray Tracing in One Weekend， 还有 Kevin Suffern 的 Ray Tracing from the Ground Up。但是最棒的材料我觉得是在github上的 [tinyrenderer系列](https://github.com/ssloy/tinyrenderer/wiki)。它教你用非常简单的代码让你理解了图形渲染管线的每一个环节。看完之后你虽然仍然不能用OpenGL画出三角形，但是却明白了OpenGL的工作原理。


### 第二步：数学

图形编程绕不开数学。3D图形这一块主要涉及的数学是线性代数。找一本你喜欢的线性代数教材，做一下后面的习题，重点掌握以下矩阵变换的应用就可以了。

可以看一下专门针对3D图形的数学书，比如Eric Lengyel 的 Mathematics for 3D Game Programming and Computer Graphics。

我推荐可以看一下MIT的OpenCourseWare上的线性代数课程，你如果不能翻墙，我相信在bilibili上一定已经有人上传了。

拿下了基本的线性代数，后面在学习 Physically Based Rendering 的时候，微积分又会变得至关重要。同样，微积分的课程在 OpenCourseWare 上也有。但是我觉得更好的微积分课程是 [mooculus](https://mooculus.osu.edu/)，是Ohio州立大学的老师设立的，我曾在coursera跟完了这门课，算是我在coursera上完成的第一门课程。

另外不得不提的是 [ 3Blue1Brown的youtube频道 ](https://www.youtube.com/channel/UCYO_jab_esuFRV4b17AJtAw), 作为学习的补充，视频制作精良，尤其推荐关于微积分和线性代数的 Essence 系列。他在哔哩哔哩上有官方频道。

在这些基础的东西弄懂了之后，再回过头去接触具体的图形api，不管是OpenGL, Vulkan, 还是Direct3D, 都会让你在学习的过程中更加地事半功倍。推荐一个大神miloyip推荐图形学相关的书单:  [ 游戏程序员学习之路 ](https://github.com/miloyip/game-programmer)。只能说一句：任重道远。