# Train a Deep Learning Model With PyTorch

An interactive beginner-friendly project that trains a fully connected neural network on MNIST handwritten digits using PyTorch.

## Quick Navigation

- [Project Snapshot](#project-snapshot)
- [Architecture](#architecture)
- [Interactive Run Guide](#interactive-run-guide)
- [Expected Outputs](#expected-outputs)
- [Project Structure](#project-structure)
- [Troubleshooting](#troubleshooting)
- [Next Improvements](#next-improvements)

## Project Snapshot

| Item      | Value                                         |
| --------- | --------------------------------------------- |
| Task      | Multi-class image classification (digits 0-9) |
| Dataset   | MNIST (60,000 train + 10,000 test)            |
| Model     | 2-layer fully connected neural network        |
| Framework | PyTorch + torchvision                         |
| Optimizer | Adam (learning rate 0.001)                    |
| Loss      | CrossEntropyLoss                              |
| Epochs    | 5                                             |

Use this checklist while running the notebook:

- [ ] Environment is ready
- [ ] Notebook runs without import errors
- [ ] Training loss decreases
- [ ] Test accuracy is printed

## Architecture

Input image shape is 28 x 28, flattened to 784 features.

```text
784 (input) -> Linear(784, 128) -> ReLU -> Linear(128, 10)
```

## Interactive Run Guide

### 1) Setup environment

```bash
python -m venv .venv
.venv\Scripts\activate
pip install torch torchvision matplotlib notebook
```

### 2) Launch notebook

```bash
jupyter notebook
```

Open and run:

- [Train_a_Deep_Learning_Model_With_Pytorch.ipynb](Train_a_Deep_Learning_Model_With_Pytorch.ipynb)

### 3) Follow this execution flow

<details>
<summary>Expand notebook flow</summary>

1. Import libraries (torch, torchvision, matplotlib).
2. Create transforms with tensor conversion and normalization.
3. Load MNIST train and test datasets.
4. Build the SimpleNN model.
5. Define loss and optimizer.
6. Train for 5 epochs and print running loss.
7. Plot training loss curve.
8. Evaluate on test set and print accuracy.

</details>

### 4) Runtime checks

<details>
<summary>Expand quick checks during training</summary>

- Loss logs should appear every 100 mini-batches.
- Average loss should generally trend downward over time.
- Final accuracy message should print after evaluation.

</details>

## Expected Outputs

You should see:

1. Training progress logs per epoch.
2. A training loss curve plot.
3. Final line similar to:

```text
Accuracy of the model on the 10000 test images: XX.XX%
```

## Project Structure

```text
.
|-- README.md
|-- Train_a_Deep_Learning_Model_With_Pytorch.ipynb
`-- data/
	`-- MNIST/
		`-- raw/
			|-- train-images-idx3-ubyte
			|-- train-labels-idx1-ubyte
			|-- t10k-images-idx3-ubyte
			`-- t10k-labels-idx1-ubyte
```

Reference paths:

- [README.md](README.md)
- [Train_a_Deep_Learning_Model_With_Pytorch.ipynb](Train_a_Deep_Learning_Model_With_Pytorch.ipynb)
- [data/MNIST/raw](data/MNIST/raw)

## Troubleshooting

<details>
<summary>Import errors (torch, torchvision, matplotlib)</summary>

Install missing dependencies:

```bash
pip install torch torchvision matplotlib
```

</details>

<details>
<summary>Kernel mismatch in notebook</summary>

Select the same Python interpreter where packages were installed.

</details>

<details>
<summary>No GPU detected</summary>

The notebook already falls back to CPU if CUDA is unavailable.

</details>

## Next Improvements

- Save model weights after training.
- Add validation loss tracking each epoch.
- Add confusion matrix and per-class accuracy.
- Replace SimpleNN with a small CNN for stronger performance.

## License

This project currently has no explicit license file.
