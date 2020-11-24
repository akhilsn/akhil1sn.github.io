---
layout: project
type: project
image: images/airline1.jpg
title: Inventory Management with Reinforcement Learning
permalink: projects/info_extraction
# All dates must be YYYY-MM-DD format!
date: 2020-11-10
labels:
  - Reinforcement Learning
  - Deep Q-Learning

summary: Solve an inventory management problem using the Q-learning algorithm.
---

### Problem Statement:
A major concern of a warehouse owner is how much stock to order from the supplier to meet the customer demand and, at the same time, minimize the costs. The warehouse owner needs to learn the demand pattern and order accordingly. In this project, we using a RL agent who can continously learn the demand pattern by interacting with the environment, i.e. by placing orders, measuring the 'reward' (profit) and updating the policy, we will solve the inventory management issue by maximizinf 'rewards'.

### Approach:

Epsilon-greedy action is picked at every state. The initial epsilon-value is high as it is important to ensure that the agent explores enough. Then, epsilon decreases as the number of episodes increases. Then, it is necessary for the agent to exploit to converge to optimal policy and action-value function
There is a q-dict maintained which stores q-values for all state-action pairs visited.
<br><br>
After the action is decided, the rest is normal Q-learning update. To get the next state, the agent calls the step function from the environment, which returns a new state and reward. And from q-dict, the best action is picked for the new state. 
<br>
Q-values are updated in q-dict
 
I ran it for 15Mn episodes, with each episode of 30 days length (I used Paperspace for simulating the episodes, it takes about 12-13 hours to simulate about 15  million episodes).
