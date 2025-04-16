#ARTIFICIAL BRILLIANCE MODEL


🎮 Deep Reinforcement Learning for Boss Fights in Dark Souls III

This project explores the application of Reinforcement Learning (RL) to real-time gameplay by training an agent to survive and win boss fights in Dark Souls III using live game memory manipulation via Cheat Engine.

The training environment is built using Gymnasium, with models trained using Stable-Baselines3 (PPO) and PyTorch. Real-time data is extracted from the game through a Cheat Engine table, enabling observations and actions directly tied to gameplay.

---

🧠 Project Overview

Core Features:
- Custom Gym-compatible environment wrapping real-time game state via Cheat Engine
- RL agent receives memory-based observations: player HP, stamina, position, etc.
- Actions (e.g., dodge, attack) are injected into game memory
- Reward system shaped around combat effectiveness (damage dealt, survival, avoiding hits)
- Uses Proximal Policy Optimization (PPO) for training

---

🛠️ Directory Structure

FP-Machine-Learning-main/
│
├── Code/                     # Lua and Python scripts for in-game control
│   ├── control_ds3_ml.py     # ML-specific agent/game interfacing
│   ├── game_manager.py       # Game orchestration and control logic
│   ├── coordinate_converter.py  # Mapping coordinates from memory to grid
│   └── *.lua                 # Cheat Engine automation scripts
│
├── dark_souls_api_bk_1.py    # Game API used for training prep
├── gym_wrapper_bk_1.py       # Custom Gym wrapper for the DS3 environment
├── train_bk_1.py             # Main training script using PPO
├── train_test.py             # Testing and evaluation script
├── DS3_Table_V1.CT           # Cheat Engine table with memory pointers
├── Mem_Adresses.txt          # Notes on used memory addresses
└── requirements.txt          # Python dependencies

---

🚀 How It Works

1. Launch Dark Souls III with the provided .CT table loaded in Cheat Engine.
2. Run the training script to initialize the Gym environment.
3. The agent:
   - Reads real-time game data
   - Chooses an action (attack/dodge/move)
   - Injects the action back into the game
   - Receives reward signals and updates policy accordingly

---

🧪 Training Info

- Model: PPO (Proximal Policy Optimization)
- Frameworks: PyTorch, Stable-Baselines3, Gymnasium
- GPU Support: Yes (tested with NVIDIA RTX 3080)
- Reward Shaping:
  - + for damage dealt
  - - for being hit or dying
- Key Hyperparameters:
  - Learning rate: 2e-4
  - Entropy coefficient: encourages exploration
  - Episode length: matches boss fight duration

---

📦 Requirements

pip install -r requirements.txt

You'll also need:
- A Steam version of Dark Souls III
- Cheat Engine 7.5 or later
- Enable script execution in Cheat Engine

---

📂 Project Link

Explore the full code and implementation here:
👉 https://github.com/Shadrackkumi07/Final-Project-Model-Training

---

📈 Results

After multiple training runs, agents learned:
- Timing for dodging attacks
- Maintaining distance and stamina
- Dealing consistent damage and improving survivability

Reward curves and episode lengths show meaningful improvement across epochs.

---

📬 Contact

Feel free to reach out if you're interested in AI + gaming, reinforcement learning, or memory hacking for intelligent agents.
