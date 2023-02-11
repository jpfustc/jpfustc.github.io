# Works by Stuart Kauffman

Stuart Kauffman的一本小册子 *The world beyond physics* 是2022年读的最重要的书之一. 我在一些科普读本中, 在代码设计的blog中以及一些雪球上的讨论中陆续地看到他的内容, 很庆幸没有错过.

我在高中时非常着迷于拉普拉斯妖: 只要知道宇宙中所有微粒的位置和动量, 就可以计算出过去, 现在和未来. 现在看来, 这份着迷来来自中学物理基础上的还原论. 很快, 热统和量力把这份地基摧垮了, 但还原论还在新的地基上立着, 暂时找不到合适的替代品. 这本书提供的数理分析和构想, 提供了一种新鲜的视角.

故事从一个天文数字讲起: 20种氨基酸组成长度为200的肽链, 存在10^260种可能. 这个数字比宇宙粒子数和宇宙年龄的乘积还要大. 还有不少例子可以构造天文数字: 52张扑克牌可以组成10^68种顺序, 纵横19道围棋有10^170种棋局; 64个密码子对应20种氨基酸外加终止子, 有10^84次方种配对; 只需要少量的组分的笛卡尔积就可以构造出恐怖的复杂度, 而只有极小部分发生了, 并被赋予意义, 这一小, 一大, 再一小三个数字之间的矛盾是如此尖锐又如此普遍: 生物大分子, 神经系统, 社会经济网络, 棋牌, 文学, 它们不得不需要某种"恰好如此"以外的解释,而生命比起人造物尤其需要解释.

生命是耗散自由能维持非平衡态的物理系统; 是一个通过控制自身, 使自身持存的控制系统. 第一个定义来自薛定谔, 第二个定义来自刘大可的"生命的起源". 这里的第二个定义稍有歧义: "通过...使"究竟是指效果, 还是指"目的"? 前者看起来是一个更加客观和物理的解释, 事实上原著专门避免了这个歧义而"效果".

Stuart Kauffman给生命的定义有三层: 首先是一个做功闭合体系, 在一个做功周期中包含了构造约束系统的全部过程; 其次是一个约束闭合系统, 使得能量以需要的方式做功, 做功的结果就是复制同样的约束系统; 最后是一个催化闭合体系. 某种程度上, 三个体系其实是一个: 催化不正是一种统计意义上的化学能做功约束么.

与"使自身持存"的结果相比较, 这个定义中更强调"复制自身", 传播有序度. 这种字面上的分歧可以被整体视角统一起来: 无论是自催化集体的分子集合, 还是以种群为单位进化的物种, 生命在它的全部历史中都以一定数量的的集体形式而存在. 那么, 使自身持存, 可以解释为种群意义上的持存, 而个体生命的延续, 不过是前者做功周期的一个小环节.

各种闭合体系还有不少例子. 分子云的密度随机涨落形成了恒星, 恒星引力对周围分子云的扰动进一步加剧了密度随机涨落, 这不就是一个传播有序度的做功闭合体系么? 朊毒体, 一种变异蛋白, 可以催化正常蛋白变异成和自身一样的变异蛋白, 也是一样. 不过, 这些例子都没有和"组合复杂度"的概念联系起来.

闭合体系的要求是"所有需要的都存在", 不能少, 但可以多: 初代恒星中的超新星爆发撒播了重元素, 使得更复杂的结构成为可能. 这些"多余成分"恰恰成为





## Drafts

频繁看到关于复杂系统的话题. 把相关的阅读都整理到这个页面下

## [How complex systems fail](https://how.complexsystems.fail/)

