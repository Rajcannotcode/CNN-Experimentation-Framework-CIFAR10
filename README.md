# CNN-Experimentation-Framework-CIFAR10
An experimentation framework for testing model architectures and hyperparameters for the CIFAR-10 database


---

## Supported Components

| Component         | Description                                                   |
|-------------------|---------------------------------------------------------------|
| `CNNModel`        | Basic CNN with BatchNorm, ReLU, and Dropout layers            |
| `RunManager`      | Handles logging, state tracking, model saving per run         |
| `Network Factory` | Centralized factory-style logic to instantiate models by name |
| Experiment Loop   | Sweeps over model types, batch sizes, learning rates, etc.    |
| Safe Downloader   | Interactive cell to download selected models and clean disk   |

---

## How to Use

1. Open `CIFAR_10_experimentation.ipynb` in Google Colab.
2. Configure the `parameters` dictionary to define experiment settings.
3. Choose from dataset transformation types:
   - `normalized`
   - `augmented`
   - `heavily_augmented`
4. Run all cells to begin training.
5. After completion, use the interactive model download cell to:
   - Select trained runs to download
   - Rename output files
   - Safely delete model files from Colab to manage memory
6. Use the resulting `DataFrame` to compare performance across experiments.

---

The preffered environment is Google Colab

## Credits

This project is largely inspired by the [deeplizard YouTube channel](https://www.youtube.com/@deeplizard), which provides clear explanations and walkthroughs for CNN experimentation in PyTorch.

The CIFAR-10 adaptation and additional engineering work were completed independently to support extensibility, structured experimentation, and Google Colab compatibility.

---

