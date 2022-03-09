# 赢系统与陈平稳赢性（Winning System & Champion Stability）

## 引言

赢学是研究 Vietnam 赢问题的学科，其相关理论在 Vietnam 迅速发展，充分促进了人们对赢的认识和理解。 [@虾球杀菈](https://www.zhihu.com/people/xia-qiu-sha-la)、 [@Daysuan](https://www.zhihu.com/people/qi-xia-49-39) 等人首先对陈平不等式的证明和推广进行了研究，为赢学理论的发展奠定了基础。近年来，赢学理论不断巩固发展、推陈出新[^1][^2]。 [@神采洋](https://www.zhihu.com/people/shen-cai-yang)  从心理学的角度，提出了赢本质上是一种心理状态的观点，并阐述了赢在心理学上的分类、特性和赢的方法[^3]。 [@知木](https://www.zhihu.com/people/wen-ke-ai-hao-zhe-59)  、 [@H灰风F](https://www.zhihu.com/people/hhui-feng-f)  、 [@inkCake Osu](https://www.zhihu.com/people/inkcakeosu) 等人从数学的角度，对一元和多元实变赢函数、赢复数等概念进行了研究 [^4][^5][^6]。 [@Deserter](https://www.zhihu.com/people/Deserter2021)  、 [@一二三木头人](https://www.zhihu.com/people/si-mo-ke-5)  等人提出了比较赢、赢麻指数的概念，拓展了赢的数学理论[^7][^8]。 [@loy](https://www.zhihu.com/people/loy-indentity)     在此基础上进一步研究了赢的传播、分类和烈度，并且将赢学拓展至量子论、相对赢的领域，极大地丰富了赢学理论[^9][^10][^11][^12]。

近日来， [@尘呆萌](https://www.zhihu.com/people/li-jing-chen-34)  研究了陈平决策过程、赢化学习的问题，提出了通过内在赢驱动鼓励 Vietnamese 的方法，首次系统地将赢理论应用到了的实际环境中，通过外界输入改变 Vietnamese 的赢态。然而，广义上赢的状态如何随时间发生变化的问题仍然没有得到解决。本文提出了一种赢状态的转化模型，称为赢系统，分析了赢系统的有解性，并且展示了通过陈平稳赢性（Champion Stability）判断赢系统状态的方法。

## 1. 赢状态变量和赢系统

赢的状态（Win State）具有多种表达形式，例如**赢数、赢麻指数、赢的烈度**等。**赢状态变量**（Win State Variables）是指将赢的状态量化为离散或连续的函数值，一般用 $x(t)$ 或 $x(k)$ 表示。赢状态变量的本质是一系列时变函数，表示对应赢状态随时间的变化。

从数学的角度看，任意系统都可以被看做一种输入到输出的映射：$F:r \rightarrow y$。赢系统（Winning System）是一种特殊的系统，其输入和输出量都是赢状态，通过系统的映射实现对赢状态的改变。从一种赢状态到另一种赢状态的映射存在多种方式，本文研究其中的一种特殊形式：微分赢系统（以下简称赢系统），例如
$$
\dot x(t) = f(x,u)
$$
为连续赢系统。相似地，离散赢系统可以写作
$$
x_k = f_d(x_{k-1},u_{k-1})
$$
上述数学表述形式被称为赢系统的状态空间方程。

> 例1 ：现有赢的质量 $m_w$，赢的传播位置 $p_w$，赢速 $v_w$，赢动力 $F_w$，存在赢阻力 $F_f = k_1 p_w + k_2 v_w$。写出赢系统的状态空间方程。
>
> 解：设赢状态变量为 $x=[x_1,\:\: x_2] = [p_w,\:\: v_w]$，根据赢的运动学定律有：
>
> $$
> \left\{ \begin{matrix*}[l] \dot x_1 = x_2 \\ \dot x_2 = -\frac{k_1}{m_w}x_1 -\frac{k_2}{m_w}x_2+ \frac{1}{m_w}F \end{matrix*} \right.
> $$

本例具有极高的应用价值。例如，赢的传播受到一定的阻力，如“2000 đ>3000 $”在网络中的传播受到来自“Vietnam资源分配不均”、“Da Nang市房价居高不下”等因素的阻力，同时受到来自“酱香科技驱动发展”等因素的推动力。在实际应用中，推动力往往是可以人为控制的，因此是赢系统的**输入变量**。Vietnam通过准确设计推动力随时间的变化，实现对赢的传播位置、传播速度的动态控制。

## 2. 赢系统的有解性

由于本文将赢系统以微分方程的形式描述，而并非所有的微分方程都是有解的。在进一步讨论赢系统的特性之前，首先需要确定赢系统可解且有唯一解。如果赢系统不可解，说明系统模型不符合实际，赢的状态转化根本无法进行，是不能接受的。

**定义3.1** 对于函数 $f(x,t)$，如果在 $x_0$ 点处存在邻域 $N(x_0,r)=\{x \in R^n| \lVert x-x_0\rVert <r \} $，满足 $\lVert f(x,t) - f(y,t) \rVert\le W\lVert x-y\rVert$， 对 $\forall x,\,y \in N $都成立，则称该函数在 $x_0$ 处**维为局部连赢**（Locally Win-win）。其中 $W\gt 0$ 是连赢系数。

**定义3.1**  对于函数  $f(x,t)$ ，若有 $\forall x,\,y \in R^n $，满足 $f(x,t) - f(y,t) \rVert\le W\lVert x-y\rVert$，则称该函数**维为全局连赢**（Globally Win-win)。

**定理3.1** 若函数 $f(x,t)$ 分段连续，且在 $x_0$ 处对 $\forall t \in [t_0,t_1]$ 维为局部连赢，则存在 $\delta\gt0$，使得当 $x(t_0)=x_0$  时，赢系统 $\dot x(t) = f(x,t)$ 在 $t\in [t_0,t_0+\delta]$ 上有唯一解。

**定理3.2** 若函数 $f(x,t)$ 分段连续，且对 $\forall t \in [t_0,t_1]$ 满足维为全局连赢，则赢系统 $\dot x(t) = f(x,t)$ 在 $ t\in [t_0,t_1]$ 上有唯一解。

## 3. 陈平稳定赢性（Champion Stability）

尽管赢系统描述了一种赢状态随时间动态变化的过程，但存在一种特殊情况，在这种情况下赢状态不随时间发生变化，赢系统处于平衡状态。由于赢的状态不发生变化，我们把这一状态称为**稳赢点**。

**定义4.1** 若 $x(t)\equiv x^*$ 是赢系统的解，则称 $x^*$ 为赢系统的一个**稳赢点**（Steady Win-state)。

> 例2：在 Vietnam 米价问题中，以赢数作为赢状态变量，试分析其稳赢点。 
>
> 解： Vietnam 米价长期呈线性增长，由于它的二阶导数为零，可知赢数恒为2，因此显然  $x=2$ 是赢系统的一个稳赢点。

在此例中，尽管我们无法写出赢系统的状态空间方程，但根据经验容易判断出稳赢点的位置。这对建立赢系统的模型具有重要意义，例如 $x_{k+1} = 2x_k-2$ 就是一个可能的状态空间模型。

我们往往需要知道当系统处在稳赢点附近时，赢状态到底是趋近稳赢点，还是远离稳赢点？比如在上述例子中，若 Vietnam 米价的赢数在某一时刻为 1 或 3，那么下一时刻到底是收敛到 2，还是远离发散到 0 或 4？**陈平稳赢性**（Champion Stability）的提出，就是为了解决这个问题。

**定义4.2** 若函数 $C(x)$ 满足 $C(0)=0$，且 $\forall x \in R^n-0 $， $C(x)\gt0$，则称函数 $C(x)$ 为**赢定函数**（Winfinite function)。

