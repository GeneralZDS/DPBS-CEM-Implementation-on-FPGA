# A Deep Pipelined Implementation of Hyperspectral Target Detection Algorithm on FPGA Using HLS

[![License](https://img.shields.io/badge/license-BSD-blue.svg)](LICENSE)

By [Dongsheng Zhao](https://generalzds.github.io/), Leijie

### Introduction

<p align="center">
<img src="https://github.com/GeneralZDS/DPBS-CEM-Implementation-on-FPGA/blob/master/img-folder/remotesensing-10-00516-ag.jpg" alt="Graphical Abstract" width="600px">
</p>

This project presents a deep pipelined background statistics (DPBS) approach to optimizing and implementing a well-known subpixel target detection algorithm, called constrained energy minimization (CEM) on FPGA by using high-level synthesis (HLS). For more details, please refer to our [rs paper](http://www.mdpi.com/2072-4292/10/4/516).

### Features

* A novel deep pipelined architecture is proposed to accelerate the proposed DPBS-CEM algorithm on FPGA using HLS. It outperforms the previous work designed with RTL in terms of data throughput performance.
* A solution is derived to remove the data dependency existing in SBS-CEM for updating the inverse matrices, by allowing four adjacent pixels to update their own individual inverse matrices that are stored in four different memories.
* The proposed structure can be simply rebuilt to support diverse HSI implementations with different spatial resolution and number of spectral bands through several parameters modified under HLS. Most importantly, the framework can support various operation modes including split/non-split data and local/global detection. It is easily adapted to match multiple rates of hyperspectral imagery.
* Last but not least, alternative solutions to the problems of feedback and high fanout are also provided.
