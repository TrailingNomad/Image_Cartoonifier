# Image_Cartoonifier
<ol>
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


  </ul>

</ol>

 
