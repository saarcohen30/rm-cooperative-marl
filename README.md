# Reproducibility of Results: Reward Machines for Cooperative Multi-Agent Reinforcement Learning
The code attached to this repository reproduces the following paper, which studies reward machines for multi-agent q-learning of temporally extended cooperative tasks:

**Cyrus Neary, Zhe Xu, Bo Wu, and Ufuk Topcu. Reward Machines for Cooperative Multi-Agent Reinforcement Learning, page 934–942. <em>International Foundation for Autonomous Agents and Multiagent Systems</em>, 2021.**

## Dependencies
DQPRM requires:
- Python 3.6
- numpy
- matplotlib

## Execution
For the sake of executing a single experiment, one should enter the \verb|run.py| Python file and set:
- `num_agents` (restricted to [2,10]) - Determines the number of agents, which the experiment comprises of.
- `experiment = 'rendezvous'` - For the execution of an experiment in the rendezvous domain. As mentioned earlier, the CQRM baseline is not executed for a rendezvous scenario which comprises of more than two agents.
- `experiment = 'buttons'` - For the execution of an experiment in the buttons domain. Note that the baselines executed in this scenario are restricted to DQPRM, IQL and h-IL. Further, this experiment solely allows a setup of three agents.
The `rendezvous_config.py` and `buttons_config.py` Python files specify the learning parameters and the parameters of rendezvous and buttons environments, respectively.

For execution on Colab, the following commands shall be performed in sequence:
- `!cp -r "drive/My Drive/rm-cooperative-marl" "rm-cooperative-marl/"` - For copying the code to the respective runtime.
- `!python rm-cooperative-marl/src/run.py` - For running the chosen task domain.
