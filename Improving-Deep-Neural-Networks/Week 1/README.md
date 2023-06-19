# **Practical aspects of Deep Learning**

## <span style="color: green;">**Congratulations! You passed!**</span>

### **Grade received** <span style="color: green;">80%</span>

### **Latest Submission Grade** 80%

### **To pass** 80% or higher

---

1. If you have 10,000 examples, how would you split the train/dev/test set? Choose the best option.
✔️
   - [ ] 60% train. 20% dev. 20% test.
   - [ ] 33% train. 33% dev. 33% test.
   - [x] 98% train. 1% dev. 1% test.
    > ✖️ <span style="color: red;">**Incorrect**</br>No. This might be considered a small data set, not in the range of big data. Thus a more classical (old) best practice should be used.</span>

---

2. The dev and the test set should be:

    - [ ] Come from different distributions.
    - [ ] Have the same number of examples.
    - [x] Come from the same distribution.
    - [ ] Be identical to each other (same (x,y) pairs).
    > ✔️ <span style="color: green;">**Correct**</span>

---

3. If your Neural Network model seems to have high bias, what of the following would be promising things to try? (Check all that apply.)

    - [ ] Add regularization.
    - [x] Make the Neural Network deeper.
    - [x] Increase the number of units in each hidden layers.
    - [ ] Get more training data.
    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

4. Working on a model to classify bananas and oranges your classifier gets a training set error of 0.1% and a dev set error of 11%. Which of the following two are true?

    - [x] The model has a high variance.
    - [ ] The model is overfitting the dev set.
    - [x] The model is overfitting the train set.
    - [ ] The model has a very high bias.
    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

5. In every case it is a good practice to use dropout when training a deep neural network because it can help to prevent overfitting. True/False?

    - [x] True
    - [ ] False
    > ✖️ <spane style="color: red;">**Incorrect**</br>Incorrect. In most cases, it is recommended to not use dropout if there is no overfit. Although in computer vision, due to the nature of the data, it is the default practice.</span>

---

6. What happens when you increase the regularization hyperparameter lambda?

    - [ ] Gradient descent taking bigger steps with each iteration (proportional to lambda)
    - [x] Weights are pushed toward becoming smaller (closer to 0)
    - [ ] Weights are pushed toward becoming bigger (further from 0)
    - [ ] Doubling lambda should roughly result in doubling the weights
    > ✔️ <spane style="color: green;">**Correct**</span>

---

7. Which of the following are true about dropout? 

    - [ ] It helps to reduce the bias of the model.
    - [ ] In practice, it eliminates units of each layer with a probability of keep_prob.
    - [x] It helps to reduce overfitting.
    - [x] In practice, it eliminates units of each layer with a probability of 1- keep_prob.
    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

8. During training a deep neural network that uses the tanh activation function, the value of the gradients is practically zero. Which of the following is most likely to help the vanishing gradient problem?

    - [ ] Use a larger regularization parameter.
    - [x] Use Xavier initialization.
    - [ ] Increase the number of cycles during the training.
    - [ ] Increase the number of layers of the network.
    > ✔️ <spane style="color: green;">**Correct**</br>Correct. A careful initialization can help reduce the vanishing gradient problem.</span>

---

9. Which of these techniques are useful for reducing variance (reducing overfitting)? (Check all that apply.)

    - [ ] Gradient Checking
    - [ ] Xavier initialization
    - [ ] Exploding gradient
    - [x] Data augmentation
    - [x] Dropout
    - [ ] Vanishing gradient
    - [x] L2 regularization
    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

10. Suppose that a model uses, as one feature, the total number of kilometers walked by a person during a year, and another feature is the height of the person in meters. What is the most likely effect of normalization of the input data?

    - [x] It will make the training faster.
    - [ ] It will make the data easier to visualize.
    - [ ] It will increase the variance of the model.
    - [ ] It won't have any positive or negative effects.
    > ✔️ <spane style="color: green;">**Correct**</br>Correct. Since the difference between the ranges of the features is very different, this will likely cause the process of gradient descent to oscillate, making the optimization process longer.</span>
