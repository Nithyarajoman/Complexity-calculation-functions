# Installion of the package

```bat
pip install Library_functions
```
# Usage

For the usage of the defined functions import the functions as shown below:
```python
from Library_functions import MAC_summary, data_summary
from Library_functions import split_zo_conv, split_yo_conv
```

# Complexity calculations

## MAC Operations and Effective Data Communicated

The functions for the below are included in this python library program "myfunctions_calculations":
- 1. MAC calulation for each layer of the model. Included the functionality for calculating the same if there is an inner model as well.
- 2. Effective data that is communicated from each layer of the model. Also extended the functionality for the inner models if present.

The MACs can be calculated for any model (trained/non-trained) using the function: 
```python
MAC_summary(model_name)
```

The probability of the non-zero data that are communicated from each layer can be calculated for any model (compiled/non-compiled) by providing the test datasets to be used and using the function: 
```python
data_summary(model_name)
```

#*********************************************************************************************************************************#

## Splitting the Complex Layers

The functions for the below are included in this python library program "myfunctions_splitting":
- 1. Slicing the convolutional layer in the Z direction, which is the number of filters
- 2. Slicing the convolutional layers in the Y direction in terms of the dimension

In both the cases we are manually providing the cut dimensions of the filter or the Y axis based on the complexity of the layer we choose. And finally we check the score of the original model and the model with the replaced layer to check if the efficiency has become better.


 