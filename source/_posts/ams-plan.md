---
title: Developing Plan for AMS
tags:
- Plan
- Minecraft
---
## Carpet-AMS-Addition维护
### 合成表相关API
计划采用Fabric API在编译期用来生成各个版本的数据包，用以动态装载/卸载（主要是考虑兼容性，所以尽量采取Minecraft官方的手段来修改）

### features
之前更新build.yml的时候漏掉了Mixin Audit相关，计划加回去

## 备份
### Prime Backup Extnsions?
镜像服、创造服专用的管理插件。考虑在镜像服中常常有临时的测试需求，但同时也经常有人在镜像服设计建筑、机器。

目前，已经有multi-source的Prime Backup插件，可以从多个MCDR的prime backup实例中摘取部分region文件用来回档。

考虑进一步整合如下功能：
- 多个创造服、镜像服的互相同步、资源分配、开关控制
- 区块级的热备份、热回档

目前第一个大概就是缝合一下multi source prime backup和多服务器启动管理的插件。当然，我比较趋向的想法其实应该是多维度的那种，也不需要特别管理某个世界的占用。

然后第二个肯定需要mod来结合，应该可以提取一个“单区块的mca文件”然后用来读取，类似于作为一个新维度装载。

## Version Revert
主要对1.20.5+的存档向下转换。1.20.5开始将nbt的机制改变为组件，希望写一个小脚本或mod让1.20.5+存档能初步向下转化。

## 模组计划
### Item Scroller CraftAddon
#### 主要添加功能
- 切石机、铁砧等
- 基于配方书的massCraft

#### 主要目标
升级到高版本。主要是将Sakura-Ryoko的版本向上移植。

### Oh-My-Minecraft-Client
考虑到plusls相关模组的维护最近相对减少，考虑将Oh-My-Minecraft-Client中的查看村民交易的功能使用原版方式（F3+I）进行实现。这一方式的好处是可以用更原版的方式进行支持，从而避免一些跨版本情况下的协议兼容性问题；另一方面是可以相当于依赖更新更活跃的Carpet-TIS-Addition。