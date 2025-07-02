# Learn_Reinforcement_Learning

It's the Python code for the course Mathematical Foundation of Reinforcement Learning by Shiyu Zhao.
You can fing the bood and relavent resourses from https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning/tree/main

| 算法/模型 (Algorithm/Model) | 目标 (Target) | 具体方法 (Methods) | 更新策略方法 (Update Policy Method) | 使用的迭代方法 (Iteration Methods Used) | State-value/Action-value on current_state | Estimate next_state value | on-policy/off-policy |
| **Value Iteration / Policy Iteration** | Maximum all state-value | Policy determined, calculate state_value, update policy | Choose max action_value | Bellman equation, iterations | No | Use new state value table | :--- |
| **MC Basic / Exploring Starts** | Maximum all state-value | Policy determined, calculate state_value, update policy | ε-greedy | Calculate mean value, no iteration | Monte Carlo (use episode) | Non't need | on-policy |
| **MC ε-greedy** | Maximum all state-value | Policy determined, calculate state_value, update policy | ε-greedy | Calculate mean value, no iteration | Monte Carlo (use episode) | Don't need | on-policy |
---
