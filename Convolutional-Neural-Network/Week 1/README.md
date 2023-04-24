# **Introduction to Deep Learning**

## <span style="color: green;">**Congratulations! You passed!**</span>

### **Grade received** <span style="color: green;">90%</span>

### **Latest Submission Grade** 90%

### **To pass** 80% or higher

---

1. What do you think applying this filter to a grayscale image will do?

    $\begin{bmatrix}
        0 & 1 & 1 & 0 \\
        1 & 3 & 3 & 1 \\
        -1 & -3 & -3 & -1 \\
        0 & -1 & -1 & 0
    \end{bmatrix}$

   - [ ] Detect 45-degree edges.
   - [ ] Detect vertical edges.
   - [x] Detect horizontal edges.
   - [ ] Detecting image contrast.

    > ✔️ <span style="color: green;">**Correct**</br>Correct. There is a high difference between the values in the top part from those in the bottom part of the matrix. When convolving this filter on a grayscale image, the horizontal edges will be detected.</span>

---

2. Suppose your input is a 128 by 128 grayscale image, and you are not using a convolutional network. If the first hidden layer has 256 neurons, each one fully connected to the input, how many parameters does this hidden layer have (including the bias parameters)?

    - [ ] 4194304
    - [x] 4194560
    - [ ] 12583168
    - [ ] 12582912

    > ✔️ <span style="color: green;">**Correct**</br>Correct, the number of inputs for each unit is $128 \times 128$ since the input image is grayscale, so we need $128 \times 128 \times 256$ parameters for the weights and $256$ parameters for the bias thus $128 \times 128 \times 256 + 256 = 4194560$.</span>

---

3. Suppose your input is a 256 by 256 grayscale image, and you use a convolutional layer with 128 filters that are each $3 \times 3$. How many parameters does this hidden layer have (including the bias parameters)?

    - [ ] 1152
    - [ ] 3584
    - [x] 1280
    - [ ] 75497600

    > ✔️ <spane style="color: green;">**Correct**</br>Yes, since the input volume has only one channel each filter has $3 \times 3 + 1$ weights including the bias, thus the total is $(3 \times 3 + 1) \times 128$.</span>

---

4. You have an input volume that is $127 \times 127 \times 16$, and convolve it with 32 filters of $5 \times 5$, using a stride of 2 and no padding. What is the output volume?

    - [ ] $62 \times 62 \times 16$
    - [ ] $123 \times 123 \times 16$
    - [x] $62 \times 62 \times 32$
    - [ ] $123 \times 123 \times 32$

    > ✔️ <span style="color: green;">**Correct**</br>Correct, using the formula $n^{l}_{H} = \frac{n^{[l-1]}_{H}+2\times p-f}{s}+1$ with $n^{[l-1]}_{H} = 127, p = 0, f = 5$, and $s = 2$ we get $62$.</span>

---

5. You have an input volume that is 15x15x8, and pad it using “pad=2”. What is the dimension of the resulting volume (after padding)?

    - [ ] 19x19x12
    - [x] 19x19x8
    - [ ] 17x17x10
    - [ ] 17x17x8

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, padding is applied over the height and the width of the input image. If the padding is two, you add 4 to the height dimension and 4 to the width dimension.</span>

---

6. You have a volume that is $64 \times 64 \times 32$, and convolve it with 40 filters of $9 \times 9$, and stride 1. You want to use a "same" convolution. What is the padding?

    - [ ] 0
    - [x] 4
    - [ ] 6
    - [ ] 8

    > ✔️ <spane style="color: green;">**Correct**</br>Correct
Yes, when using a padding of 4 the output volume has $n_{H} = \frac{121-9+2\times 4}{1}+1$</span>

---

7. You have an input volume that is 128x128x12, and apply max pooling with a stride of 4 and a filter size of 4. What is the output volume?

    - [ ] $64 \times 64 \times 12$
    - [ ] $128 \times 128 \times 3$
    - [x] $32 \times 32 \times 12$
    - [ ] $32 \times 32 \times 3$

    > ✔️ <spane style="color: green;">**Correct**</br>Yes, using the formula $n^{l}_{H} = \frac{n^{[l-1]}_{H}+2\times p-f}{s}+1$ with $p = 0, f = 4, s = 4$ and $n^{[l-1]}_{H} = 32$</span>

---

8. Which of the following are hyperparameters of the pooling layers? (Choose all that apply)

    - [ ] Average weights.
    - [x] Filter size.
    - [x] Whether it is max or average.
    - [ ] Number of filters.

    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

9. In lecture we talked about “parameter sharing” as a benefit of using convolutional networks. Which of the following statements about parameter sharing in ConvNets are true? (Check all that apply)

    - [ ] It allows parameters learned for one task to be shared even for a different task (transfer learning).
    - [x] It allows a feature detector to be used in multiple locations throughout the whole input image/input volume.
    - [ ] It allows gradient descent to set many of the parameters to zero, thus making the connections sparse.
    - [x] It reduces the total number of parameters, thus reducing overfitting.

    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

10. The sparsity of connections and weight sharing are mechanisms that allow us to use fewer parameters in a convolutional layer making it possible to train a network with smaller training sets. True/False?

    - [x] False
    - [ ] True

    > ✖️ <span style="color: red;">**Incorrect**.</br>No, weight sharing reduces significantly the number of parameters in a neural network, and sparsity of connections allows us to use a smaller number of inputs thus reducing even further the number of parameters.</span>
