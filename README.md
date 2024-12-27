# 信号分析与处理

![Static Badge](https://img.shields.io/badge/%E8%80%83%E8%AF%95%E8%AF%BE-red) ![Static Badge](https://img.shields.io/badge/%E5%AD%A6%E5%88%86-3-moccasin)

![Static Badge](https://img.shields.io/badge/%E6%88%90%E7%BB%A9%E6%9E%84%E6%88%90-gold)
![Static Badge](https://img.shields.io/badge/%E4%BD%9C%E4%B8%9A-20%25-wheat) ![Static Badge](https://img.shields.io/badge/实验-20%25-wheat) ![Static Badge](https://img.shields.io/badge/%E6%9C%9F%E6%9C%AB%E8%80%83%E8%AF%95-60%25-wheat)

![Static Badge](https://img.shields.io/badge/总学时-48-gold)
![Static Badge](https://img.shields.io/badge/讲课学时-40-wheat) ![Static Badge](https://img.shields.io/badge/实验学时-2*4-wheat)

## 教材与参考书

- 课程 ppt（非常详细，预习、自学、复习都适用）。老师每章之前都会发本章的课件，抓紧时间预习。
- （清华大学）郑君里等，信号与系统（第三版），高等教育出版社。
- （浙江大学）赵光宙，信号分析与处理（第三版），机械工业出版社。
- [美] Alan V Oppenheim 著，刘树棠译，信号与系统（第二版），中国工信出版集团·电子工业出版社。

## 授课教师

- 教师 1：谢晓晨
  - 授课风格：由于学时有限，语速较快，基本没有停顿。但是逻辑非常清晰，讲课的整体思维链也非常连贯。
  - 听课建议：不要走神，不要尝试在课上抄笔记（会跟不上的），课后再整理笔记。

## 学习建议

课程共分为四块：

- 连续信号分析（约 12 学时）
  - 连续信号的时域描述和分析（表示与运算，比较陌生的可能是卷积）；
  - 连续信号的频域分析
    - 周期信号的傅里叶级数（CFS）
    - 非周期信号的傅里叶变换（CFTF，注意从周期信号到非周期信号的过渡）
    - 傅里叶变换的性质
    - 周期信号的傅里叶变换（注意冲激函数的使用，注意周期信号的傅里叶级数 `Fn` 与其傅里叶变换 `F(w)` 的关系）
  - 连续信号的复频域分析（本课程中不作为重点，但还是需要掌握）
- 离散信号分析（约 10 学时）
  - 信号的采样和恢复（时域离散化，频域周期化）
  - 离散信号的时域描述和运算
  - 离散信号的频域分析
    - 离散傅里叶级数（DFS）
    - 离散时间傅里叶变换（DTFT）
    - 离散傅里叶变换（DFT）：相对比较抽象，多花一些时间理解
  - 快速傅里叶变换及应用（FFT）
  - 离散信号的 z 域分析（本课程中不作为重点，但还是需要掌握）
- 信号处理基础（约 4 学时）
  - 系统的描述及其六大性质
  - 信号的线性系统处理
    - 时域法分析：时域法解微分方程或差分方程
    - 频域法分析：频率特性、无失真传输
    - 复频域分析：利用拉氏变换或 z 变换来解微分方程或差分方程
- 滤波器（约 6 学时）
  - 滤波器概述：滤波的概念及其基本原理；滤波器的分类；滤波器的技术指标
  - 模拟化设计：重点掌握 Butterworth 低通滤波器的设计
  - 数字化设计：重点掌握无限冲激响应（IIR）数字滤波器的设计：冲激响应不变法、双线性变换法

> by [Gaster](https://github.com/WDGaster703),2024.12

23级信号相比22级，理论部分增加了8学时，总体内容不变，学时分配为：
- 绪论（约 2 学时）
- 连续信号分析（约 12 学时）
- 离散信号分析（约 12 学时）
- 信号处理基础（约 6 学时）
- 滤波器（约 8 学时）

> by [psp_dada](https://github.com/pspdada), 2024.11


本课程专注于信号**分析**与**处理**的核心概念。

课程内容整体来说抽象层级较高且包含大量新概念，学时偏少导致许多概念难以理解，尤其是上课时第一次接触那么多级数与变换（CFS、CTFT、DFS、DTFT、DFT、FFT）而容易感到头皮发麻。但通过深入学习和细致理解，你会发现这些概念之间存在内在的联系和相似性，有助于更有效地掌握。

概念之间的联系之一：**对偶**

在课程中，我们将探讨时域和频域性质之间的诸多**对偶**关系：`时域离散性——频域周期性`、`时域连续性——频域非周期`、`时域周期性——频域离散性`、`时域非周期——频域连续性`。以及连续信号与离散信号的级数和变换的定义的惊人的**对偶**特性，如 CFS 中的 `Fn=F(nω_1)` 与 DFS 中的 `Xk=X(kΩ_0)` 的定义形式上十分类似， CTFT 中的 `F(ω)` 与 DTFT 中的 `X(Ω)` 也具有类似的结构。

**对比学习法**

为了更好地理解和掌握这些概念，我建议采用**对比**学习的方法，将连续信号（第一章）与离散信号（第二章）出现的诸多性质并列比较。这种方法不仅能够加深对每个概念的理解，还能揭示它们之间的关联，使学习过程更加高效。

对于自动化专业的学生而言，学习信号这门课的帮助不仅仅局限于这门课。这门课以频域分析作为重点，对理解自控理论中线性系统的频域分析有帮助；此外也能加深学生们对于复频域（连续的 s 域和离散的 z 域）的理解与计算能力，以及复频域在系统上的应用（毕竟对系统复频域的计算远比频域方便）。

## 关于考试

> by [phychi](https://github.com/phychi), 2023.12

- 20 平时分（作业）+20 实验+100 分折合 60 分的考试。这次考试我考的还行（作业接近 20 分+实验 20 分+卷面 83 分）。
- 我并不是一个成绩很好的学生。按照这次经验，实验的 20 分基本上你按时给老师检查，按时交报告就能拿满。对于作业，自己写完后来 openauto 项目对答案，在助教批改扣分前解决错误，可以拿比较高的分数（不能抄答案，这样会似懂非懂，计算能力也会不够）考试的题目算比较基础的，你一开始听说信号分析与处理=（信号与系统+数字信号处理）的浓缩版，还只上 2.5 学分。内容确实很多，但是不要被吓到，有些东西是不会考的，例如一开始的卷积的定理的证明（显得太数学了），还有一些赶进度最后 FIR 数字滤波器应该也能意识到不会考。
- 包括这门课在内的其他几门课都有一个很大的缺点：除了作业题和 PPT 题目没有其他参考题可写！因为上课内容对赵光宙的教材内容也是浓缩取舍，而且没有官方答案。这个问题可能是导致大家发挥不够好的原因之一（我看了上课班次排名是 11/126，这可是卷面分 83），有空多做一点题锻炼计算能力熟练度（我是计算能力不行 2 个小时都没算完）

> by [psp_dada](https://github.com/pspdada), 2024.12

- 平时分 20/20，实验分 19/20，期末分 94/100 -> 95: 排名 5/135

24 年秋的信号期末考试在同学们对这门课所学习的内容有一定了解（参考上一节我写的“学习建议”部分）之后，整体的**难度不大**，基本都是一板一眼的题目。这门课由于学时过少，使得本可以掌握许多新知识点的课程最终也沦为了大背诵。

对于这门课的考试，掌握作业题以及往年题已完全足够。此处的“掌握”并不只仅仅指完成即可，因为这门课本身需要思考的部分比较多，消化吸收新接触到的概念和性质的难度也十分大，因此希望大家能多从作业中**体会、理解**知识点，形成自己对于**信号分析与处理**的理解。但大家也不要因为这门课的难度而灰心丧气，若花费许多时间和精力仍对这门课的知识点感到困惑，可以多和老师（xxc 老师真的很好很热心）助教以及同学们交流，若实在无法理解，也无需太过担心，毕竟其实我也没有完全理解）。

我分享了我本学期学习这门课程时所作的作业详解以及往年题详解（与其他同学进行过多次讨论校对，但如果仍有错误欢迎修改），希望对大家有所帮助。

我实验分扣了一分大概是因为过了交实验报告的 ddl 才补交导致的，因为当时需要交实验报告的课程太多了，所以有点混乱忘了交，大家引以为戒）。

24 年秋考试可以携带计算器。
