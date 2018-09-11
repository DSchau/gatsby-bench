---
classname: "shogun::CIterativeMachine"
type: "class"
parents:
   - T
---

# class `shogun::CIterativeMachine` {#classshogun_1_1CIterativeMachine}

```
class shogun::CIterativeMachine
  : public T
```

Mix-in class that implements an iterative model whose training can be prematurely stopped, and in particular be resumed, anytime.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`CIterativeMachine`](#classshogun_1_1CIterativeMachine_1a8bbd5914ed48c23775ed43571477f77e)`()` | Default constructor
`public inline virtual  `[`~CIterativeMachine`](#classshogun_1_1CIterativeMachine_1ae54f84a0ca746267b17a6a345169bfc3)`()` | 
`public inline bool `[`is_complete`](#classshogun_1_1CIterativeMachine_1aa942bb8ca5855ff1669c3928c839057e)`()` | Returns convergence status
`public inline virtual bool `[`continue_train`](#classshogun_1_1CIterativeMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` | 
`protected int32_t `[`m_max_iterations`](#classshogun_1_1CIterativeMachine_1ac4164d18d68598ffa30f36532536695a) | Maximum Iterations
`protected int32_t `[`m_current_iteration`](#classshogun_1_1CIterativeMachine_1a027a4b08c17ed34c63c285e8e6f18421) | Current iteration of training loop
`protected bool `[`m_complete`](#classshogun_1_1CIterativeMachine_1a6a2f1510670741e97257d8f221ba92d7) | Completion status
`protected inline virtual bool `[`train_machine`](#classshogun_1_1CIterativeMachine_1acff88580df5439ae7154299f7c743b73)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | 
`protected void `[`iteration`](#classshogun_1_1CIterativeMachine_1ac2299a1610f0b821c6cecb988ed66036)`()` | To be overloaded by sublcasses to implement custom single iterations of training loop.
`protected void `[`init_model`](#classshogun_1_1CIterativeMachine_1a039e10aee62b44f5cc199584f65105e2)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` | To be overloaded in subclasses to initialize the model for training
`protected inline virtual void `[`end_training`](#classshogun_1_1CIterativeMachine_1adc0e7c7291884fb46bc4456038477cc7)`()` | Can be overloaded in subclasses to show more information and/or clean up states

## Members

#### `public inline  `[`CIterativeMachine`](#classshogun_1_1CIterativeMachine_1a8bbd5914ed48c23775ed43571477f77e)`()` {#classshogun_1_1CIterativeMachine_1a8bbd5914ed48c23775ed43571477f77e}

Default constructor

#### `public inline virtual  `[`~CIterativeMachine`](#classshogun_1_1CIterativeMachine_1ae54f84a0ca746267b17a6a345169bfc3)`()` {#classshogun_1_1CIterativeMachine_1ae54f84a0ca746267b17a6a345169bfc3}

#### `public inline bool `[`is_complete`](#classshogun_1_1CIterativeMachine_1aa942bb8ca5855ff1669c3928c839057e)`()` {#classshogun_1_1CIterativeMachine_1aa942bb8ca5855ff1669c3928c839057e}

Returns convergence status

#### `public inline virtual bool `[`continue_train`](#classshogun_1_1CIterativeMachine_1a0d918d8b628c91f0c22f2a623b495812)`()` {#classshogun_1_1CIterativeMachine_1a0d918d8b628c91f0c22f2a623b495812}

#### `protected int32_t `[`m_max_iterations`](#classshogun_1_1CIterativeMachine_1ac4164d18d68598ffa30f36532536695a) {#classshogun_1_1CIterativeMachine_1ac4164d18d68598ffa30f36532536695a}

Maximum Iterations

#### `protected int32_t `[`m_current_iteration`](#classshogun_1_1CIterativeMachine_1a027a4b08c17ed34c63c285e8e6f18421) {#classshogun_1_1CIterativeMachine_1a027a4b08c17ed34c63c285e8e6f18421}

Current iteration of training loop

#### `protected bool `[`m_complete`](#classshogun_1_1CIterativeMachine_1a6a2f1510670741e97257d8f221ba92d7) {#classshogun_1_1CIterativeMachine_1a6a2f1510670741e97257d8f221ba92d7}

Completion status

#### `protected inline virtual bool `[`train_machine`](#classshogun_1_1CIterativeMachine_1acff88580df5439ae7154299f7c743b73)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CIterativeMachine_1acff88580df5439ae7154299f7c743b73}

#### `protected void `[`iteration`](#classshogun_1_1CIterativeMachine_1ac2299a1610f0b821c6cecb988ed66036)`()` {#classshogun_1_1CIterativeMachine_1ac2299a1610f0b821c6cecb988ed66036}

To be overloaded by sublcasses to implement custom single iterations of training loop.

#### `protected void `[`init_model`](#classshogun_1_1CIterativeMachine_1a039e10aee62b44f5cc199584f65105e2)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * data)` {#classshogun_1_1CIterativeMachine_1a039e10aee62b44f5cc199584f65105e2}

To be overloaded in subclasses to initialize the model for training

#### `protected inline virtual void `[`end_training`](#classshogun_1_1CIterativeMachine_1adc0e7c7291884fb46bc4456038477cc7)`()` {#classshogun_1_1CIterativeMachine_1adc0e7c7291884fb46bc4456038477cc7}

Can be overloaded in subclasses to show more information and/or clean up states

