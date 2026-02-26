---
title: 'Alinx ACU7EV核心板电源方案分析'
author: 杨致远
date: '2025-02-17T19:42:45+08:00'
draft: false
---
红框为0.85V 25A核心电源模块，muRata MYMGM1R824ELA5RP
![pic/20260226194310_00e7c599026c5d4a0be9313f4c302137.png](https://barbarian-1306448949.cos.ap-nanjing.myqcloud.com/pic/20260226194310_00e7c599026c5d4a0be9313f4c302137.png)
![pic/20260226194511_cf4d5680d2ac14ada8186ddecfc8aad0.png](https://barbarian-1306448949.cos.ap-nanjing.myqcloud.com/pic/20260226194511_cf4d5680d2ac14ada8186ddecfc8aad0.png)

其他各路电源采用TPS6508640 PMIC
彩框标注为BUCK1,2,6三个大BUCK（外置开关管）
白框标注为BUCK3,4,5三个小BUCK（内置开关管）
需要注意的是Alinx提供的原理图上电感型号和实际板卡上贴装的不同
该PMIC的可编程版TPS650861尝试编程时一直不成功，原因未知。
在Layout时需要注意PGNDSNS等线，严格按参考布线，否则会出现过载误动作，芯片周期性持续重启的问题。
![pic/20260226194542_7fb671ecb1bdd4d55b469fb419007b8b.png](https://barbarian-1306448949.cos.ap-nanjing.myqcloud.com/pic/20260226194542_7fb671ecb1bdd4d55b469fb419007b8b.png)
![pic/20260226195110_5e4ed0f16cde76b19ff926e0da076c24.png](https://barbarian-1306448949.cos.ap-nanjing.myqcloud.com/pic/20260226195110_5e4ed0f16cde76b19ff926e0da076c24.png)