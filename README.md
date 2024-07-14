#Overview
A fast, interpretable and theory-inspired application of neural networks

##Contributors
- Jaiman Parekh
- Kevin Steiger
- Mark Nyevgen

##Explanation
A convolutional neural network to extract edges from noisy images using the **shearlet** and **ridgelet** transform.

The discrete shearlet transform will be used in a preprocessing stage to identify edges in images. Shearlets will be used due to their extensive properties in forming *optimal orthonormal bases* for singular temporal/spatial data and due to their capability in assigning *orientation* to curves. Additionally, many fruitful connections to abstract harmonic analysis are present in their theoretical exploration.

Then the processed data will be fed into a CNN, where ReLU activation functions will be used. A key deviation from classic CNNs, though, is the use of a *shallow network* of large width; i.e, minimal layers will be used but each layer will have a large number of neurons. The weights for these neurons will then converge to a distribution governed by the ridge transform of the input data. As such, *backpropagation is not needed*, as the resulting weights for each neuron will be known.

Finally, this model will be trained, tested, and compared against competing models. 

##References
By no means a comprehensive list, simply the main guiding papers.

Ridgelet transform: arXiv:2007.03441v2
Shearlet transform: arXiv:1901.01388v2
