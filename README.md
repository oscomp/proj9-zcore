# proj9-zcore

zcore这个项目是探索把现代系统语言Rust、OS级异步调用机制、Multi-Kernel机制、灵活开放的系统结构RISC-V等带入到操作系统的架构与设计的创新中来，思考未来的操作系统应该是什么样。我们希望通过这个项目为对Rust、RISC-V和操作系统感兴趣的同学营造一个活跃的学习与交流空间，吸引更多对操作系统感兴趣的同学参与。

参与zcore，有很多新东西需要学习，比如Rust和RISC-V等，为此，我们已经2020年暑假与鹏城实验室合作，举办了一个os-tutorial的活动，吸引了不少学生参与，给出了一个自学指导系列教程。很多同学也积极参与，并把他们的学习过程记录了下来，以便于后来的同学进行参考，少走一些坑。

zcore的源码仓库：

- https://github.com/rcore-os/zCore

### 所属赛道

2021全国大学生操作系统比赛的“OS功能设计”赛道

### 参赛要求
- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2021全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

王润基
- github https://github.com/wangrunji0408
- email wrj19@mails.tsinghua.edu.cn

### 难度

中等

### 特征
- 基于Rust语言的操作系统
- 在内核中充分利用Rust提供的异步机制
- 支持google的zircon的大部分syscall
- 支持Linux的部分syscall
- 可运行在用户态
- 可运行在x86, RISC-V（开发中）上

### 文档
- [从零（不懂Rust，RISC-V等）起步基于Rust写OS的学习指导](https://github.com/rcore-os/rCore/wiki/os-tutorial-summer-of-code)
- [zcore发布新闻](https://zhuanlan.zhihu.com/p/137733625)
- [毕设论文和设计文档等](https://github.com/rcore-os/zCore/wiki/documents-of-zcore)


### License

- Apache 2.0 license

## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

在现有zcore的基础上，进一步完成如下目标：

### 第一题：分阶段重新实现简化版zcore

- 与导师协商，形成一系列的小步骤，参考目前的代码，重新按小步骤实现一个简化版的zcore
- 在每个步骤完成后，能够有测试用例，并尽量与OS课程中涉及的内容相关
- 撰写实验设计与分析文档

### 第二题：提供Linux内核的系统服务
- 实现更多的Linux syscall，支持更多的Linux应用
- 参考rCore中移植的smltcp协议栈，把它移植到zCore中，支持Linux网络应用
- 支持virtio的各种驱动

### 第三题：提供zircon内核的系统服务
- 实现更多的zircon syscall，支持更多的Fuchsia应用和服务

### 第四题：完善内核级异步调度机制
- 修改OS架构，支持和完善内核级异步调度机制

### 第五题：支持其他硬件

- 支持ARM，可以在树莓派上运行
- 支持RISC-V，可以在K210/SIFIVE开发板上
