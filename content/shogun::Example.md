---
classname: "shogun::Example"
type: "class"
---

# class `shogun::Example` {#classshogun_1_1Example}

Class [Example](#classshogun_1_1Example) is the container type for the vector+label combination.

The vector is stored as an SGVector<T>, and the label is a float64_t.

Objects of this type are stored in the ring of class [CParseBuffer](#classshogun_1_1CParseBuffer).

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`label`](#classshogun_1_1Example_1ac3e8f638676b6f4449dee4e8407d8487) | Label.
`public T * `[`fv`](#classshogun_1_1Example_1a40d86e7ce2ff5215cc23508d0d4305dd) | Feature vector of type T.
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`length`](#classshogun_1_1Example_1a1e4cc81ff0b3102f12e93b4db7e1665b) | 

## Members

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`label`](#classshogun_1_1Example_1ac3e8f638676b6f4449dee4e8407d8487) {#classshogun_1_1Example_1ac3e8f638676b6f4449dee4e8407d8487}

Label.

#### `public T * `[`fv`](#classshogun_1_1Example_1a40d86e7ce2ff5215cc23508d0d4305dd) {#classshogun_1_1Example_1a40d86e7ce2ff5215cc23508d0d4305dd}

Feature vector of type T.

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`length`](#classshogun_1_1Example_1a1e4cc81ff0b3102f12e93b4db7e1665b) {#classshogun_1_1Example_1a1e4cc81ff0b3102f12e93b4db7e1665b}

