# 🤖 State-Action Value Function Visualization – Mars Rover Exp

## 📌 Project Overview

This project demonstrates how the **state-action value function** $Q(s, a)$ evolves in a simple **Markov Decision Process (MDP)** using a Mars Rover example.

We visualize how varying parameters like **reward values**, **discount factor ($\gamma$)**, and **misstep probability** affect the Q-values across different states and actions.

---

## 🧠 Core Concepts

* **Q(s, a):** Expected return of taking action `a` in state `s` and following an optimal policy thereafter.
* **Gamma (γ):** Discount factor that controls the importance of future rewards.
* **Misstep Probability:** Probability of the agent taking the wrong action due to uncertainty.

---

## ⚙️ Parameters

```python
num_states = 6               # Number of states in the grid
num_actions = 3              # Number of possible actions per state
terminal_left_reward = 100   # Reward for reaching the left terminal
terminal_right_reward = 40   # Reward for reaching the right terminal
each_step_reward = 0         # Reward for non-terminal steps
gamma = 0.5                  # Discount factor
misstep_prob = 0             # Probability of unintended action
```

---

## 📊 Example Code

```python
import numpy as np
from utils import *

# Parameters (modifiable)
terminal_left_reward = 100
terminal_right_reward = 40
each_step_reward = 0
gamma = 0.5
misstep_prob = 0

generate_visualization(
    terminal_left_reward, 
    terminal_right_reward, 
    each_step_reward, 
    gamma, 
    misstep_prob
)
```

---

## 🔍 What You’ll See

* A visual representation of the Mars Rover’s state space
* Arrows or heatmaps showing the value of Q(s, a) for each action
* Changes in behavior when:

  * Terminal rewards are adjusted
  * Discount factor is changed
  * Uncertainty (misstep probability) is introduced

---

## 📦 File Structure

```
.
├── mars_rover_q_example.py    # Main script
├── utils.py                   # Contains generate_visualization() and related helpers
├── README.md                  # This documentation
```

---

## ✅ Requirements

* Python 3.x
* NumPy
* Matplotlib (or any other visualization library used in `utils.py`)

Install using:

```bash
pip install numpy matplotlib
```

---

## 📚 References

* Sutton & Barto: "Reinforcement Learning: An Introduction"
* OpenAI Gym for MDP design inspiration

---

## 🧠 Further Exploration

* Add stochastic transitions with higher `misstep_prob`
* Try different reward structures
* Use other RL algorithms (e.g., SARSA, Q-Learning) to compare with visualization
