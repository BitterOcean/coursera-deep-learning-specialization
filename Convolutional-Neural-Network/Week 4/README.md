# **Special Applications: Face Recognition & Neural Style Transfer**

## <span style="color: green;">**Congratulations! You passed!**</span>

### **Grade received** <span style="color: green;">100%</span>

### **Latest Submission Grade** 100%

### **To pass** 80% or higher

---

1. Face verification and face recognition are the two most common names given to the task of comparing a new picture against one person's face. True/False?

   - [x] False
   - [ ] True

    > ✔️ <spane style="color: green;">**Correct**</br>Correct. This is the description of face verification, but not of face recognition.</span>

---

2. Why do we learn a function $d(img1,img2)$ for face verification? (Select all that apply.)

    - [ ] This allows us to learn to predict a person’s identity using a softmax output unit, where the number of classes equals the number of persons in the database plus 1 (for the final “not in database” class).
    - [x] We need to solve a one-shot learning problem.
    - [x] This allows us to learn to recognize a new person given just a single image of that person.
    - [ ] Given how few images we have per person, we need to apply transfer learning.

    > ✔️ <spane style="color: green;">**Correct**</br>Great, you got all the right answers.</span>

---

3. In order to train the parameters of a face recognition system, it would be reasonable to use a training set comprising 100,000 pictures of 100,000 different persons.

    - [x] False
    - [ ] True

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, to train a network using the triplet loss you need several pictures of the same person.</span>

---

4. Which of the following is a correct definition of the triplet loss? Consider that $\alpha > 0$. (We encourage you to figure out the answer from first principles, rather than just refer to the lecture.)

    - [x] $max(||f(A)-f(P)||^2 - ||f(A)-f(N)||^2 + \alpha, 0)$
    - [ ] $max(||f(A)-f(N)||^2 - ||f(A)-f(P)||^2 + \alpha, 0)$
    - [ ] $max(||f(A)-f(N)||^2 - ||f(A)-f(P)||^2 - \alpha, 0)$
    - [ ] $max(||f(A)-f(P)||^2 - ||f(A)-f(N)||^2 - \alpha, 0)$

    > ✔️ <span style="color: green;">**Correct**</br>Correct</span>

---

5. Consider the following Siamese network architecture: 

    The upper and lower neural networks have different input images, but have exactly the same parameters.

    - [ ] False
    - [x] True

    > ✔️ <spane style="color: green;">**Correct**</br>Yes it is true, parameters are shared among these two networks.</span>

---

6. You train a ConvNet on a dataset with 100 different classes. You wonder if you can find a hidden unit which responds strongly to pictures of cats. (I.e., a neuron so that, of all the input/training images that strongly activate that neuron, the majority are cat pictures.) You are more likely to find this unit in layer 4 of the network than in layer 1.

    - [x] True
    - [ ] False

    > ✔️ <spane style="color: green;">**Correct**</br>Yes, this neuron understands complex shapes (cat pictures) so it is more likely to be in a deeper layer than in the first layer.</span>

---

7. Neural style transfer is trained as a supervised learning task in which the goal is to input two images ($x$), and train a network to output a new, synthesized image ($y$)

    - [ ] True
    - [x] False

    > ✔️ <spane style="color: green;">**Correct**</br>Yes, Neural style transfer is about training the pixels of an image to make it look artistic, it is not learning any parameters.</span>

---

8. In neural style transfer, we define style as:

    - [ ] The correlation between the generated image $G$ and the style image $S$.
    - [ ] $\left\| a^{[l](S)} - a^{[l](G)} \right\|^2$ the distance between the activation of the style image and the content image.
    - [x] The correlation between activations across channels of an image.
    - [ ] The correlation between the activation of the content image $C$ and the style image $S$.

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, this correlation is represented by $G^{[I](I)}_{kk^{'}}$ for the image $I$.</span>

---

9. In neural style transfer, we can't use gradient descent since there are no trainable parameters. True/False?

    - [ ] True
    - [x] False

    > ✔️ <spane style="color: green;">**Correct**</br>Correct. We use gradient descent on the cost function $J(G)$ and we update the pixel values of the generated image $G$.</span>

---

10. You are working with 3D data. The input "image" has size $64\times 64\times 64\times 3$, if you apply a convolutional layer with 16 filters of size $4\times 4\times 4$, zero padding and stride 2. What is the size of the output volume?

    - [ ] $31\times 31\times 31\times 3$
    - [x] $31\times 31\times 31\times 16$
    - [ ] $61\times 61\times 61\times 14$
    - [ ] $64\times 64\times 64\times 3$

    > ✔️ <spane style="color: green;">**Correct**</br>Correct, we can use the formula $\lfloor \frac{n^{l-1}-f+2\times p}{s} \rfloor + 1 = n^{[l]}$ to the three first dimensions.</span>
