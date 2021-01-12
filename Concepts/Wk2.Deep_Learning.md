## CS540 W21 NLP + DL
### Week 2: Deep Learning 

### What is DL? 
Simply put, DL is a function that f:X->Y from model class F that best approximates g: X->Y (usually unnown but have samples from it) given a dataset D of observations of g.

#### Approximation & types of erros 
1. Modeling error
2. Estimation error
3. Optimization Error

#### How does DL work in each case of error?
1. They make a massive function class. 
2. Also, we use large datasets, well-matched architectures, and early stopping. 
3. Surprisingly low with SGD, the reason is unknown. --> We just got lucky! 


### Neuron
#### Hyperparameters: activation function 
Types of activation function
- None: f(z) = z
- Sigmoid: f(z) = 1/(1+e^(-z))
- Tanh
- ReLu
- Leaky ReLu

##### Let's take a gradient of each activation function. 
When you look at the shapes, ReLu/Leaky ReLu activation functions force the gradient to zero. 

ReLu returns output very sparsely. This property can be very useful since unlike Sigmoid which only returns 0 when the input is negative infinity. 

Therefore, ReLu gives a lot of sparsity. 

#### Shape of Activation Function 
Weight: it determines the shift -- the scale of w determines the sharpness/steepness
Biase: it determines the direction. 

* Stacking the functions together to form neural nets with different weight and bias values. (w/ matrix form)
-- stacking can be done both vertically and horizontally (sequentially).

#### Function Approximation 
- In Word2Vec: Maximize the negtive log likelihood
- Loss functions classification 
1. Squared error
2. Absolute error
3. Huber 


### Stochastic Gradient Descent 
SGD is used as a tool to minize the loss. In this class, we're going to take derivatives of vectors in respect of scalar. 

#### Our convention: numerator dim -> rows, denominator dim -> cols; 
1. vector over scalar
2. scholar over vector
3. vector over vector --> Jacobian 
4. vector over matrix --> there's not a good convention for this. We just formulate the matrix into nxm vectors and handle it in the third case.

#### Refresher: Multivariant function of derivatives

### Backpropagation: 
A reverse-mode automatic differentiation algorithms. 

#### Foundations of Backpropagation: 
- Neural networks tend to have 

#### Quiz: multiplication of matrixes left to right or right to left? 
- Right to left is faster since d has a large number (high-dimensional input), 

- Reverse mode output -> input is recommended since dim output << dim input 
