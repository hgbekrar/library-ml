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

## depicting a neural network with 1D input and 1D output
$$ y = f(x, **\phi**) =  \phi_0 + \phi_1\times a(\theta_{10} +\theta_{11} \times x) +\phi_2\times a(\theta_{20} +\theta_{21} \times x) + \phi_3\times a(\theta_{30} +\theta_{31} \times x)$$

<img width="485" height="519" alt="neural network complete" src="https://github.com/user-attachments/assets/3d24e469-7855-43ed-969a-5b4f8437de09" />
<img width="485" height="519" alt="neural network" src="https://github.com/user-attachments/assets/ab7e8153-4c17-4501-b244-488f002a036e" />

* both a complete drawing of the neural network and a simpler version of the same network
* the elements on the arrows represent the weights. the number on one node is multiplied by the weights in the outcoming arrow; the result is added to the next node.
