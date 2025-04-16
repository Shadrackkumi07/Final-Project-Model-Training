# 🧠 ARTIFICIAL BRILLIANCE MODEL

> 🎮 **Deep Reinforcement Learning for Boss Fights in Dark Souls III**

This project explores the use of Deep Reinforcement Learning (RL) to train an intelligent agent capable of surviving and defeating bosses in **Dark Souls III**, leveraging **real-time memory manipulation** via Cheat Engine.

Using **Gymnasium** as the RL environment, combined with **Stable-Baselines3 (PPO)** and **PyTorch**, the model interacts with the live game by reading and injecting data directly into memory — making gameplay fully agent-controllable.

---

## 🔍 Project Highlights

- 🔁 **Custom Gym-Compatible Environment** built on real-time game memory via Cheat Engine.
- 📊 **Memory-based Observations**: HP, stamina, position, and more extracted live.
- 🎮 **Action Injection**: Agent performs moves (attack, dodge, roll) by writing into game memory.
- 🎯 **Reward System**: Optimized for survival, damage dealt, and effective dodging.
- 🤖 **Training via PPO**: Proximal Policy Optimization from Stable-Baselines3.

---

## 📁 Directory Structure

```
FP-Machine-Learning-main/
│
├── Code/                        # Lua and Python scripts for control
│   ├── control_ds3_ml.py        # ML agent <-> game interface
│   ├── game_manager.py          # Orchestrates game logic
│   ├── coordinate_converter.py  # Maps memory to coordinates
│   └── *.lua                    # Cheat Engine automation scripts
│
├── dark_souls_api_bk_1.py       # Game API for training setup
├── gym_wrapper_bk_1.py          # Custom Gym wrapper for DS3
├── train_bk_1.py                # PPO training script
├── train_test.py                # Evaluation/test script
├── DS3_Table_V1.CT              # Cheat Engine memory pointer table
├── Mem_Adresses.txt             # Notes on memory offsets
└── requirements.txt             # Python dependencies
```

---

## 🚀 How It Works

1. Start **Dark Souls III** with the Cheat Engine `.CT` table loaded.
2. Launch `train_bk_1.py` to initialize training.
3. The agent:
   - 🔍 Observes the game state from memory.
   - 🧠 Chooses an action (e.g., dodge, attack).
   - ✍️ Injects it into the game memory.
   - 🎁 Receives reward based on performance and adjusts behavior.

---

## 🧪 Training Details

| Item              | Description                           |
|-------------------|---------------------------------------|
| **Model**         | PPO (Proximal Policy Optimization)    |
| **Frameworks**    | PyTorch, Stable-Baselines3, Gymnasium |
| **GPU Support**   | ✅ Tested on NVIDIA RTX 3080           |
| **Reward Shaping**| + Damage dealt, - Getting hit/dying   |
| **Key Hyperparams**| LR: `2e-4`, Entropy Coef: `0.01`     |

---

## 📦 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

You'll also need:

- ✅ Steam version of **Dark Souls III**
- ✅ **Cheat Engine 7.5+**
- ✅ Enable script execution in Cheat Engine settings

---

## 📈 Results

After training:

- 🕹️ Agent learned dodge timing, spacing, and stamina management
- ⚔️ Performance improved steadily across episodes
- 📉 Reward graphs show consistent learning and adaptation

---

## 🔗 Project Link

Check out the full project here:  
👉 [**GitHub Repo**](https://github.com/Shadrackkumi07/Final-Project-Model-Training)

---
