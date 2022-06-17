路上听了一小段TLA+: 通过代数方程描述(indefinite?)状态机. 感觉同函数式编程有些相通: 其中第二节的内容可以重述为: 给定一组方程和当前状态参数x, y, 求解下一状态参数x', y'使得至少一个方程成立, 则由x, y状态进入x', y'状态合法.

indifinite: 与FSM相比, x, y甚至不需要指定"进入下一状态"的方法, 只需要给定一个"判断任意状态是否为合法下一状态"的方法即可. post verification instead of pre instruction.

有趣的是, 视频里Lamport的讲述方式: 为了解释no next state的表达方式而突然思维跳跃地强调equal/assignment的区别; 用同样的力度讲述equation clase这样的重点和conjuction sign在ASCII源码中记为"/\"之类无关紧要的细节, 也颇契合TLA+这种"抹去时序, 一视同仁"的思维方式.

P.S. Lamport原来还是初代LaTeX的作者. Long live plain text!