* 这篇文章的作者Richard Cook来自芝加哥大学"认知技术实验室". 他对"复杂系统失效"的分析也是非具体的.
* \[1\]风险是复杂系统的固有特征. \[5\]复杂系统通常总是在不断演变的非理想状态下运行: 需求的变化, 时效压力, 组件迭代, 维护缺位, 决定了系统没有一个静态的理想状态, 更不可能简单地向这一目标收敛.
* \[3\]系统崩溃往往是多重失效的复合结果. \[4\]在见证这种组合效应之前, 设计者很难预判系统的失效方式并予以完全的预防. \[2\]正常工作的复杂系统往往通过冗余保护来分隔各个失效. 这种被动防御一方面起到很好的效果, \[6\]另一方面永远是不充分的.
* \[7\]作者就此指出: 事后的"根因分析"是一种错误的做法, 尤其是唯一根因分析: 暴露出的系统的问题是多重隐性问题的组合. 归因更多是人们"找出一个被指责的对象"的心理需要在作祟. \[8\]而且往往收到后视镜偏见的影响: "怎么连这个都没想到", "这种做法下灾难是不可避免的". \[15\]针对系统问题打补丁时, 由于系统泵困本身是多重因素以特定方式共振引起的小概率事件, 如果不小心评估和控制改动引起的额外耦合, 这些补丁可能反倒增加出问题的概率和定位难度.
* \[9\]复杂系统中的操作者同时肩负两方面的任务: 一方面维持系统的日常运转和产出, 另一方面规避可能放生的风险. 安全是要牺牲效率换取的. 外来视角常常在不出问题时低估风险强调效率, 而在事故后高估风险强调安全. \[10\] 基于复杂系统自身某种程度的不可知性, 以及两种任务的权衡, 所有干预和操作总有赌博的色彩. \[11\]甚至于, 在采取行动以前, 整个系统的目标, 安全还是效率, 都是混沌而模糊的, 连一团可以描述的概率云都不是. 人为干预和操作在各个环节消除这种模糊性, 使系统坍缩到一个具体的状态.
* \[16\]与系统的功能性一样, 系统的安全性也是一个"涌现性质", 不是各个组件性质的简单叠加.
* \[12\]\[13\]\[14\]\[17\]\[18\]略

## Drift into failure [Link 1](https://sidneydekker.stackedsite.com/wp-content/uploads/sites/899/2013/01/DekkerDriftRiskChapter2013.pdf) [Link 2](https://safetydifferently.com/wp-content/uploads/2014/08/SDDriftPaper.pdf)

* 有两篇以此为题的文章, 一篇是为"Nonlinear Dynamics"这本书的约稿; 另一篇是论文.
* 前者除了将complexity and systems theory 摆在Newton-Cartesian approach, which means going down and in的对立面之外贡献不大. 金融危机的引子没有起到多少关联作用.

## The origins of order: self organization and self selection

* 不记得在哪里下到这本书了, 所以没有链接
* 主题在重新构造进化模型上. 先从第六章"复杂系统的自组织与适应"读起.
* "有组织的秩序, 无组织的复杂, 有组织的复杂"
* "秩序与混乱的边缘"
* Mathematical foundation of complex system, dynamical attractors: boxing the behavior of a system into a small parts of its state space
* random NK boolean networks
    * complex regime, where frozen component is just percolating and the unfrozen component just ceasing to percolate, hence breaking up into isolated islands. Alternating the activity of single unfrozen elements unleashes avalanches of change iwth a characteristic size distribution having many small and few large avalanches.
    * Emergence of order does not require that all details of structure and logic be controlled precisely. Refer to Chapter 12 for illustration with regard to ontogenesis(个体发育过程)
* Fitness landscape versus network regime. Refer to chapter 2 and 3 for NK landscape model
* Complex systems' capacity to perform complex tasks.
    * Poised system on the edge of chaos

**Dynamical systems**
* Dynamical systems theory: differential equations, rate of change of variable vector determined by present state.
* Steady state as "attractor", endpoint of all state-transition trajectories
* one dimension attractor of a cycle; higher dimensional attractor of multi uninterracted cycles, with irrational periodic ratio.
* Strange attractor, sensitivity of initial conditions; may be of very low dimensionality, often non integer. Average of dimensionality of many points on it. Different dimensionality at different point?
* parameter, attractor portrait of the dynamical system. fiburcation: dramiatic change of attractors despite gradual change of parameters.
    * 涡流; 对流单体
* bifurcation, 分岔
* structurally stable: limited bifurcations versus frequent bifurcations; ruggedness of landscape. Mediate landscape ruggedness might be optimized for evovalibity, which corresponds to boundaries between order and chaos

**NK Boolean network**

