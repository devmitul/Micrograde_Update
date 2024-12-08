# **Neural Networks and Backpropagation - Micrograd Upgrade**

🚀 **An upgraded implementation of neural networks and backpropagation inspired by [micrograd](https://github.com/karpathy/micrograd).**

---

## 🌟 **Overview**
This project is a hands-on exploration of the foundational concepts behind neural networks, focusing on implementing backpropagation from scratch. It's designed for both learning and practical experimentation, offering a customizable and extensible API.

Inspired by [Andrej Karpathy's micrograd](https://github.com/karpathy/micrograd), this upgraded version introduces advanced features and enhancements.

---

## 🔑 **Key Features**
- **Expanded Activation Functions**: Includes ReLU, LeakyReLU, Tanh, and others.
- **Loss Functions**: Implemented Mean Squared Error (MSE) and batch processing.
- **GPU Acceleration**: Optimized for GPU usage to handle larger datasets efficiently.
- **Multi-Layer Perceptron (MLP)**: Full implementation of a multi-layer neural network.
- **Gradient Visualization**: Enhanced computational graph visualization for debugging and learning.

---

## ⚙️ Setup and Installation

1️⃣ Clone the Repository

```bash
  git clone https://github.com/devmitul/ neural-networks-backpropagation-upgrade.git
  cd neural-networks-backpropagation-upgrade
```
2️⃣ Install Dependencies
Install the required Python packages:    
```bash
pip install -r requirements.txt
```
3️⃣ Run the Project
```bash
python src/mlp.py
```

## 🛠️ Usage

 **Define Inputs and Model**
 - Create inputs, weights, and biases:
```python
inputs = [Value(1.0), Value(2.0)]
weights = [
    [[Value(0.1), Value(0.2)], [Value(-0.3), Value(0.4)]],
    [[Value(0.5), Value(-0.6)], [Value(0.7), Value(0.8)]]
]
biases = [Value(0.1), Value(-0.2)]
```
**Forward Pass**
- Perform computations using the MLP model:
```python
outputs = forward_mlp(inputs, weights, biases)
```
**Backward Pass**
- Compute gradients via backpropagation
```python
outputs[0].backward()
```
**Visualize the Computation Graph**
- Render the computational Graph:
```python
dot = draw_dot(outputs[0])
dot.render("computation_graph", format="svg", cleanup=True)
```
## 🧪 Examples
**Mean Squared Error Loss**
- Compute the loss between predicted and target values:
```python
predicted = Value(2.5, label="predicted")
target = Value(3.0, label="target")
loss = mse_loss(predicted, target)
loss.backward()
```
**Mini-Batch Processing**
- Perform batch-wise computations:

```python
batch_outputs = forward_batch(inputs, weights, Value(0.5, label="bias"))
```

**GPU Acceleration**
- Enable GPU-based computations:

```python
x1 = ValueGPU(2.0, label="x1")
```

## 📊 Features

- **Learn Backpropagation:** Step-by-step gradient computations.
- **Customizable Layers:** Build networks with - custom configurations.
- **Scalable for Datasets:** Efficient batch processing and GPU support.

## 🙌 Acknowledgments
- A big thank you to [Andrej Karpathy](https://github.com/karpathy/micrograd) for the original [micrograd](https://github.com/karpathy/micrograd) project, which served as the foundation and inspiration for this implementation.

## 📝 License

- This project is open-source and available under the [MIT](https://choosealicense.com/licenses/mit/) License.

## Feedback
- I'd love to hear your thoughts! Feel free to open an issue or contact me for collaboration opportunities.
- If you have any feedback, please reach out to us at mitulnaliyadhara2000@gmail.com.

You can download [README.md](https://github.com/user-attachments/files/18053483/README.md) from here.
