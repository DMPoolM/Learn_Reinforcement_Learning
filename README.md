# Learn_Reinforcement_Learning

It's the Python code for the course Mathematical Foundation of Reinforcement Learning by Shiyu Zhao.
You can fing the bood and relavent resourses from https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning/tree/main

| 算法/模型 (Algorithm/Model) | 目标 (Target) | 价值函数 (Value Function) | 更新时机 (Update Timing) | 更新依赖方法 (Update Dependency Method) | 生成经验的方式 (Experience Generation Method) | Depends on State-value/Action-value? | Select state-value or action-value after selecting a next_state| on-policy/off-policy |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **MC Basic / Exploring Starts** | Maximum all state-value | Same as state-value, calculate E | After getting whole episode | After getting whole episode | 从完整序列中任意一个状态开始，不要求贪婪 | No | 使用该状态对应的state-value | on-policy |
| **MC ε-greedy** | Maximum all state-value | Same as state-value, calculate E | ε-greedy | 在每个状态开始的序列，不要求贪婪 | 其它episode会用到 | Don't need | on-policy |
---
