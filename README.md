# Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization
from coursera courses (deep learning specification)
https://www.coursera.org/learn/deep-neural-network/home/welcome

1.1 Practical aspects of deep learning
- Train/dev/test sets
			<br/>i. 70/30 train/test
			<br/>ii. 60/20/20 train/dev/test
			<br/>iii. Big data era (e.g. >1,000,000) 98/1/1 or 99.5/0.4/0.1
			<br/>iv. Mismatched train/test distribution
				<br/>-1) Train and test sets use different distributions
				<br/>-2) Make sure dev and test sets come from the same distribution
It is OK not have a test set (only dev set, some people call it test set)
- Bias/ Variance
			<br/>i. High bias: underfitting, high train set error
			<br/>ii. High Variance: overfitting, high dev set error

- Basic recipe for machine learning
			<br/>i. High bias? (training data performance)-> bigger network/more hidden layer/more hidden units/train longer/neutral net architecture search
			<br/>ii. High variance? (dev set performance)-> more training data/regularization(e.g increase the regularization parameter lambda, L2 regularization, Data augmentation)/NN architecture search
			<br/>iii. Bias variance tradeoff sometime is not always true in Deep learning
- weight decay: 		
  <br/>Weight decay: A regularization technique (such as L2 regularization) that results in gradient descent shrinking the weights on every iteration; Increasing regularization hyperparameter lambda: weights are pushed toward becoming smaller (closer to 0)

- Dropout Regularization
			 <br/>i. Remove some notes
			 <br/>ii. Implementing dropout (inverted dropout)
       	<br/>iii. Making predictions at test time
				-• Not use dropout at test:
				-• You do not apply dropout (do not randomly eliminate units) and do not keep the 1/keep_prob factor in the calculations used in training
				- Increasing the parameter keep_prob will cause:
					• Reducing the regularization effect
					• Causing the neural network to end up with a lower training set error
			<br/>iv. Why dropout works:Intuition: can't rely on any one feature, so have to spread out weights- shrink weight
      
- Other regularization methods
	<br/>i. Data augmentation: rotate image, mirror image, zoom in, distortion, transformation
	<br/>ii. Early stopping 
		1) Orthogonalization issue: Optimize cost function J; Not overfit

- Normalization
	<br/>i. why normalize the input x: Not normalized: elongated hard for gradient descent to reach minimal; makes the cost function faster to optimize

- Vanishing/exploding gradient problem
  <br/>	1) your derivatives or your slopes can sometimes get either very, 
				very big or very, very small
	<br/>2) Partial solution: carefully select the weight

1.2 Initialization Practice Project
 - [Initialization Practice Project link](Initialization.ipynb)

1.3 Regularization Practice Project
- [Regularization Practice Project Link](Regularization+-+v2.ipynb)

1.4 Gradient Checking Practice Projact
- [Regularization Practice Project Link](Gradient Checking.ipynb)
