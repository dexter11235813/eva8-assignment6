# eva8-assignment6

<h2 align = 'left'> Part 1 </h2>

![](/assets/backprop-calculations.png) 
<center> Screenshot of the worksheet containing backpropagation calculations</center>

All the calculations are available in the [BackPropagation.xlsx](BackPropagation.xlsx) notebook, in the sheet named ```assignment6-calculations```. 

- The model contains 2 input and 2 output nodes. 
- During the backpropagation step, the relative contribution of each node to the final loss value is evaluated, starting from the nodes closest to the output, and working backwards using the chain rule. 
- The weight updates begin from the nodes closest to the inputs, and proceed towards the weights closest to the output. 
- The weight update is regulated by the Learning Rate parameter. A lower LR leads to smaller changes in the weights, whereas a higher LR results in more drastic weight changes.



<h3 align = 'center'> Effect of changing learning rate on the loss curve</h3>

As the learning rate for the backpropagation algorithm increases, the loss curve decreases quickly, suggesting that the network converges to the true values of the weight quickly with higher LR. But for a very high learning rate like 1e4, the model does not learn anything as the weight updates are too drastic, and therefore the loss curve does not decrease. 


![](/assets/eta0.1.png) 
<center> Loss Curve with LR = 0.1</center>

![](/assets/eta0.2.png) 
<center> Loss Curve with LR = 0.2</center>

![](/assets/eta0.5.png) 
<center> Loss Curve with LR = 0.5</center>

![](/assets/eta0.8.png) 
<center> Loss Curve with LR = 0.8</center>

![](/assets/eta1.png) 
<center> Loss Curve with LR = 1</center>

![](/assets/eta2.png) 
<center> Loss Curve with LR = 2</center>

![](/assets/eta1e4.png) 
<center> Loss Curve with LR = 10000</center>


<h2 align = 'left'> Part 2 </h2>

Parameter Count = 19,298 

Maximum Test Accuracy = 99.51, in the 16th epoch. 

- The model is composed of 9 ```conv``` blocks, with the number of kernels expanding to 32 in the middle before reducing to 10 in the final layer. 
- Each ```conv``` layer is followed by a ```BatchNorm``` and a ```Dropout``` layer,  except the final ```conv``` layer, which is followed by an ```AvgPool``` layer.
-  The model crosses the 99.4 % test accuracy score in the 9th epoch, and stays above the benchmark for the rest of the training duration. 

![](/assets/model_summary.png) 
<center> Model Summary</center>
