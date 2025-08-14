---
layout: default
title: 一 集群硬件综述
nav_order: 2
---

# 一 集群硬件综述


## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1.1 概述

本套集群系统共有八台高性能主机组成，其中一台为登录节点（管理节点，无加速计算卡），其余七台为计算节点。计算节点的主要计算设备为GeForce GTX TITAN X，GeForce RTX 3090，Tesla P100，其中GeForce GTX TITAN X和GeForce RTX 3090单精度浮点运算能力强，适合进行适合于做大规模的可视化渲染，机器学习模型训练等计算，Tesla P100双精度浮点运算能力强，适合用于科学计算等双精度浮点运算应用。用户可以根据需求选择不同的设备运行作业，达到最好的加速效果。

## 1.2 硬件配置

| 节点名称  | CPU                                       | GPU                | 内存 |
| --------- | ----------------------------------------- | ------------------ | ---- |
| manager   | Intel(R) Xeon(R) Gold 5218R CPU @ 2.10GHz | None               | 128G |
| compute01 | Intel(R) Xeon(R) Gold 5218R CPU @ 2.10GHz | 2GeForce RTX 3090  | 128G |
| compute02 | Intel(R) Xeon(R) CPU E5-2620 v2 @ 2.10GHz | 4GeForce GTX TITAN | 32G  |
| compute03 | Intel(R) Xeon(R) CPU E5-2620 v2 @ 2.10GHz | 4GeForce GTX TITAN | 128G |
| compute04 | Intel(R) Xeon(R) CPU E5-2620 v2 @ 2.10GHz | 2GeForce RTX 3090  | 144G |
| compute05 | Intel(R) Xeon(R) CPU E5-2620 v2 @ 2.10GHz | 2GeForce RTX 3090  | 144G |
| compute06 | Intel(R) Xeon(R) CPU E5-2620 v2 @ 2.10GHz | 2Tesla P100        | 144G |
| compute07 | Intel(R) Xeon(R) CPU E5-2620 v2 @ 2.10GHz | 2Tesla P100        | 144G |

## 1.3 网络配置

集群使用千兆以太网作为集群管理网络，使用56GB/s Infiniband高速网作为集群计算网络。

| 节点名称  | 以太网   | Infiniband |
| --------- | -------- | ---------- |
| manager   | 10.1.1.1 | 11.1.1.11  |
| compute01 | 10.1.1.2 | 11.1.1.2   |
| compute02 | 10.1.1.3 | 11.1.1.3   |
| compute03 | 10.1.1.4 | 11.1.1.4   |
| compute04 | 10.1.1.5 | 11.1.1.5   |
| compute05 | 10.1.1.6 | 11.1.1.6   |
| compute06 | 10.1.1.7 | 11.1.1.7   |
| compute07 | 10.1.1.8 | 11.1.1.8   |


