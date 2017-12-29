# Thirsty Scholar's Deep Thinking

This repo contains the following materials:
$$
\mathbb E_{q(\textbf{w}|\theta)} [\log p(\mathcal D | \textbf{w})]
$$


## Deep Deterministic Policy Gradient (DDPG)

A simple implementation of the *deep deterministic policy gradient* algorithm presented in [this paper](https://arxiv.org/pdf/1509.02971.pdf) on the classical [Pendulum task](https://github.com/openai/gym/wiki/Pendulum-v0) via [OpenAI Gym](https://gym.openai.com). The resulting learning curve is shown below.

![ddpg_pendulum_result](DDPG/ddpg_pendulum_result.png)

I also standardized the state input by keeping a running stat (taken from [John Schulman's repo](https://github.com/joschu/modular_rl/blob/master/modular_rl/running_stat.py)) and scale the reward signal into the range roughly between [-1, 0] by dividing it by 16.



## Proximal Policy Optimization (PPO)

A simple implementation of the single-threaded version of the *proximal policy optimization* algorithm with the clipped surrogate objective in [this paper](https://arxiv.org/abs/1707.06347) by OpenAI. The learning curve on the classical [CartPole](https://github.com/openai/gym/wiki/CartPole-v0) task is shown below.

![ppo_cartpole_result](PPO/ppo_cartpole_result.png)

I also standardized the state input by keeping a running stat (taken from [John Schulman's repo](https://github.com/joschu/modular_rl/blob/master/modular_rl/running_stat.py)) and slightly modified the reward function to make it more suitable for learning.