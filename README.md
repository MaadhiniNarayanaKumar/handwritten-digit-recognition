# Handwritten digit recognition

A Keras notebook that loads MNIST, flattens each 28×28 digit, and trains a small dense network to ten classes.

## What it does

`handwritten-digit-recognition.ipynb` loads MNIST from `tensorflow.keras.datasets`. There are 60,000 training images and 10,000 test images.

- Pixels are divided by 255.
- Each image is reshaped from 28×28 to a vector of 784.
- Labels are one-hot encoded with `to_categorical`.
- The network is Dense 512 ReLU, Dense 64 ReLU, Dense 32 ReLU, Dense 10 softmax.
- Training uses Adam, categorical crossentropy, and accuracy for 100 epochs.

The saved run reports train accuracy about 0.998 and test accuracy 0.980. After `evaluate`, the notebook prints `argmax` of the first 100 test predictions next to the true labels.

## Run it

```bash
jupyter notebook handwritten-digit-recognition.ipynb
```

The first cell needs TensorFlow, Keras, scikit-learn, NumPy, and Matplotlib. MNIST downloads on the first `load_data()` call.

## Notes

The notebook does not save weights, and it has no drawing canvas. `StandardScaler` and `train_test_split` are imported and unused. MNIST already ships as a train and test split, so the notebook does not call `train_test_split`.

The project page is on the portfolio: [maadhiniportfolio.vercel.app/projects/handwritten-digit-recognition](https://maadhiniportfolio.vercel.app/projects/handwritten-digit-recognition).
