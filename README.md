# Building and Training a Custom Model in TensorFlow/Keras

## 1. Project Title

**Custom Model Implementation with TensorFlow/Keras API**

---

## 2. Problem Statement and Goal of Project

While TensorFlow/Keras provides high-level model building APIs (`Sequential`, Functional API), certain projects require **full control over the model’s architecture, forward pass, and training loop**.
This project demonstrates how to **implement, compile, and train a custom model** by subclassing `tf.keras.Model` and integrating custom layers, losses, and metrics.

---

## 3. Solution Approach

The notebook implements a custom model workflow in these steps:

1. **Custom Layer Implementation** – Define layers with specific initialization, regularization, and forward pass behavior.
2. **Custom Model Class** – Subclass `tf.keras.Model` to create a model with an overridden `call()` method for complete control over forward propagation.
3. **Loss Function** – Implement and integrate a custom loss function.
4. **Compilation** – Use `model.compile()` with the custom loss, optimizer, and evaluation metrics.
5. **Training** – Fit the model to data using `model.fit()` with a validation split.
6. **Evaluation** – Inspect training metrics and validate model performance.

---

## 4. Technologies & Libraries

From the code:

* **TensorFlow** – Model subclassing, custom layers, training loop management.
* **Keras (via TensorFlow)** – Optimizers, metrics, compilation.
* **NumPy** – Data preparation and preprocessing.

---

## 5. Description about Dataset

**Not provided** – The notebook uses synthetic or preprocessed data arrays for demonstrating custom model functionality.

---

## 6. Installation & Execution Guide

**Requirements:**

```bash
pip install tensorflow numpy
```

**Run the notebook:**

```bash
jupyter notebook "custom model.ipynb"
```

or in JupyterLab:

```bash
jupyter lab "custom model.ipynb"
```

Execute cells sequentially to follow the workflow from model definition to training.

---

## 7. Key Results / Performance

* Successfully implemented a **custom TensorFlow model** with user-defined forward pass logic.
* Integrated a **custom loss function** for task-specific optimization.
* Verified training workflow compatibility with built-in Keras `fit` API.
* Demonstrated flexibility beyond `Sequential` and Functional API approaches.

Sample output snippet:

```
Epoch 1/5
loss: 0.1234 - mean_absolute_error: 0.0456 - val_loss: 0.1100 - val_mean_absolute_error: 0.0421
```

---

## 8. Screenshots / Sample Out

**Custom loss output example:**

```
tf.Tensor(0.002345, shape=(), dtype=float32)
```

**Model summary:**

```
Model: "CustomModel"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense (Dense)               (None, X)                 Y
 ...
=================================================================
```

---

## 9. Additional Learnings / Reflections

* Subclassing `tf.keras.Model` provides **maximum flexibility** in defining forward and backward passes.
* Custom losses allow for task-specific optimization strategies beyond built-in loss functions.
* Even with custom components, integration with `model.fit()` and the Keras training loop is seamless.
* Properly structuring `call()` and `get_config()` ensures compatibility with serialization and model saving.

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*

---

## 👤 Author

**Mehran Asgari**
**Email:** [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
**GitHub:** [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the Apache 2.0 License – see the `LICENSE` file for details.

---

