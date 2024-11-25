# Searching for a policy

We start with a difference between **Learning and Planning**: in a learning process, environment is unknown, agents interact with the environment, agent improves its policy (kind of trial and error). In a planning phase a model of the environment is known.

A **policy** is something that determines the action the agent should take in each state.
A **deterministic policy**: maps each state to a specific action with a probability: $$
\pi(s)=a
$$A **Stochastic policy**: maps each state to a probability distribution over actions:
$$
\pi(a|s)=P[A_{t}=a| S_{t}=s]
$$
When working with "best policy" we need to focus on our objectives: most common case is **handling worst-case scenario**, i.e. minimizing the potential losses or worst-case outcomes (example, Natural Disaster).
A different objective is the **maximization of returns**: portfolio management for example could be an application. It's also what we do when doing reinforced learning.
A trade-off between this approaches is **robust optimization**, suitable for a range of scenarios.

# Reinforcement learning

A RL model is composed of two main entities: **agent and environment**. An agent perform an **action** that changes the environment. then it provides a **reward** and a change of **state**.
We are working in a **discrete scenario**.

![[Pasted image 20241125124025.png]]
In this context, the problem characteristics are:
- **Sequential**: solution is a sequence of steps
- **Discrete**: the alternative actions can be enumerated

The **goal** is to **maximize the expected cumulative reward**. The agent is rewarded for its actions: the reward could be sparse, uncertain or delayed.

More formally, at each step:
1. The agent receives a representation of the state $s$
2. The agent decides an action $a$
3. The agent receives a reward based on a **reward function** $f_{r}$

The **State is a function of the history**:
$$
f(H_{t})=S_{t+1}
$$
The environment state $S_{T}^E$ is the true state, but it might be not fully observable or contain irrelevant information.

A **State is Markov** if:
$$
P[S_{t+1}|S_{t}]=P[S_{t+1}|S_{0},S_{1},S_{2}\dots S_{t}]
$$
i.e. the future is **independent from the past, given the present**.
