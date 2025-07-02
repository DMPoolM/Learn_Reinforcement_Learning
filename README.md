# Learn_Reinforcement_Learning

It's the Python code for the course Mathematical Foundation of Reinforcement Learning by Shiyu Zhao.
You can fing the bood and relavent resourses from https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning/tree/main

| 算法/模型 (Algorithm/Model) | 目标 (Target) | 价值函数 (Value Function) | 更新时机 (Update Timing) | 更新依赖方法 (Update Dependency Method) | 生成经验的方式 (Experience Generation Method) | 不依赖于State-value/Action-value? | 选择了下一个状态后用state-value还是action-value | on-policy/off-policy[6] |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **MC Basic / Exploring Starts** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | 见完整序列后 | 见完整序列后 | 从完整序列中任意一个状态开始，不要求贪婪 | 无 | 使用该状态对应的state-value | on-policy |
| **MC ε-greedy** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | ε-greedy | 在每个状态开始的序列，不要求贪婪 | 其它episode会用到 | 不需要 | on-policy |
| **TD** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | ε-greedy | N/A | 见每次交互 | 使用该状态对应的state-value | on-policy |
| **Sarsa** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | ε-greedy | N/A | 见每次交互 | 使用下一个状态对应的action-value | on-policy |
| **Expected Sarsa** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | ε-greedy | N/A | 见每次交互 | 使用下一个状态对应的所有action-value的期望 | on-policy |
| **Q-learning** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | 动态选择,最大化action-value | N/A | 见每次交互 | 使用下一个状态对应的最大action-value | off-policy[2] |
| **Sarsa with FFA** | 按照目标函数最大 | 价值函数与state-value一样,求期望 | ε-greedy | 与更新时机一致 | 见每次交互 | 使用下一个状态对应的action-value | on-policy |
| **Q-learning with FFA** | 按照目标函数最大 | 待定（不同于[3]的更新策略） | 动态选择,最大化action-value | 与更新时机一致 | 见每次交互 | 使用下一个状态对应的最大action-value | off-policy |
| **Deep Q-learning** | 按照目标函数最大 | 待定（不同于[3]的更新策略） | 动态选择,最大化action-value | 待定（不同于[3]的更新策略） | 见每次交互 | 使用下一个状态对应的最大action-value | off-policy |
| **DDPG** | 按照目标函数最大 | 计算策略 | 动态选择,最大化价值函数 | 见replay buffer | action-value和policy function都依赖 | 使用action-value function作为下一个状态的输入 | off-policy |
| **A2C** | 按照目标函数最大 | 计算策略 | 动态选择,最大化价值函数 | N/A | action-value和policy function都依赖, policy function的参数依赖action-value, action-value的参数也依赖policy | 使用state-value function来评价一次完整交互 | on-policy |
| **A3C** | 按照目标函数最大 | 计算策略 | 动态选择,最大化价值函数 | 在相应的线程梯度触发后上传，主线程目标函数触发后下载 | action-value和policy function都依赖, policy function的参数依赖action-value, action-value的参数也依赖policy | 使用state-value function来评价一次完整交互 | on-policy |
| **DPG** | 按照目标函数最大 | 计算策略 | 动态选择,最大化价值函数 | 见目标函数梯度触发后上传，主线程目标函数触发后下载 | action-value和policy function都依赖, policy function的参数依赖action-value, action-value的参数也依赖policy | 使用value function作为下一次的policy的输入 | off-policy |

---
**Footnotes:**

[1] 在这里的state-value指的是所有状态的目标函数中的state-value，对于特定于某个状态而言，就是计算所有可能路径的state-value。对于特定而言，可能取一个采样序列的state-value或者取期望。与是否贪婪策略有关。
[2] Q-learning选择的更新策略不一定是当前使用的策略(behavior policy)
[3] 更新策略指policy update, 而state-value/action-value的更新具体指value update
[4] on-policy指行为策略、及评估和改进的策略是同一个策略
[5] 不可以使用experience sampling
[6] off-policy指行为策略与评估、改进的策略不是同一个策略
[7] state-value既指代state-value，也指代state-value function, action-value既指代action, 也指代action-value function. 都是贪婪策略
