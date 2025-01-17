---
sidebar_position: 1
---

# Overview

Environments in `dojo` are representations of different DeFi protocols agents can interact with.
We currently support [UniswapV3 🦄](./UniswapV3) and are working hard to launch [AAVE 👻](https://twitter.com/EDuijnstee/status/1709877207047266657) support soon.

## ⛏️ Purpose
Environments generally provide the following functionality: 
1. ⏯️ Move the simulation forward in time to the next block at every simulation step
2. 🔎 Emit observations to provide the agent with the necessary information about the environment’s current state (based on the agent’s actions)
3. 🥇 Emit rewards generated by the agent to evaluate the agent’s actions
4. 🏋️ Accept a list of actions and execute the action in the environment.
Each environment module contains information on the observations, actions and environment object for that environment. For example, to get this information for UniswapV3: 

```python
from dojo.environments.uniswapV3 import UniV3Obs, UniV3Env
```

:::info
We are working on incorporating more complicated market impact models. Right now, the simulation simply replays the historic transactions.
:::
