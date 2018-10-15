## Xv6，一个简单的类Unix教学操作系统

### 介绍
Xv6 是 2006 年夏天为麻省理工学院的操作系统课程（6.828: Operating System Engineering）开发的教学操作系统。我们希望 xv6 在其他课程中也会有用。此节收集资源以帮助在其他课程中使用 xv6，包括对源代码本身的评论。

### 历史和背景
多年来，麻省理工学院没有操作系统课程。2002 年秋天，创建了一个用于教授操作系统工程的人员。在课程讲座中，该课程使用 John Lions 的着评注的第六版Unix（aka V6）。在实验任务中，学生为英特尔 x86 编写了大部分外部操作系统，最终命名为 JOS。让学生接触到多种系统（v6 和 JOS），有助于培养学生对操作系统设计的理解。

V6 从一开始就提出了教学挑战。学生们怀疑在过时的硬件（PDP-11）上运行的并用过时的编程语言（pre-K＆R C）编写的过时的 30 年前操作系统的实用性。学生们也在努力同时学习两种不同架构（PDP-11 和 Intel x86）的低级细节。到 2006 年夏天，我们决定用一个新的操作系统 xv6 取代 V6，这个操作系统以 V6 为模型，但是用 ANSI C 编写并在多处理器 Intel x86 机器上运行。Xv6 使用 x86 使其与学生的体验相比，与 V6 相比，并且围绕单一架构统一了课程。添加多处理器支持需要使用锁和线程处理并发（而不是使用特殊情况下的解决方案，例如启用/禁用中断）并帮助实现相关性。最后，编写一个新系统允许我们编写更清晰的 V6 部分，如调度程序和文件系统。6.828 在 2006 年秋季使用 xv6 代替 V6。

### Xv6 源码和教材
最新的 xv6 源和教材可通过

`git clone git：//github.com/mit-pdos/xv6-public.git`

`git clone git：//github.com/mit-pdos/xv6-book.git`

我们也以印刷小册子的形式分发资料，每页都有行号，这样大家在上课时就能聚在一起，这本小册子叫 [xv6-rev11.pdf](https://pdos.csail.mit.edu/6.828/2018/xv6/xv6-rev11.pdf)，一起的还有 [教材](https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf)。本书中的行号是指源小册子。

xv6 使用 GNU C 编译器编译，使用 ELF 二进制文件以 x86 为目标。在 BSD 和 Linux 系统上，您可以使用本机编译器; 在不使用 ELF 二进制文件的 OS X 上，必须使用交叉编译器。Xv6 确实能在真实硬件上启动，但通常我们使用 QEMU 仿真器运行它。GCC 交叉编译器和 QEMU 都可以在 6.828 工具页面上找到。

### Xv6 讲义材料
在 6.828 中，课程上半部分的课程涵盖了 xv6 的源码和教材。下半部分的课程使用研究论文考虑高级主题; 对于某些人来说，xv6 是进行具体讨论的有用基础。讲义可从 [教学计划](Schedule.md) 页面下载获得。

### Xv6 作业
Xv6 主页包含小编程练习，以有趣的方式扩展 xv6。通过动手处理 xv6，学生有机会吸收 xv6 并探索文本中未涉及的想法。家庭作业可从 [教学计划](Schedule.md) 页面获得。

### Unix Version 6

6.828 的 xv6 受 Unix V6 的启发:
* Lions' Commentary on UNIX' 6th Edition, John Lions, Peer to Peer Communications; ISBN: 1-57398-013-7; 1st edition (June 14, 2000).
    * [在线版本](http://www.lemis.com/grog/Documentation/Lions/) 和 [源代码](http://v6.cuzuco.com/)
    * v6 [源代码](http://minnie.tuhs.org/cgi-bin/utree.pl?file=V6) 也可以通过 [Unix Heritage Society](http://www.tuhs.org/) 在线获得

以下内容对于阅读原始代码非常有用：
 * The PDP11/40 Processor Handbook, Digital Equipment Corporation, 1972.
    *  [PDF](http://pdos.csail.mit.edu/6.828/2005/readings/pdp11-40.pdf)（扫描版本，不可文本搜索）
    * 由指令名称索引并且 [基于 Web 的版本](http://pdos.csail.mit.edu/6.828/2005/pdp11/)。
