# chapter 3 - shallow neural networks

## same methodology
an equation represents a **family** of input/output relations. 

depending on the choice of the parameters we chose a member of this family. 

we **fit** the data to our model with a training data set by defining a cost function and looking for parameters **minimizing** it.

we look at how well the model perform on test data (**generalization**)

## hidden units
refers to a term in calculating the output (one preliminary step in the neural network process = the caluclation input/output relationship) inside an activation function

in the example these are linear functions inside a ReLu activation function
### active patterns :
#### active
when a hidden unit is non zero on a certain space of inputs we call it active
#### inactive
when a hidden unit equals zero on a certain space of inputs we call it inactive
