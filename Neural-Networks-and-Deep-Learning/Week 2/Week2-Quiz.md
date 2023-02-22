# Neural Network Basics

1. What does a neuron compute?

   > **A neuron computes a linear function $z = Wx + b$ followed by an activation function**

---

2. Which of these is the "Logistic Loss"?

    > **$\mathcal{L}^{(i)}(\hat{y}^{(i)}, y^{(i)}) = -(y^{(i)} \log(\hat{y}^{(i)}) + (1-y^{(i)})\log(1-\hat{y}^{(i)}))$**

---

3. Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector $x$?

    > **x = img.reshape((32*32*3, 1))**

---

4. Consider the following random arrays $a$ and $b$, and $c$:

   $a = np.random.randn(3, 3) ~\sharp a.shape = (3, 3)$

   $b = np.random.randn(2, 1) ~\sharp b.shape = (2, 1)$

   $c = a + b$

   What will be the shape of $c$?

    > **The computation cannot happen becausse it is not possible to broadcast more than one dimension**

---

5. Consider the following random arrays $a$ and $b$:

   $a = np.random.randn(1, 3) ~\sharp a.shape = (1, 3)$

   $b = np.random.randn(3, 3) ~\sharp b.shape = (3, 3)$

   $c = a * b$

   What will be the shape of $c$?

   > **c.shape = (3, 3)**
---

6. Suppose you have $n_{x}$ input features per example. Recall that $X = [x^{(1)}~x^{(2)}~\cdots~x^{(m)}]$ What is the dimension of $X$? 

    > **$(n_x, m)$**

---

7. Consider the following array:
   
   $a = np.array([[2, 1], [1, 3]])$

   What is the result of $a*a$ ?

    > **$\begin{pmatrix}
        4 & 1 \\
        1 & 9
    \end{pmatrix}$**

---

8. Consider the following code sinppet:
   
   $a.shape = (3, 4)$

   $b.shape = (4, 1)$

   for i in range(3):
   
   for j in range(4):
   
   c[i][j] = a[i][j] + b[j]
    
    How do you vectorize this?

    > **c = a + b.T**

---

9. Consider the code sinppet:
   
   $a.shape = (3, 3)$

   $b.shape = (3, 3)$

   $c = a**2 + b.T**2$

   Which of the following gives an equivalent output for $c$?
    
    
   > **for i in range(3):</br>
   for j in range(3):</br>
   c[i][j] = a[i][j]\*\*2 + b[j][i]\*\*2**

---

10. Consider the following computational graph.
    
    ![q10.png](img/q10.png)

    What is the output of $J$?

   > **$(a+c)(b-1)$**
