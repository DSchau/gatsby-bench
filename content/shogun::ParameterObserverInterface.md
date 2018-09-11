---
classname: "shogun::ParameterObserverInterface"
type: "class"
---

# class `shogun::ParameterObserverInterface` {#classshogun_1_1ParameterObserverInterface}

Interface for the parameter observer classes

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a59c24a2eaaaf347bd6d41722660f8fa4)`()` | Default constructor
`public  `[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a06fa5f427ddea3106e42669746f496a1)`(std::vector< std::string > & parameters)` | Constructor 
`public  `[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a230c78eee4c0ee917c70b500c9090a4e)`(const std::string & filename,std::vector< std::string > & parameters)` | Constructor 
`public virtual  `[`~ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a2434fc381ff656f18d1942989e630f83)`()` | Virtual destructor
`public virtual bool `[`filter`](#classshogun_1_1ParameterObserverInterface_1a06755c51d360cd63cb274ac8450c3b09)`(const std::string & param)` | Filter function, check if the parameter name supplied is what we want to monitor 
`public void `[`on_next`](#classshogun_1_1ParameterObserverInterface_1a17bd29a864d1f411d17efc4a07ef6957)`(const `[`TimedObservedValue`](#namespaceshogun_1aa7652406eeda765b6de5783028c8b301)` & value)` | Method which will be called when the parameter observable emits a value. 
`public void `[`on_error`](#classshogun_1_1ParameterObserverInterface_1ae2d4088ef67c9da57d64a73d2ef6d988)`(std::exception_ptr)` | Method which will be called on errors
`public void `[`on_complete`](#classshogun_1_1ParameterObserverInterface_1a4591c80fd4d0ac1e2ebbfb5d08fe33a7)`()` | Method which will be called on completion
`public inline virtual void `[`clear`](#classshogun_1_1ParameterObserverInterface_1aae048282c7011eedc2e0492f6421ea73)`()` | Method useful to empty the observer from obseverd value it may have stored.
`protected std::vector< std::string > `[`m_parameters`](#classshogun_1_1ParameterObserverInterface_1a1209abb222360997a05c68f909c8e8a3) | List of parameter's names we want to monitor
`protected `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` `[`m_type`](#classshogun_1_1ParameterObserverInterface_1ace0053c84cd8401172d2e5af7a306bbb) | The type of params this observers accept

## Members

#### `public  `[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a59c24a2eaaaf347bd6d41722660f8fa4)`()` {#classshogun_1_1ParameterObserverInterface_1a59c24a2eaaaf347bd6d41722660f8fa4}

Default constructor

#### `public  `[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a06fa5f427ddea3106e42669746f496a1)`(std::vector< std::string > & parameters)` {#classshogun_1_1ParameterObserverInterface_1a06fa5f427ddea3106e42669746f496a1}

Constructor 
#### Parameters
* `parameters` list of parameters which we want to watch over

#### `public  `[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a230c78eee4c0ee917c70b500c9090a4e)`(const std::string & filename,std::vector< std::string > & parameters)` {#classshogun_1_1ParameterObserverInterface_1a230c78eee4c0ee917c70b500c9090a4e}

Constructor 
#### Parameters
* `filename` name of the generated output file 

* `parameters` list of parameters which we want to watch over

#### `public virtual  `[`~ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface_1a2434fc381ff656f18d1942989e630f83)`()` {#classshogun_1_1ParameterObserverInterface_1a2434fc381ff656f18d1942989e630f83}

Virtual destructor

#### `public virtual bool `[`filter`](#classshogun_1_1ParameterObserverInterface_1a06755c51d360cd63cb274ac8450c3b09)`(const std::string & param)` {#classshogun_1_1ParameterObserverInterface_1a06755c51d360cd63cb274ac8450c3b09}

Filter function, check if the parameter name supplied is what we want to monitor 
#### Parameters
* `param` the param name 

#### Returns
true if param is found inside of m_parameters list

#### `public void `[`on_next`](#classshogun_1_1ParameterObserverInterface_1a17bd29a864d1f411d17efc4a07ef6957)`(const `[`TimedObservedValue`](#namespaceshogun_1aa7652406eeda765b6de5783028c8b301)` & value)` {#classshogun_1_1ParameterObserverInterface_1a17bd29a864d1f411d17efc4a07ef6957}

Method which will be called when the parameter observable emits a value. 
#### Parameters
* `value` the value emitted by the parameter observable

#### `public void `[`on_error`](#classshogun_1_1ParameterObserverInterface_1ae2d4088ef67c9da57d64a73d2ef6d988)`(std::exception_ptr)` {#classshogun_1_1ParameterObserverInterface_1ae2d4088ef67c9da57d64a73d2ef6d988}

Method which will be called on errors

#### `public void `[`on_complete`](#classshogun_1_1ParameterObserverInterface_1a4591c80fd4d0ac1e2ebbfb5d08fe33a7)`()` {#classshogun_1_1ParameterObserverInterface_1a4591c80fd4d0ac1e2ebbfb5d08fe33a7}

Method which will be called on completion

#### `public inline virtual void `[`clear`](#classshogun_1_1ParameterObserverInterface_1aae048282c7011eedc2e0492f6421ea73)`()` {#classshogun_1_1ParameterObserverInterface_1aae048282c7011eedc2e0492f6421ea73}

Method useful to empty the observer from obseverd value it may have stored.

#### `protected std::vector< std::string > `[`m_parameters`](#classshogun_1_1ParameterObserverInterface_1a1209abb222360997a05c68f909c8e8a3) {#classshogun_1_1ParameterObserverInterface_1a1209abb222360997a05c68f909c8e8a3}

List of parameter's names we want to monitor

#### `protected `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` `[`m_type`](#classshogun_1_1ParameterObserverInterface_1ace0053c84cd8401172d2e5af7a306bbb) {#classshogun_1_1ParameterObserverInterface_1ace0053c84cd8401172d2e5af7a306bbb}

The type of params this observers accept

