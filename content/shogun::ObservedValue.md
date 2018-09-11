---
classname: "shogun::ObservedValue"
type: "class"
---

# class `shogun::ObservedValue` {#classshogun_1_1ObservedValue}

Observed value which is emitted by algorithms.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`ObservedValue`](#classshogun_1_1ObservedValue_1a774c62e359fd0c3373157878a9d91788)`(int64_t step,std::string & name,`[`Any`](#classshogun_1_1Any)` value,`[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type)` | Constructor 
`public inline  `[`~ObservedValue`](#classshogun_1_1ObservedValue_1a06bc6fe93050ca52d2503f09bcb87e6b)`()` | 
`public inline int64_t `[`get_step`](#classshogun_1_1ObservedValue_1af38736cfe348e60c9809cf20a754369d)`() const` | Get the step 
`public inline void `[`set_step`](#classshogun_1_1ObservedValue_1ad3411e5b70c144f0e43c32d008b5645e)`(int64_t step)` | Set the step 
`public inline const std::string & `[`get_name`](#classshogun_1_1ObservedValue_1aea1591b1773209f55ccc85356efb639a)`() const` | Get the param's name 
`public inline void `[`set_name`](#classshogun_1_1ObservedValue_1ad5260b9627048b854b45d05ed34adc22)`(const std::string & name)` | Set the param's name 
`public inline const `[`Any`](#classshogun_1_1Any)` & `[`get_value`](#classshogun_1_1ObservedValue_1adf3a0e19a701caccb7652a63cef9600b)`() const` | Get the Any-wrapped value 
`public inline void `[`set_value`](#classshogun_1_1ObservedValue_1ab88eb41b6e22f4098aa19c468aafefa9)`(const `[`Any`](#classshogun_1_1Any)` & value)` | Set the param's value 
`public inline `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` `[`get_type`](#classshogun_1_1ObservedValue_1a81971c757523a4a140d76f43663be433)`() const` | Get the type of this [ObservedValue](#classshogun_1_1ObservedValue)
`public inline void `[`set_type`](#classshogun_1_1ObservedValue_1a4c9100e85ed0a32db0195a872b5335ae)`(const `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type)` | Set the observed value type 
`protected int64_t `[`m_step`](#classshogun_1_1ObservedValue_1a0466afa2e7d96f1ee8bc64f75295d897) | [ObservedValue](#classshogun_1_1ObservedValue) step (used by Tensorboard to print graphs)
`protected std::string `[`m_name`](#classshogun_1_1ObservedValue_1adb41893ba19e889e56c559f25fc1a68a) | [Parameter](#classshogun_1_1Parameter)'s name
`protected `[`Any`](#classshogun_1_1Any)` `[`m_value`](#classshogun_1_1ObservedValue_1a179ec21b58b7aed3019a61b22934d525) | [Parameter](#classshogun_1_1Parameter)'s value
`protected `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` `[`m_type`](#classshogun_1_1ObservedValue_1ace0053c84cd8401172d2e5af7a306bbb) | [ObservedValue](#classshogun_1_1ObservedValue) type

## Members

#### `public inline  `[`ObservedValue`](#classshogun_1_1ObservedValue_1a774c62e359fd0c3373157878a9d91788)`(int64_t step,std::string & name,`[`Any`](#classshogun_1_1Any)` value,`[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type)` {#classshogun_1_1ObservedValue_1a774c62e359fd0c3373157878a9d91788}

Constructor 
#### Parameters
* `step` step 

* `name` param's name 

* `value` Any-wrapped value of the param

#### `public inline  `[`~ObservedValue`](#classshogun_1_1ObservedValue_1a06bc6fe93050ca52d2503f09bcb87e6b)`()` {#classshogun_1_1ObservedValue_1a06bc6fe93050ca52d2503f09bcb87e6b}

#### `public inline int64_t `[`get_step`](#classshogun_1_1ObservedValue_1af38736cfe348e60c9809cf20a754369d)`() const` {#classshogun_1_1ObservedValue_1af38736cfe348e60c9809cf20a754369d}

Get the step 
#### Returns
an integer representing the step

#### `public inline void `[`set_step`](#classshogun_1_1ObservedValue_1ad3411e5b70c144f0e43c32d008b5645e)`(int64_t step)` {#classshogun_1_1ObservedValue_1ad3411e5b70c144f0e43c32d008b5645e}

Set the step 
#### Parameters
* `step` step

#### `public inline const std::string & `[`get_name`](#classshogun_1_1ObservedValue_1aea1591b1773209f55ccc85356efb639a)`() const` {#classshogun_1_1ObservedValue_1aea1591b1773209f55ccc85356efb639a}

Get the param's name 
#### Returns
param's name

#### `public inline void `[`set_name`](#classshogun_1_1ObservedValue_1ad5260b9627048b854b45d05ed34adc22)`(const std::string & name)` {#classshogun_1_1ObservedValue_1ad5260b9627048b854b45d05ed34adc22}

Set the param's name 
#### Parameters
* `name`

#### `public inline const `[`Any`](#classshogun_1_1Any)` & `[`get_value`](#classshogun_1_1ObservedValue_1adf3a0e19a701caccb7652a63cef9600b)`() const` {#classshogun_1_1ObservedValue_1adf3a0e19a701caccb7652a63cef9600b}

Get the Any-wrapped value 
#### Returns
Any-wrapped value

#### `public inline void `[`set_value`](#classshogun_1_1ObservedValue_1ab88eb41b6e22f4098aa19c468aafefa9)`(const `[`Any`](#classshogun_1_1Any)` & value)` {#classshogun_1_1ObservedValue_1ab88eb41b6e22f4098aa19c468aafefa9}

Set the param's value 
#### Parameters
* `value`

#### `public inline `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` `[`get_type`](#classshogun_1_1ObservedValue_1a81971c757523a4a140d76f43663be433)`() const` {#classshogun_1_1ObservedValue_1a81971c757523a4a140d76f43663be433}

Get the type of this [ObservedValue](#classshogun_1_1ObservedValue)
#### Returns
observed value type

#### `public inline void `[`set_type`](#classshogun_1_1ObservedValue_1a4c9100e85ed0a32db0195a872b5335ae)`(const `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type)` {#classshogun_1_1ObservedValue_1a4c9100e85ed0a32db0195a872b5335ae}

Set the observed value type 
#### Parameters
* `type` type of this observed value

#### `protected int64_t `[`m_step`](#classshogun_1_1ObservedValue_1a0466afa2e7d96f1ee8bc64f75295d897) {#classshogun_1_1ObservedValue_1a0466afa2e7d96f1ee8bc64f75295d897}

[ObservedValue](#classshogun_1_1ObservedValue) step (used by Tensorboard to print graphs)

#### `protected std::string `[`m_name`](#classshogun_1_1ObservedValue_1adb41893ba19e889e56c559f25fc1a68a) {#classshogun_1_1ObservedValue_1adb41893ba19e889e56c559f25fc1a68a}

[Parameter](#classshogun_1_1Parameter)'s name

#### `protected `[`Any`](#classshogun_1_1Any)` `[`m_value`](#classshogun_1_1ObservedValue_1a179ec21b58b7aed3019a61b22934d525) {#classshogun_1_1ObservedValue_1a179ec21b58b7aed3019a61b22934d525}

[Parameter](#classshogun_1_1Parameter)'s value

#### `protected `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` `[`m_type`](#classshogun_1_1ObservedValue_1ace0053c84cd8401172d2e5af7a306bbb) {#classshogun_1_1ObservedValue_1ace0053c84cd8401172d2e5af7a306bbb}

[ObservedValue](#classshogun_1_1ObservedValue) type

