---
title: zhouyuhan-stage2 and stage 3
date: 2025-04-22 17:14:37
tags:
    - author:<zhouyuhan>
---
## 训练营学习记录

这篇文章用来记录我在2025春夏季开源操作系统训练营的学习过程，之所以会参加本次训练营，是因为我想进一步学习操作系统以及学习操作系统以及通过完成rcore包括通过完成组件化操作系统进行进一步磨练自己。

## 训练营二阶段关于rcore实验完成记录

在第二阶段的学习过程中，我收获颇丰，深入理解了 Rust 语言和操作系统的核心概念。在学习 Rust 语言时，我全面掌握了其独特的所有权、借用和生命周期规则，这些特性为 Rust 提供了强大的内存安全保障。而在操作系统方面，我不再停留在浅显的层面，而是深入探讨了内核架构，从系统启动到各个模块的交互过程有了清晰的认知。特别是在进程管理方面，我了解了进程的创建、销毁及状态转换的原理，并深入分析了不同调度算法对 CPU 资源分配的影响。

在内存管理方面，我深入研究了物理内存分配与虚拟内存映射的机制，了解了页表机制在其中扮演的关键角色，惊叹于内存管理的复杂性与精巧性。在我的个人项目中，我将 Rust 和操作系统的知识结合，参与了从设计、实现到调试的全过程，解决了许多技术难题，这一过程让我不断成长和提升。

这一阶段的学习为我打开了全新的视野，未来我将继续深入探索，将所学的知识更好地应用于实践。

## 训练营三阶段关于arceos实验以及挑战实验

print_with_color
通过使用 ASCII 字符，实现了简单的控制台颜色输出。

support_hashmap
为了快速实现功能，引入了一个现成的库来处理哈希映射。

alt_alloc
由于测试用例较为简单，实现难度较低。严格按照要求实现后，我对是否完全正确也并没有特别的把握。

shell
在原有的 Shell 实现中，已经有了 rename 功能。为了简化，我直接调用了现有库来处理 rename，同时利用文件创建、复制文件内容和删除原文件的方式，模拟了 mv 命令的功能。

sys_map
通过使用 find_free_area 来找到合适的内存区域并进行数据读取，尽管 find_free_area 找到的内存地址并不完全符合 man mmap 的描述，但依旧能够实现所需的功能。

page_fault
难度适中，相比于原先的实现，这部分内容更多是基于 rcore 的基础进行了延伸与补充。

simple_hv
通过修改 guest 的 sepc 寄存器值，并设置 a0、a1 的值，成功实现了一个基础的 Hypervisor 操作。