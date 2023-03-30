### Ct-LVI: A Framework Towards Continuous-time Laser-Visual-Inertial Odometry and Mapping

Zhong Wang<sup>1</sup>, Lin Zhang<sup>1</sup>, Shengjie Zhao<sup>1</sup>, and Yicong Zhou<sup>2</sup>

<sup>1</sup>School of Software Engineering, Tongji University, Shanghai, China

<sup>2</sup>Department of Computer and Information Science, University of Macau, China

#### Introduction

>  This is the website for our paper "Ct-LVI: A Framework Towards Continuous-time Laser-Visual-Inertial Odometry and Mapping".

![Framework](framework.png)

<center style="color:#C0C0C0;text-decoration:underline">Figure 1. (a) Self-developed handheld device. (b) The framework of Ct-LVI: “Preprocessing” produces synchronized and de-skewed point clouds, roughly fitted trajectory, and tracked visual features; “Front-end” conducts continuous-time laser-visual-inertial odometry; and “Backend” eliminates drifts via laser-visual fused loop detection and constraint construction, as well as global pose graph adjustment.</center>

#### Source Codes

[Ct-LVI Codes](code.zip)

#### Demo Video

> The following demo video shows the functionality and demonstrates the performance of our Ct-LVI.

<video id="v1" controls="" src="Video.mp4" preload="true">
