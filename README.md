# Multi-Layer Perceptrons Workshop – Group 1

CSCN8010 – Foundations of Machine Learning

| Group Member | Student ID |
|---|---|
| Sultan Akinola Atanda | 9114837 |
| John Buni | 9115726 |
| Echezona Oji | 9078881 |
| Antonio Sainz | 9072844 |

## About the Workshop

This workshop is about multi-layer perceptrons (MLPs). We classify handwritten digits from the MNIST dataset in two ways.

**Challenge 1 – Framework comparison.** We build the same network (784 → 128 → 64 → 10) in Keras, PyTorch and TensorFlow Core, and compare their speed and accuracy. We also test how batch size affects training time, and explain why each framework is fast or slow.

**Challenge 2 – Neural network from scratch.** We build the same network using only NumPy: forward propagation, cross-entropy loss, backpropagation and gradient descent. We then run experiments on the activation function, learning rate, depth and weight initialisation, and plot how activations and gradients flow through the layers.

The notebook ends each challenge with a reflection.

## Who Did What

| Member | Challenge 1 | Challenge 2 |
|---|---|---|
| Sultan | Talking points, reflection, merging | Setup (data, network, initialisation), reflection |
| John | Keras questions | Part 1 – Forward propagation |
| Eche | PyTorch questions | Part 2 – Backpropagation and training |
| Antonio | TensorFlow Core questions | Part 3 – Experiments and visualisations |

## Files

| File | Description |
|---|---|
| `MultiLayerPerceptrons_Workshop.ipynb` | The workshop notebook with both challenges |
| `requirements.txt` | Python packages needed to run the notebook |
| `data/` | MNIST files used by PyTorch (downloaded automatically if missing) |

## How to Run

1. Clone the repository and open the folder:
   ```bash
   git clone https://github.com/JohnBuni/MultiLayerPerceptrons_Workshop.git
   cd MultiLayerPerceptrons_Workshop
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate        # Windows
   source .venv/bin/activate     # macOS / Linux
   ```
3. Install the packages:
   ```bash
   pip install -r requirements.txt
   ```
4. Start Jupyter and open `MultiLayerPerceptrons_Workshop.ipynb`:
   ```bash
   jupyter notebook
   ```
5. Run all cells from top to bottom (**Kernel → Restart & Run All**). Challenge 2 uses the MNIST data loaded in Step 6, so run the cells in order.

MNIST downloads automatically the first time: Keras saves it to `~/.keras/datasets` and PyTorch saves it to `./data`. A full run takes about 15–20 minutes on a laptop CPU, most of it in Challenge 1.

## Results Summary

| Model (5 epochs) | Test accuracy |
|---|---|
| Keras | 97.22% |
| TensorFlow Core | 97.76% |
| PyTorch | 96.33% |
| NumPy from scratch | 97.55% |
