---
classname: "shogun::CConvolutionalFeatureMap"
type: "class"
---

# class `shogun::CConvolutionalFeatureMap` {#classshogun_1_1CConvolutionalFeatureMap}

Handles convolution and gradient calculation for a single feature map in a convolutional neural network.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`CConvolutionalFeatureMap`](#classshogun_1_1CConvolutionalFeatureMap_1a2c2b2b713c6708d3b9a970c56abded5e)`(int32_t input_width,int32_t input_height,int32_t radius_x,int32_t radius_y,int32_t stride_x,int32_t stride_y,int32_t index,`[`EConvMapActivationFunction`](#namespaceshogun_1a2b9827281875ee8de764ea86e7735482)` function,`[`ENLAutoencoderPosition`](#namespaceshogun_1aedb2adb9649185615d1a620bdd8d8164)` autoencoder_position)` | Constuctor
`public void `[`compute_activations`](#classshogun_1_1CConvolutionalFeatureMap_1adc7bc2d10bc708bcb8b5ce8da9055dc8)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > input_indices,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activations)` | Computes the activations of the feature map
`public void `[`compute_gradients`](#classshogun_1_1CConvolutionalFeatureMap_1ac1eab2ed59f18e2f662c389313006259)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activations,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activation_gradients,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > input_indices,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameter_gradients)` | Computes the gradients with respect to the parameters and the inputs to the map
`public void `[`pool_activations`](#classshogun_1_1CConvolutionalFeatureMap_1a1ce92520890631b0491e9451936108d4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activations,int32_t pooling_width,int32_t pooling_height,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > pooled_activations,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > max_indices)` | Applies max pooling to the activations
`protected int32_t `[`m_input_width`](#classshogun_1_1CConvolutionalFeatureMap_1abf86f9ed134bde802f8821da930aebde) | Width of the input
`protected int32_t `[`m_input_height`](#classshogun_1_1CConvolutionalFeatureMap_1af885e7b199507f4998065e9b4160493c) | Height of the input
`protected int32_t `[`m_radius_x`](#classshogun_1_1CConvolutionalFeatureMap_1a599a8b1d8da39107e3fa1e82da043690) | Radius of the convolution filter on the x (width) axis
`protected int32_t `[`m_radius_y`](#classshogun_1_1CConvolutionalFeatureMap_1abde3cf32adf4a0fc4d62867b075dd0a0) | Radius of the convolution filter on the y (height) axis
`protected int32_t `[`m_stride_x`](#classshogun_1_1CConvolutionalFeatureMap_1abe2b0d829fbf75927f88e7860fb2ec28) | Stride in the x direction
`protected int32_t `[`m_stride_y`](#classshogun_1_1CConvolutionalFeatureMap_1ac2060e907f6b314f6ab33284f3c81ab6) | Stride in the y direcetion
`protected int32_t `[`m_index`](#classshogun_1_1CConvolutionalFeatureMap_1afe8f9f0db8cbb38fff2ac9b204af0d0e) | Index of this feature map in its layer. This affects which part of the activations/activation_gradients matrix that map will use
`protected `[`EConvMapActivationFunction`](#namespaceshogun_1a2b9827281875ee8de764ea86e7735482)` `[`m_activation_function`](#classshogun_1_1CConvolutionalFeatureMap_1a9b1ac011288e212bd55d6de55da1d55c) | The map's activation function
`protected int32_t `[`m_output_width`](#classshogun_1_1CConvolutionalFeatureMap_1a645a2cedc4c6b9e5057fbd64fb76dc9f) | Width of the convolution's output image
`protected int32_t `[`m_output_height`](#classshogun_1_1CConvolutionalFeatureMap_1a7af7e473e4093b07288294e46892485c) | Height of the convolution's output image
`protected int32_t `[`m_input_num_neurons`](#classshogun_1_1CConvolutionalFeatureMap_1a4a896f86085ef1722895125a391ddde6) | Number of neurons in the input
`protected int32_t `[`m_output_num_neurons`](#classshogun_1_1CConvolutionalFeatureMap_1aba71b1821cd98ad8d6b1c4063c59ac38) | Number of neurons in the output
`protected int32_t `[`m_row_offset`](#classshogun_1_1CConvolutionalFeatureMap_1a02586bfded2437b3c4b321d3b241a5ef) | Row offset for accessing the activations
`protected int32_t `[`m_filter_width`](#classshogun_1_1CConvolutionalFeatureMap_1a42d9f68774edd826bba4bf6df8c6a913) | Width of the convolution filter
`protected int32_t `[`m_filter_height`](#classshogun_1_1CConvolutionalFeatureMap_1a3b2e5397bf88f1fdd599258f18a60c11) | Height of the convolution filter
`protected `[`ENLAutoencoderPosition`](#namespaceshogun_1aedb2adb9649185615d1a620bdd8d8164)` `[`m_autoencoder_position`](#classshogun_1_1CConvolutionalFeatureMap_1aec7a100ffbe6edaa5d24096fd0ec5724) | For autoencoders, specifies the position of the layer in the autoencoder, i.e an encoding layer or a decoding layer. Default value is NLAP_NONE
`protected void `[`convolve`](#classshogun_1_1CConvolutionalFeatureMap_1ae6232908959dcaeb74bc87c750922277)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > weights,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > outputs,bool flip,bool reset_output,int32_t inputs_row_offset,int32_t outputs_row_offset)` | Perfoms convolution
`protected void `[`compute_weight_gradients`](#classshogun_1_1CConvolutionalFeatureMap_1aae01abdbba46f5712859e9272ceb529a)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > local_gradients,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > weight_gradients,int32_t inputs_row_offset,int32_t local_gradients_row_offset)` | Computes the gradients of the error with respect to the weights, for a particular input matrix

## Members

#### `public  `[`CConvolutionalFeatureMap`](#classshogun_1_1CConvolutionalFeatureMap_1a2c2b2b713c6708d3b9a970c56abded5e)`(int32_t input_width,int32_t input_height,int32_t radius_x,int32_t radius_y,int32_t stride_x,int32_t stride_y,int32_t index,`[`EConvMapActivationFunction`](#namespaceshogun_1a2b9827281875ee8de764ea86e7735482)` function,`[`ENLAutoencoderPosition`](#namespaceshogun_1aedb2adb9649185615d1a620bdd8d8164)` autoencoder_position)` {#classshogun_1_1CConvolutionalFeatureMap_1a2c2b2b713c6708d3b9a970c56abded5e}

Constuctor

#### Parameters
* `input_width` Width of the input 

* `input_height` Height of the input 

* `radius_x` Radius of the convolution filter on the x (width) axis 

* `radius_y` Radius of the convolution filter on the y (height) axis 

* `stride_x` Stride in the x direction 

* `stride_y` Stride in the y direction 

* `index` Index of this feature map in its layer. This affects which part of the activations/activation_gradients matrix the map will store its outputs in. 

* `function` Activation function 

* `autoencoder_position` Autoencoder position

#### `public void `[`compute_activations`](#classshogun_1_1CConvolutionalFeatureMap_1adc7bc2d10bc708bcb8b5ce8da9055dc8)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > input_indices,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activations)` {#classshogun_1_1CConvolutionalFeatureMap_1adc7bc2d10bc708bcb8b5ce8da9055dc8}

Computes the activations of the feature map

#### Parameters
* `parameters` Vector of parameters for the map. length width*height+(2*radius_x+1)+(2*radius_y+1) 

* `layers` The layers array that forms the network in which the map is being used 

* `input_indices` Indices of the layers that are connected to the map as input 

* `activations` Matrix in which the activations are to be stored

#### `public void `[`compute_gradients`](#classshogun_1_1CConvolutionalFeatureMap_1ac1eab2ed59f18e2f662c389313006259)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameters,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activations,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activation_gradients,`[`CDynamicObjectArray`](#classshogun_1_1CDynamicObjectArray)` * layers,`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > input_indices,`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > parameter_gradients)` {#classshogun_1_1CConvolutionalFeatureMap_1ac1eab2ed59f18e2f662c389313006259}

Computes the gradients with respect to the parameters and the inputs to the map

#### Parameters
* `parameters` Vector of parameters for the map. length width*height+(2*radius_x+1)+(2*radius_y+1) 

* `activations` Activations of the map 

* `activation_gradients` Gradients of the error with respect to the map's activations 

* `layers` The layers array that forms the network in which the map is being used 

* `input_indices` Indices of the layers that are connected to the map as input 

* `parameter_gradients` Vector in which the parameters gradients are to be stored

#### `public void `[`pool_activations`](#classshogun_1_1CConvolutionalFeatureMap_1a1ce92520890631b0491e9451936108d4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > activations,int32_t pooling_width,int32_t pooling_height,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > pooled_activations,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > max_indices)` {#classshogun_1_1CConvolutionalFeatureMap_1a1ce92520890631b0491e9451936108d4}

Applies max pooling to the activations

#### Parameters
* `activations` Activations of the map 

* `pooling_width` Width of the pooling region 

* `pooling_height` Height of the pooling region 

* `pooled_activations` Result of the pooling process 

* `max_indices` Row indices of the max elements for each pooling region

#### `protected int32_t `[`m_input_width`](#classshogun_1_1CConvolutionalFeatureMap_1abf86f9ed134bde802f8821da930aebde) {#classshogun_1_1CConvolutionalFeatureMap_1abf86f9ed134bde802f8821da930aebde}

Width of the input

#### `protected int32_t `[`m_input_height`](#classshogun_1_1CConvolutionalFeatureMap_1af885e7b199507f4998065e9b4160493c) {#classshogun_1_1CConvolutionalFeatureMap_1af885e7b199507f4998065e9b4160493c}

Height of the input

#### `protected int32_t `[`m_radius_x`](#classshogun_1_1CConvolutionalFeatureMap_1a599a8b1d8da39107e3fa1e82da043690) {#classshogun_1_1CConvolutionalFeatureMap_1a599a8b1d8da39107e3fa1e82da043690}

Radius of the convolution filter on the x (width) axis

#### `protected int32_t `[`m_radius_y`](#classshogun_1_1CConvolutionalFeatureMap_1abde3cf32adf4a0fc4d62867b075dd0a0) {#classshogun_1_1CConvolutionalFeatureMap_1abde3cf32adf4a0fc4d62867b075dd0a0}

Radius of the convolution filter on the y (height) axis

#### `protected int32_t `[`m_stride_x`](#classshogun_1_1CConvolutionalFeatureMap_1abe2b0d829fbf75927f88e7860fb2ec28) {#classshogun_1_1CConvolutionalFeatureMap_1abe2b0d829fbf75927f88e7860fb2ec28}

Stride in the x direction

#### `protected int32_t `[`m_stride_y`](#classshogun_1_1CConvolutionalFeatureMap_1ac2060e907f6b314f6ab33284f3c81ab6) {#classshogun_1_1CConvolutionalFeatureMap_1ac2060e907f6b314f6ab33284f3c81ab6}

Stride in the y direcetion

#### `protected int32_t `[`m_index`](#classshogun_1_1CConvolutionalFeatureMap_1afe8f9f0db8cbb38fff2ac9b204af0d0e) {#classshogun_1_1CConvolutionalFeatureMap_1afe8f9f0db8cbb38fff2ac9b204af0d0e}

Index of this feature map in its layer. This affects which part of the activations/activation_gradients matrix that map will use

#### `protected `[`EConvMapActivationFunction`](#namespaceshogun_1a2b9827281875ee8de764ea86e7735482)` `[`m_activation_function`](#classshogun_1_1CConvolutionalFeatureMap_1a9b1ac011288e212bd55d6de55da1d55c) {#classshogun_1_1CConvolutionalFeatureMap_1a9b1ac011288e212bd55d6de55da1d55c}

The map's activation function

#### `protected int32_t `[`m_output_width`](#classshogun_1_1CConvolutionalFeatureMap_1a645a2cedc4c6b9e5057fbd64fb76dc9f) {#classshogun_1_1CConvolutionalFeatureMap_1a645a2cedc4c6b9e5057fbd64fb76dc9f}

Width of the convolution's output image

#### `protected int32_t `[`m_output_height`](#classshogun_1_1CConvolutionalFeatureMap_1a7af7e473e4093b07288294e46892485c) {#classshogun_1_1CConvolutionalFeatureMap_1a7af7e473e4093b07288294e46892485c}

Height of the convolution's output image

#### `protected int32_t `[`m_input_num_neurons`](#classshogun_1_1CConvolutionalFeatureMap_1a4a896f86085ef1722895125a391ddde6) {#classshogun_1_1CConvolutionalFeatureMap_1a4a896f86085ef1722895125a391ddde6}

Number of neurons in the input

#### `protected int32_t `[`m_output_num_neurons`](#classshogun_1_1CConvolutionalFeatureMap_1aba71b1821cd98ad8d6b1c4063c59ac38) {#classshogun_1_1CConvolutionalFeatureMap_1aba71b1821cd98ad8d6b1c4063c59ac38}

Number of neurons in the output

#### `protected int32_t `[`m_row_offset`](#classshogun_1_1CConvolutionalFeatureMap_1a02586bfded2437b3c4b321d3b241a5ef) {#classshogun_1_1CConvolutionalFeatureMap_1a02586bfded2437b3c4b321d3b241a5ef}

Row offset for accessing the activations

#### `protected int32_t `[`m_filter_width`](#classshogun_1_1CConvolutionalFeatureMap_1a42d9f68774edd826bba4bf6df8c6a913) {#classshogun_1_1CConvolutionalFeatureMap_1a42d9f68774edd826bba4bf6df8c6a913}

Width of the convolution filter

#### `protected int32_t `[`m_filter_height`](#classshogun_1_1CConvolutionalFeatureMap_1a3b2e5397bf88f1fdd599258f18a60c11) {#classshogun_1_1CConvolutionalFeatureMap_1a3b2e5397bf88f1fdd599258f18a60c11}

Height of the convolution filter

#### `protected `[`ENLAutoencoderPosition`](#namespaceshogun_1aedb2adb9649185615d1a620bdd8d8164)` `[`m_autoencoder_position`](#classshogun_1_1CConvolutionalFeatureMap_1aec7a100ffbe6edaa5d24096fd0ec5724) {#classshogun_1_1CConvolutionalFeatureMap_1aec7a100ffbe6edaa5d24096fd0ec5724}

For autoencoders, specifies the position of the layer in the autoencoder, i.e an encoding layer or a decoding layer. Default value is NLAP_NONE

#### `protected void `[`convolve`](#classshogun_1_1CConvolutionalFeatureMap_1ae6232908959dcaeb74bc87c750922277)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > weights,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > outputs,bool flip,bool reset_output,int32_t inputs_row_offset,int32_t outputs_row_offset)` {#classshogun_1_1CConvolutionalFeatureMap_1ae6232908959dcaeb74bc87c750922277}

Perfoms convolution

#### Parameters
* `inputs` Inputs matrix. Each column in the matrix is treated as an image in column major format 

* `weights` Convolution filter 

* `outputs` Output matrix 

* `flip` If true the weights are flipped, performing cross-correlation instead of convolution 

* `reset_output` true the output is reset to zero before performing convolution 

* `inputs_row_offset` Index of the row at which the input image starts 

* `outputs_row_offset` Index of the row at which the output image starts

#### `protected void `[`compute_weight_gradients`](#classshogun_1_1CConvolutionalFeatureMap_1aae01abdbba46f5712859e9272ceb529a)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > inputs,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > local_gradients,`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > weight_gradients,int32_t inputs_row_offset,int32_t local_gradients_row_offset)` {#classshogun_1_1CConvolutionalFeatureMap_1aae01abdbba46f5712859e9272ceb529a}

Computes the gradients of the error with respect to the weights, for a particular input matrix

#### Parameters
* `inputs` Inputs matrix 

* `local_gradients` Gradients with respect the map's pre-activations 

* `weight_gradients` Matrix to store the gradients in 

* `inputs_row_offset` Offset for accessing the rows of the inputs matrix 

* `local_gradients_row_offset` Offset for accessing the rows of the local gradients matrix

