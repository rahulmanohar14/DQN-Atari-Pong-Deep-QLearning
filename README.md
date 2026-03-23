# Deep Q-Learning with Atari Pong

A Deep Q-Learning agent that learns to play Atari Pong from raw pixel inputs, built with PyTorch and Gymnasium.

## Results

- Agent progresses from -21 (losing every point) to +12.4 average evaluation reward (winning consistently)
- Trained for 500 episodes (963,799 total steps) on Google Colab T4 GPU
- Four ablation studies comparing learning rate, discount factor, exploration strategy, and decay rate

## Architecture

- **Input:** 4 stacked 84x84 grayscale frames
- **Network:** 3 convolutional layers + 2 fully connected layers (1.7M parameters)
- **Algorithm:** DQN with experience replay and target network

## Ablation Results

| Experiment | Avg50 at Ep 150 |
|---|---|
| Baseline (lr=1e-4, gamma=0.99) | -18.40 |
| High LR (lr=5e-4) | -20.48 |
| Low Gamma (gamma=0.90) | -18.62 |
| Boltzmann (tau=1.0) | -19.80 |
| Fast Decay (decay=0.99) | -17.02 |

## Tech Stack

- Python 3.12
- PyTorch 2.10
- Gymnasium (Atari)
- NumPy, Matplotlib, OpenCV

## How to Run

1. Open the notebook in Google Colab
2. Set runtime to T4 GPU
3. Run all cells (training takes ~2 hours)

## Demo Video

[Video Walkthrough](https://drive.google.com/file/d/1rcibNjiKCj8j2L9qCs5FrxiZ2UN8vKcM/view?usp=sharing)

## Author

Rahul Manohar - MS in Information Systems, Northeastern University

## License

MIT License
