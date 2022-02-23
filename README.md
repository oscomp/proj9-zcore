# proj9-zCore

zCore 是一个基于Rust语言的开源操作系统内核，最初目标是用Rust 语言重写的Google基于C++的 Zircon 微内核。目前zCore进一步发展为内核级支持Rust的异步机制，新的处理器RISC-V，支持Intel 新CPU的用户态中断机制，支持Linux应用等新型操作系统，并将用于各自AIoT系统中，如无人机，无人车等。zCore内核能充分发挥Rust语言的优势，具有小巧、安全、高性能、开发便捷等特征。

这个项目探索把现代系统语言 Rust、OS 级异步机制、Multi-Kernel 机制、灵活开放的指令集架构 RISC-V 等，带入到操作系统的设计与实现创新中来，是对未来操作系统的一种尝试。

我们希望这个项目能为对 Rust、RISC-V 和 OS 感兴趣的同学营造一个活跃的学习与交流空间，吸引更多同学参与开发。为此，我们已经在 2020年暑假与鹏城实验室合作，2021年暑假与启元实验室合作，举办了一个 [os-tutorial 活动](https://github.com/rcore-os/rCore/wiki/os-tutorial-summer-of-code)，给出了一个自学指导系列教程。这一活动吸引了全国多所学校的同学参与，他们也将学习过程记录下来，以便于后来的同学进行参考，少踩一些坑。

zCore 的源码仓库：

- https://github.com/rcore-os/zCore

### 所属赛道

2022全国大学生操作系统比赛的“OS功能设计”赛道

### 参赛要求
- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2022年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2022全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

张译仁
- github https://github.com/DeathWish5
- email zhang-yr20@mails.tsinghua.edu.cn

陈渝
- github https://github.com/chyyuu
- email  yuchen@tsinghua.edu.cn
 
### 难度

中等

### 特征
- 基于 Rust 语言，并充分利用了 Rust 提供的异步机制
- 支持 Zircon 微内核的大部分 syscall，以及 Linux 内核的一部分 syscall
- 可以 LibOS 的形式运行在用户态，或以传统 OS 的形式运行在裸机上
- 可运行在 x86_64 和 RISC-V（开发中）上

### 文档
- [清华大学OS课程实验指导：从零开始基于 Rust 写 RISC-V based OS kernel](https://rcore-os.github.io/rCore-Tutorial-Book-v3/)
- [zCore 发布新闻](https://zhuanlan.zhihu.com/p/137733625)
- [毕设论文和设计文档等](https://github.com/rcore-os/zCore/wiki/documents-of-zCore)


### License

- Apache 2.0 license

## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

在现有 zCore 的基础上，进一步完成如下目标：

### 第一题：分阶段重新实现简化版 zCore

- 与导师协商，形成一系列的小步骤，参考目前的代码，重新按小步骤实现一个简化版的 zCore
- 在每个步骤完成后，能够有测试用例，并尽量与 OS 课程中涉及的内容相关
- 撰写实验设计与分析文档，参考：[zCore Tutorial](https://github.com/rcore-os/zCore-Tutorial)

### 第二题：提供 Linux 内核的系统服务
- 实现更多的 Linux syscall，支持更多的 Linux 应用，如GCC编译器，Rust编译器等。
- 参考 rCore 中集成的 smoltcp 协议栈，把它移植到 zCore 中，以支持 Linux 网络应用
- 支持 virtio 的各种驱动

### 第三题：提供 Zircon 内核的系统服务
- 完善 Zircon syscall，支持更多的 Fuchsia 应用和服务
- 尝试支持磁盘驱动、网卡驱动、显卡驱动以及 GUI 程序

### 第四题：完善多核支持及异步调度机制
- 完善 x86_64 多核支持，能够在多核上正确运行多线程程序
- 修改 OS 架构，支持和完善内核级异步调度机制

### 第五题：支持其它指令集和硬件
目前已经支持X86 计算机和基于RISC-V 64的哪吒D1开发板

- 在ARM64 based 树莓派4开发板上运行
- 在RISC-V 64 based SIFIVE u740/u540 计算机上运行
- 在新一代x86-64 至强可扩展处理器（Sapphire Rapids） 计算机上运行，支持用户态中断。
