🖋 Handwritten Digit Recognition with ANN (Keras + MNIST)
📌 Project Overview
This project uses the famous MNIST dataset to train an Artificial Neural Network (ANN) that can recognize handwritten digits from 0 to 9.

Dataset Size: 70,000 grayscale images of handwritten digits
Image Size: 28 × 28 pixels
Training Data: 60,000 images
Testing Data: 10,000 images
Think of it like teaching a child to recognize numbers — first we show thousands of examples (training), then we test with new ones (testing) to see how well they learned.

🗂 Dataset
The MNIST dataset is built into Keras and can be loaded easily:

from tensorflow.keras.datasets import mnist
(X_train, y_train), (X_test, y_test) = mnist.load_data()
