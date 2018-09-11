---
classname: "shogun::Range"
type: "class"
---

# class `shogun::Range` {#classshogun_1_1Range}

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`Range`](#classshogun_1_1Range_1a35ed024345fc207ba5a19a109a076b83)`(T rbegin,T rend)` | Creates range with specified bounds. Assumes rbegin < rend.
`public inline `[`Iterator`](#classshogun_1_1Range_1_1Iterator)` `[`begin`](#classshogun_1_1Range_1a09dd208593b9721a30a83ed978ede577)`() const` | Create iterator that corresponds to the start of range.
`public inline `[`Iterator`](#classshogun_1_1Range_1_1Iterator)` `[`end`](#classshogun_1_1Range_1a62469461ed7c932afba3808f4da0fe3d)`() const` | Create iterator that corresponds to the end of range.

## Members

#### `public inline  `[`Range`](#classshogun_1_1Range_1a35ed024345fc207ba5a19a109a076b83)`(T rbegin,T rend)` {#classshogun_1_1Range_1a35ed024345fc207ba5a19a109a076b83}

Creates range with specified bounds. Assumes rbegin < rend.

#### Parameters
* `rbegin` lower bound of range 

* `rend` upper bound of range (excluding)

#### `public inline `[`Iterator`](#classshogun_1_1Range_1_1Iterator)` `[`begin`](#classshogun_1_1Range_1a09dd208593b9721a30a83ed978ede577)`() const` {#classshogun_1_1Range_1a09dd208593b9721a30a83ed978ede577}

Create iterator that corresponds to the start of range.

Usually called through for-loop syntax.

#### `public inline `[`Iterator`](#classshogun_1_1Range_1_1Iterator)` `[`end`](#classshogun_1_1Range_1a62469461ed7c932afba3808f4da0fe3d)`() const` {#classshogun_1_1Range_1a62469461ed7c932afba3808f4da0fe3d}

Create iterator that corresponds to the end of range.

Usually called through for-loop syntax.

