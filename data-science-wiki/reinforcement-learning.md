
Created by @jl33-ai 👦🏻

---

Reinforcement Learning (RL) is an aspect of machine learning where an agent learns to behave in an environment, by performing actions and seeing the results. 

In reinforcement learning, an **agent** learns by interacting with its **environment** to achieve a goal. 

The objective is to learn the optimal policy by optimizing the cumulative reward.

## Table of Contents

1. What is Reinforcement Learning
2. Elements of Reinforcement Learning
3. Types of Reinforcement Learning
4. Q-Learning 
5. Pros and Cons of Reinforcement Learning
6. Applications of Reinforcement Learning

---

## 🚀 What is Reinforcement Learning

- It is a type of Machine Learning, which is also a subtype of Artificial Intelligence.
- It enables machines and software agents to automatically determine the ideal behavior within a specific context, in order to maximize its performance. This is achieved by feedback in terms of rewards and punishments.
- The machine or the agent learns from the consequences of its actions, rather than from being taught explicitly. 
- It is inspired by behaviourist psychology.

---
## 🌐 Elements of Reinforcement Learning

- Agent: An entity that learns from trial and error.
- Environment: World/state through which the agent interacts and learns.
- Actions: Steps taken by the agent in the environment.
- Rewards: Feedback returned after the agent has taken an action.

---
## 💡 Types of Reinforcement Learning

- Positive Reinforcement: Strengthens actions which lead to reward.
- Negative Reinforcement: Strengthens actions that allow avoiding a negative condition.
- Policy Search: Agent uses trial and error to find the best policy.

---
## 👓 Q-Learning 

Q-learning is one of the simplest reinforcement learning algorithms. Representing an action in Q-table and used to find the best action for each state. 

Example:
```python
def update(self, state, action, reward, next_state):
    max_future_q = np.max(self.q_table[next_state])
    current_q = self.q_table[state][action]

    # formula to calculate the new Q-value for the given state and action pair
    new_q = (1 - self.lr) * current_q + self.lr * (reward + self.discount * max_future_q)

    # update the q_table with the new Q-value
    self.q_table[state][action] = new_q
```

---
## ✅ Pros and Cons of Reinforcement Learning

### Pros:

- No need for a large amount of data: They only need rewards and punishments as feedback.
- Trial and error learning: This is the most human-like learning.

### Cons:
  
- Computationally expensive: Large number of possible actions and states is the challenge. 
- Real world applications: It is not generally safe or sane to deploy a trial-and-error learning algorithm into a real-world scenario.

---
## 🌍 Applications of Reinforcement Learning

- Game AI
- Power Systems
- Robotics
- Production & Manufacturing
- Supply Chain
- Traffic Light Control
- Digital Marketing

---
<sup>For more details and context, refer to <a href="https://en.wikipedia.org/wiki/Reinforcement_learning">Wikipedia - Reinforcement Learning</a> </sup>.
