# Visualizing the State-Action Value Function – Mars Rover Example



This project explores how the **state-action value function** \$Q(s, a)\$ changes within a basic **Markov Decision Process (MDP)**, illustrated through a Mars Rover scenario.

The visualization highlights the impact of different parameters—such as **reward settings**, **discount factor (\$\gamma\$)**, and **misstep probability**—on Q-values for various states and actions.

---

## Key Ideas

* **Q(s, a):** Represents the expected return when taking action `a` in state `s` and continuing with the optimal policy.
* **Gamma (γ):** The discount factor that determines the weight of future rewards.
* **Misstep Probability:** The likelihood that the agent executes an unintended action due to uncertainty.


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