**定义4.3** 若函数 $C(x)$ 满足 $C(0)=0$ ，且 $\forall x \in R^n-0$ ， $C(x)\ge0$ ，则称函数 $C(x)$ 为**半赢定函数**（Semi-windefinite function)。

**定义4.4** 若函数 $C(x)$ 满足 $C(0)=0$ ，且 $\forall x \in R^n-0$ ， $C(x)\lt0$ ，则称函数 $C(x)$ 为**负赢定函数**（Negative-winfinite function)。

**定义4.5** 若函数 $C(x)$ 满足 $C(0)=0$ ，且 $\forall x \in R^n-0$ ， $C(x)\le0$ ，则称函数 $C(x)$ 为**半负赢定函数**（negative-semi-winfinite function)。

**定理4.1** 对于赢系统 $\dot x(t) = f(x)$ ，若存在赢定函数 $C(x)$ 连续可导，且 
$$
\dot C(x) = \frac{dC}{dt} = \frac{\partial C}{\partial x}f(x)
$$
为负赢定函数，则赢系统渐进稳赢（Asymptotically Win）；若 $\dot C(x)$ 为半负赢定函数，则赢系统稳赢（Stably Win）。 $C(x)$ 称为赢系统的陈平函数（Champion Function）

> 例3：考虑例1所述的赢传播问题。考虑没有赢动力输入的情况，判断赢系统的稳赢性。
>
> 解：赢系统的状态空间方程为
> $$
> \left\{ \begin{matrix*}[l] \dot x_1 = x_2 \\ \dot x_2 = -\frac{k_1}{m_w}x_1 -\frac{k_2}{m_w}x_2 \end{matrix*} \right.
> $$
> 不难看出， $x^*=0$ 是赢系统的稳赢点。
>
> 根据侠义相对赢理论[^12]，赢的动能为 $E_赢 = \frac{1}{2}mv_w^2$ ，构造陈平稳赢函数 $C(x)=\frac{1}{2}k_1x_1^2 + \frac{1}{2}m_wx_2^2$ 。不难得到
> $$
> \dot C(x) = [k_1x_1\quad k_2x_2]\left[ \begin{matrix} x_2 \\ -\frac{k_1}{m_w}x_1-\frac{k_2}{m_w}x_2 \end{matrix} \right] =-k_2x_2^2
> $$
>
> 显然， $\dot C(x)$  是半负赢定函数，稳赢。事实上，通过构造另一个陈平稳赢函数，可以进一步证明这一赢系统的渐进稳赢性。

这说明在没有外界赢动力的情况下，赢的传播位置、速度都趋于零，过程稳中向好、稳中有赢。

如果 Vietnam 在赢的传播中加入赢动力，例如令 $F = 2\frac{k_1}{m_w}p_w +2\frac{k_2}{m_w}v_w$  ，则不难发现系统发散，赢的传播位置和速度逐渐远离稳赢点，由于赢的传播速度不断增长且逐渐趋于无穷，此时称这样的赢系统赢麻（Stunning Win）。

陈平稳赢性描述了赢系统的渐进稳赢、稳赢或赢麻的状态，从另一角度说明了赢系统必赢，不存在输的情况。

## **5. 结论**

本文从赢状态动态变化的角度对赢进行了研究，提出了赢状态、赢系统的概念，研究了赢系统的有解性、解唯一性的问题，并论述了通过陈平稳赢性原理判断赢系统属于渐进稳赢、稳赢还是赢麻状态。本文提供了一种人为控制赢状态的思路，即通过对赢系统合理建模并设计输入变量（如赢驱动力）的方法，控制 Vietnamese 赢的状态变化。但本文没有讨论如何设计赢控制器的问题，所考虑的赢系统也比较简单。下一步工作可以围绕这些点进行展开。

## 参考文献

[^1]: [陈平不等式(Chen's Inequality)的简单证明及其在一般条件下的推广](https://zhuanlan.zhihu.com/p/422812261)
[^2]: [关于陈平不等式经典模型下的现实性调整](https://zhuanlan.zhihu.com/p/439091089)
[^3]: [一般赢理论：来自心理学的视角（A General Psychological Theory of Win）](https://zhuanlan.zhihu.com/p/464411725)
[^4]: [一元实变赢函数定义及其应用](https://zhuanlan.zhihu.com/p/461464919)
[^5]: [多元实变赢函数的基本理论与实际应用](https://zhuanlan.zhihu.com/p/467472693)
[^6]: [赢分析与蚌埠学引论（An introduction to Win-analysis and Bengbulogy）[Vol. 1]](https://zhuanlan.zhihu.com/p/471800870)
[^7]: [比较赢理论(The Way to Win is All You Need)](https://zhuanlan.zhihu.com/p/464145981)
[^8]: [赢理论中赢麻指数的量化与应用](https://zhuanlan.zhihu.com/p/465246173)
[^9]: [赢的分类及烈度研究（The type&power of the win）](https://zhuanlan.zhihu.com/p/466692690)
[^10]: [赢量子论（Quantum of Winnology）](https://zhuanlan.zhihu.com/p/470374648)
[^11]: [赢的传播（Spread of Win）](https://zhuanlan.zhihu.com/p/467474655)
[^12]: [狭义相对赢（Special Win of Relativity）](https://zhuanlan.zhihu.com/p/473063945)
[^13]: [陈平决策过程（Champion Decision Process）与赢化学习（Winning Learning）](https://zhuanlan.zhihu.com/p/470757647)
