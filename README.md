# Learn_Reinforcement_Learning

It's the Python code for the course Mathematical Foundation of Reinforcement Learning by Shiyu Zhao.
You can fing the bood and relavent resourses from https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning/tree/main

| 算法/模型 (Algorithm/Model) | 目标 (Target) | 价值函数 (Value Function) | 更新时机 (Update Timing) | 更新依赖方法 (Update Dependency Method) | 生成经验的方式 (Experience Generation Method) | 不依赖于State-value/Action-value? | 选择了下一个状态后用state-value还是action-value | on-policy/off-policy[6] |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **MC Basic / Exploring Starts** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | 见完整序列后 | 见完整序列后 | 从完整序列中任意一个状态开始，不要求贪婪 | 无 | 使用该状态对应的state-value | on-policy |
| **MC ε-greedy** | 按照所有state-value最大 | 价值函数与state-value一样,求期望 | ε-greedy | 在每个状态开始的序列，不要求贪婪 | 其它episode会用到 | 不需要 | on-policy |
---
