# connect4game_RL
This research focuses on the application of reinforcement learning (RL) techniques to develop an AI agent capable of playing Connect-4 optimally. The study explores the use of Q-learning and Deep Q-Networks (DQN) to enable the agent to learn effective strategies through interaction with the game environment. The primary objective is to demonstrate adaptive and strategic gameplay through reinforcement learning methodologies. The challenges, implementation, and training optimizations are discussed to highlight the efficiency of RL in sequential decision-making games.
Keywords—Reinforcement Learning, Q-Learning, DQN, Connect-4, Artificial Intelligence, Deep Learning.
#  Connect4 Game with Reinforcement Learning

This project implements a **Connect4 game agent trained using Reinforcement Learning (RL)**. The agent learns how to play the classic board game by interacting with the environment, optimizing its moves over time using reward signals.

> 🎮 Connect4 is a two-player strategy game where the goal is to drop colored discs into a grid and connect four in a row — vertically, horizontally, or diagonally.

---

##  Features

- ✅ Classic **Connect4 board** (6 rows × 7 columns)
- 🧠 **RL Agent** trained via:
  - Q-Learning / Deep Q-Network (DQN)
- 🧪 Self-play or vs-rule-based opponent
- 🎯 Reward-driven decision making
- 📊 Visualized training performance and evaluation stats

---

##  Objective

- Train an RL agent to **play Connect4 optimally**
- Maximize winning rate over random or rule-based opponents
- Apply RL concepts such as:
  - Environment interaction
  - Policy learning
  - Q-table or Q-network updates
  - Exploration vs exploitation

---

##  Tools & Libraries

- Python 3.8+
- `numpy` – Matrix operations and logic
- `matplotlib` – Training performance graphs
- `gym` or `pygame` (optional) – Game visualization or environment wrapper
- `tensorflow` / `pytorch` (if DQN used)

Install required libraries:
bash
pip install numpy matplotlib

for DQN:  pip install torch  # or tensorflow

# overall structure
connect4-rl/
├── connect4_env.py              # Game environment logic
├── agent_qlearning.py           # Q-Learning agent implementation
├── agent_dqn.py                 # Deep Q-Network agent (optional)
├── train.py                     # Training loop and evaluation
├── visualize.py                 # Match replays or board visualization
├── README.md                    # Documentation (you’re here)
└── results/
    ├── rewards_plot.png
    └── agent_vs_random.txt


🎲 Game Rules (Connect4)
6 rows × 7 columns board

Players alternate turns

Drop tokens from the top of a column

Win by connecting four tokens in a row:

Horizontally

Vertically

Diagonally

🤖 Reinforcement Learning Design
🏗 Environment
State: Encoded 6x7 matrix of the board

Actions: Integer (0–6), representing the column to drop a token

Reward Function:

+1 for win

-1 for loss

0 for draw or invalid move

🧠 Agent (Q-Learning)
Maintains Q-table: Q[state][action]

Updates using Bellman Equation:

css
Copy
Edit
Q(s, a) ← Q(s, a) + α [r + γ max Q(s', a') - Q(s, a)]
Uses ε-greedy policy:

Explores random moves with probability ε

Exploits known best move otherwise

🧠 (Optional) Agent (DQN)
Neural network replaces Q-table

Input: flattened board state

Output: Q-values for each possible action

Trained via backpropagation and experience replay


# Train agent
python train.py

# Watch gameplay
python visualize.py
You can adjust hyperparameters (learning rate, discount factor, episodes) inside train.py.

📈 Sample Output
yaml
Copy
Edit
Training episode 5000/10000 - Win rate: 65.3%
Average Reward: 0.71

🚀 Possible Extensions
Implement Minimax opponent

Add GUI using PyGame

Transition to Policy Gradient or Actor-Critic methods

Train agent using self-play

🙌 Acknowledgements
Inspired by classic games research in reinforcement learning

Educational implementation of agent-environment interaction

Reward system modeled after OpenAI Gym principles

 References
Sutton & Barto – Reinforcement Learning: An Introduction

OpenAI Gym

DeepMind AlphaZero

🤖 Fun Fact
RL agents can learn to beat humans at Connect4 with just trial-and-error — no rules hardcoded!

# sample results
![image](https://github.com/user-attachments/assets/8b99e678-e652-4f93-8bfb-50cf9d3f368b)
![image](https://github.com/user-attachments/assets/fa900e96-c7f0-49ad-80d7-c7cff163180f)
![image](https://github.com/user-attachments/assets/d1e33d3f-f5a8-4392-b35d-a04c5547a6d7)
![image](https://github.com/user-attachments/assets/7853dca8-a9bc-4e78-b30a-62272c7a8a4b)
![image](https://github.com/user-attachments/assets/87dea410-cc98-4d96-a474-14954d6f5979)
![image](https://github.com/user-attachments/assets/b00fddd5-8599-446d-82a9-784ffd9f53a9)



