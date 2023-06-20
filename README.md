# Image_Cartoonifier
<ul>
  <li>Machine learning :</li>
</br>
 If for a particular task T, performance P increases with experience E, the problem can be classified as a machine learning problem
 </br>
 </br>
 <li>Supervised learning :</li>
 </br>
You are given a dataset with correct values. Supervised learning problems can be classified as -
</br>
</br>
<ul>
<li>Regression : Predicts continuous value output. It is also used when you have a large number of discrete values</li>
</br>
<li>Classification : Predicts discrete value output</li>
</br>
</ul>
<li>Unsupervised Learning :</li>
</br>
You are given a dataset without any knowledge of the values, find a structure in the given dataset. Some algorithms are -
</br>
</br>
<ul>
<li>Clustering Algorithm : Cluster the given dataset into different groups</li>
</br>
<li>Cocktail Party Algorithm : Used to separate superposed audio from varied sources</li>
</br>
</br>
</ul>
Supervised learning Idea:
</br>
</br>
Optimization Problem : Minimize the cost function subject to no constraints. The following ideas can be used-
</br>
</br>
<ul>
    <li>Gradient descent : An idea utilized in unconstrained optimisation to reduce the objective function by traversing a certain length (step length or learning rate ) in the negative direction of the gradient at the point. The following points must be remembered while chosing the step length -</li>
   <ul>
     </br>
  </br>
     <li>If step length is too small gradient descent is too slow</li>
     </br>
      <li>If step length is too large gradient descent can overshoot the minimum. It may fail to converge or even diverge.</li>
     </br>
      <li>No need to decrease the step length over time. As we approach the local minimum, gradient descent will automatically take smaller steps.</li>
     </br>
      <li>To choose an optimal step length start with a very small step length and keep on scaling till the cost function decreases with increases in number of iterations </li>
     </br>
   </ul>
   <li>Normal equation : An idea to analytically solve the optimization problem by setting the partial derivatives of the objective function to zero. It does not require a step length to be chosen. It is a non iterative method. </li>
    </ul>
</br>
</br>
Terminology
</br>
</br>
<ul>
  <li>Training set : Dataset</li>
  </br>
    <li>Hypothesis function : It maps the training set to the estimated value of the output.</li>
    </br>
    <li>Cost function : It gives an estimate as to how close is the hypothesis to the actual value.</li>
    </br>
    <li>Feature scaling : For multiple features, it is seen that gradient descent converges much faster if the features are in the same range of values. So features sre appropriately multiplied or divided (scaled) by certain values.</li>


  </ul>

</ul>
<ul>
  <li><b> Neural Networks</b></li>
  </br>Types of Neural networks</br></br>
  <ul>
  <li>Standard neural network-Application : Real estate and Online advertising</li>
  </br>
  <li>Convolutional neural network- Used for image inputs. 
  Application : Photo tagging</li>
  </br>
  <li>Recurrent neural network- Used when you have sequence data such as text and audio. An audio is considered as a temporal (time) sequence.
  Application : Speech recognition and Machine translation </li>
  </br>
  <li>Hybrid neural network- Used for complex applications such as autonomous driving </li>
  </br>
</ul>
 </br>Steps</br></br>
  <ul>
  <li>Forward propagation : To calculate the objective function (function to be optimized)</li>
  </br>
  <li>Backward propagation : To calculate the derivative of the objective function ( Visualize a computational graph of the derivative using the chain rule) </li>
  </br>
</ul>
  Structure of Neural networks</br></br>
  <ul>
  <li>Input layer : Contains a stack of nodes which are input to the neural network </li>
  </br>
  <li>Hidden layer : Consists of the stack of nodes which aren't seen in the training data</li>
  </br>
  <li>Output layer : The output/predicted value of the neural network</li>
  </br>
  <li>Activation values : Set of nodes which are passed as input to the subsequent layer </li>
  </br>
  <li>Hyper parameters : Parameters that help you compute the real parameters. Eg- learning rate, number of hidden units, number of hidden nodes etc. </li>
  </br>
  <li>N layered neural network : A neural network is said to be N layered if it consists of N lyers <b>excluding</b> the input layer</li>
  </br>
  <li>Vectorization : Nodes of a particular layer are stacked vertically and training examples are stacked horizontally</li>
  </br>
  <li>Activation function : Function that maps two subsequent layers</li>
  </br>
    Types :
  </br>
    <ul>
      <li>Linear activation function  : May be used with the output layer. Generally not used with hidden layers because the combination of linear functions is a linear function. </li>
      </br>
      <li>Sigmoid function : Used primarily for the output layer during binary classification</li>
      </br>
      <li>Hyperbolic tangent function : Superior to the sigmoid function. Mean value is zero. At very large and small values of z the gradient becomes almost zero making gradient descent slow. </li>
      </br>
      <li>Rectified Linear Unit (ReLU) function : Def - max(0,z) </br> Most commonly used. Overcomes the drawback of the tanh function in the positive range.</li>
      </br>
      <li>Leaky ReLU function : Def - max(0.01*z,z) </br>Overcomes the drawback of gradient descent being very slow in all ranges.</li>
      </br>
    </ul>
    Random Initialization : z = wx + b </br> The weight w is randomly initialized instead of being initialized to a zero matrix because doing the latter will give the same output for every node which defeats the purpose of having multiple nodes in a particular hidden layer. This problem is often termed as symmetry. However the weight b can be initialized to a zeo matrix as initializing w to a non zero matrix breaks the symmetry.
</ul>
 </ul>

 
 <ul>
  <li><b> Convolutional Neural Networks</b></li>
  </br>Applications</br></br>
  <ul>
  <li>Image classification - Identify objects present in the image</li>
  </br>
  <li>Object detection - Identify the location of objects in the image </li>
  </br>
  <li>Neural style transfer - Applying an art style to your image </li>
  </br>
  </ul>
   <li>Convolution Vs Cross Correlation</li>
   <p>In mathematics and signal processing the convolution operation involves applying an additional mirror operation on the filter before overlapping it with the image. This gives the convolution operator an additional property of associativity ( $A*(B*C)=(A*B)*C$) useful in mathematics and signal processing. Convolution without this inital mirroring of the filter is strictly called cross correlation but in machine learning literature it is referred to as convolution.</p>
    <li>Disadvantages of convolution</li>
 </br>
    <ul>
      <li>Shrinkage of image output : If you have a nXn image convoluted with a fXf filter the image output is of size (n-f+1)X(n-f+1) </li>
    </br>
       <li>Throwing away information from the corners : During convolution the filter overlaps with the corners only once whereas the other pixels are overlapped with several times. It is as if the corner information is being less represented in the output. </li>
    </br>
    </ul>
   <li>Padding</li>
 </br>To overcome the above disadvantages we add extra pixels around the border. This is known as padding. Depending on the type of padding there are two types of convolutions :</br>
   <ul>
     <li>Valid : Padding size is 0.</li>
     <li>Same : Padding size is such that image output is of the same size as that of the input. When the padding size is p image output is of size (n+2p-f-1)X(n+2p-f+1). For no shrinkage</br> $n+2p-f+1=n$</br>$p= (f-1)/2$</br>Note : Generally f is odd which enables symmetric padding and helps us to define a central position.</li>
   </ul>
 </br>
   <li>Strided Convolutions : Defining the stride tells us how many pixels to jump while applying the filter for the convolution operation. The size of the image output is $((n+2p-f)/s +1)X((n+2p-f)/s + 1)$</li>
    </ul>
  
    
</ul>
 
