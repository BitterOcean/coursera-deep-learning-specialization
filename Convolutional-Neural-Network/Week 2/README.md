# **Deep Convolutional Models**

## <span style="color: green;">**Congratulations! You passed!**</span>

### **Grade received** <span style="color: green;">90%</span>

### **Latest Submission Grade** 90%

### **To pass** 80% or higher

---

1. Which of the following do you typically see in ConvNet? (Check all that apply.)

   - [ ] Multiple FC layers followed by a CONV layer.
   - [ ] ConvNet makes exclusive use of CONV layers.
   - [ ] Use of multiple POOL layers followed by a CONV layer.
   - [x] Use of FC layers after flattening the volume to output classes.

    > ✔️ <spane style="color: green;">**Correct**</br>Yes, FC layers are typically used in the last few layers after flattening the volume to generate the output in classification.</span>

---

2. In LeNet - 5 we can see that as we get into deeper networks the number of channels increases while the height and width of the volume decreases. True/False?

    - [ ] False
    - [x] True

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, since in its implementation only valid convolutions were used, without padding, the height and width of the volume were reduced at each convolution. These were also reduced by the POOL layers, whereas the number of channels was increased from 6 to 16.</span>

---

3. The motivation of Residual Networks is that very deep networks are so good at fitting complex functions that when training them we almost always overfit the training data. True/False?

    - [ ] True
    - [x] False

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, very deep neural networks are hard to train and a deeper network does not always imply lower training error. Residual Networks allow us to train very deep neural networks.</span>

---

4. The following equation captures the computation in a ResNet block. What goes into the two blanks above?

    $a^{[l+2]}=g(W^{[l+2]}g(W^{[l+1]}a^{[l]}+b^{[l+1]})+b^{[l+2]}+ \cdots)+\cdots$

    - [ ] 0 and $a^{[l+1]}$, respectively
    - [x] $a^{[l]}$ and 0, respectively
    - [ ] 0 and $a^{[l]}$, respectively
    - [ ] $z^{[l]}$ and $a^{[l]}$, respectively

    > ✔️ <span style="color: green;">**Correct**</br>Correct</span>

---

5. Adding a ResNet block to the end of a network makes it deeper. Which of the following is true?

    - [ ] The number of parameters will decrease due to the shortcut connections.
    - [ ] The performance of the networks is hurt since we make the network harder to train.
    - [ ] It shifts the behavior of the network to be more like the identity function.
    - [x] The performance of the networks doesn't get hurt since the ResNet block can easily approximate the identity function.

    > ✔️ <spane style="color: green;">**Correct**</br>Yes, as noted in the lectures in a ResNet block the computations are given by $a^{[l+2]}=g(W^{[l+2]}a^{[l+1]}+b^{[l+2]}+a^{[l]})$ thus if $W^{[l+2]}$ and $b^{[l+2]}$ are zero then we get the identity function.</span>

---

6. Suppose you have an input volume of dimension $n_{H}\times n_{W}\times n_{C}$. Which of the following statements do you agree with? (Assume that the “1x1 convolutional layer” below always uses a stride of 1 and no padding.)

    - [ ] You can use a 1x1 convolutional layer to reduce $n_{H}, n_{W}$, and $n_{C}$.
    - [x] You can use a 1x1 convolutional layer to reduce $n_{C}$ but not $n_{H}$ and $n_{W}$
    - [x] You can use a 2D pooling layer to reduce $n_{H}, n_{W}$, but not $n_{C}$.
    - [ ] You can use a 2D pooling layer to reduce $n_{H}, n_{W}$, and $n_{C}$.

    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

7. A demographic dataset with statistics on different cities' population, GDP per capita, and economic growth is an example of “unstructured” data because it contains data coming from different sources. True/False?

    - [x] Inception blocks allow the use of a combination of 1x1, 3x3, 5x5 convolutions and pooling by stacking up all the activations resulting from each type of layer.
    - [ ] Making an inception network deeper won't hurt the training set performance.
    - [x] One problem with simply stacking up several layers is the computational cost of it.
    - [ ] Inception blocks allow the use of a combination of 1x1, 3x3, 5x5 convolutions, and pooling by applying one layer after the other.

    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

8. RNNs (Recurrent Neural Networks) are good for data with a temporal component. True/False?

    - [ ] The same techniques for winning computer vision competitions, such as using multiple crops at test time, are widely used in practical deployments (or production system deployments) of ConvNets.
    - [ ] It is a convenient way to get working with an implementation of a complex ConvNet architecture.
    - [x] Parameters trained for one computer vision task are often useful as pre-training for other computer vision tasks.
       > ✔️ <spane style="color: green;">**Correct**</br>True.</span>
    - [x] A model trained for one computer vision task can usually be used to perform data augmentation for a different computer vision task.
      > ✖️ <span style="color: red;">**This should not be selected**</br>False, data augmentation is another process and has little to do with the weights or the architecture of the model (which you have seen in this course. However, with the advancement in the field some counterexamples have emerged, like GANs).</span>  

    > ✖️ <span style="color: red;">**Incorrect**</br>You didn't select all the correct answers</span>

---

9. In Depthwise Separable Convolution you:

    - [ ] Perform one step of convolution.
    - [x] You convolve the input image with $n_{c}$ number of $n_{f}\times n_{f}$ filters ($n_{c}$ is the number of color channels of the input image).
    - [ ] You convolve the input image with a filter of $n_{f}\times n_{f}\times n_{c}$ where $n_{c}$ acts as the depth of the filter ($n_{c}$ is the number of color channels of the input image).
    - [ ] The final output is of the dimension $n_{out} \times n_{out}\times n_{c}$ (where $n_{c}$ is the number of color channels of the input image).
    - [x] For the “Depthwise” computations each filter convolves with only one corresponding color channel of the input image.
    - [x] Perform two steps of convolution.
    - [ ] For the “Depthwise” computations each filter convolves with all of the color channels of the input image.
    - [x] The final output is of the dimension $n_{out} \times n_{out}\times n^{'}_{c}$ (where $n^{'}_{c}$ is the number of filters used in the pointwise convolution step).

    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

10. Suppose that in a MobileNet v2 Bottleneck block the input volume has shape $64\times 64\times 16$. If we use $32$ filters for the expansion and $16$ filters for the projection. What is the size of the input and output volume of the depthwise convolution, assuming a pad='same'?

    - [x] $64\times 64\times 32$, $64\times 64\times 32$
    - [ ] $32\times 32\times 32$, $32\times 32\times 32$
    - [ ] $64\times 64\times 16$, $64\times 64\times 32$
    - [ ] $64\times 64\times 32$, $64\times 64\times 16$

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, the size of the input and output volume of the depthwise convolution is determined by the number of filters in the expansion.</span>
