# Learn_Reinforcement_Learning

It's the Python code for the course Mathematical Foundation of Reinforcement Learning by Shiyu Zhao. 

You can find the book and relevant resources from https://github.com/MathFoundationRL/Book-Mathematical-Foundation-of-Reinforcement-Learning/tree/main

| 算法/模型 (Algorithm/Model) | 目标 (Target) | 具体方法 (Methods) | 更新策略方法 (Update Policy Method) | 使用的迭代方法 (Iteration Methods Used) | Estimate state-value/action-value for current-state[1] | Estimate next-state value | on-policy/off-policy |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Value Iteration / Policy Iteration** | Maximum all state-value | Policy determined, calculate state-value, update policy | Choose max action-value | Bellman equation, iterations | No | Use new state value table | :--- |
| **MC Basic / Exploring Starts** | Maximum all state-value | Policy determined, calculate state-value, update policy | ε-greedy | Calculate mean value, no iteration | Monte Carlo (use episode) | Non't need | on-policy |
| **MC ε-greedy** | Maximum all state-value | Policy determined, calculate state-value, update policy | ε-greedy | Calculate mean value, no iteration | By Monte Carlo (use episode) | Don't need | on-policy |
| **Sarsa / Expected Sarsa** | Maximum all state-value | Policy determined, calculate state-value, update policy | ε-greedy | RM | By Bellman Equation | Use the next sampled q(s, a) / E[q(s, a)] | on-policy |
| **n-step Sarsa** | Maximum all state-value | Policy determined, calculate state-value, update policy | ε-greedy | RM | By Bellman Equation | Use the several following sampled return and the last state-value | on-policy |
| **Q - learning** | Maximum all state-value | Calculate state-value and update policy | Choose max action-value | RM | By Opyimal Bellman Equation | Use the max q(s, a) in the q-value table in current iteration for next state | off-policy[2] |
---
**Footnotes:**

[1] 'Estimate state-value' means the state-value in the target function. For RM, it converts sampled **r** to sampled state-value through MC/ or approximate r to action-value through the Bellman Equation.
[2] Can be on-policy, using ε-greedy to update policy.
