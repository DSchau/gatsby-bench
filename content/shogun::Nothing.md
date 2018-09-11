---
classname: "shogun::Nothing"
type: "class"
---

# class `shogun::Nothing` {#classshogun_1_1Nothing}

Represents non-typed absent value.

Can be casted to any 
**See also**: Maybe<T> resulting in [Maybe](#classshogun_1_1Maybe) with absent value.

Contains reason for absence as a regular C string.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public const char * `[`m_absence_reason`](#classshogun_1_1Nothing_1abba9fc307ca09db2bdf9a467910b6161) | Represents a reason why something is absent. Memory is not managed.
`public inline  `[`Nothing`](#classshogun_1_1Nothing_1a04647b4bb1df49b586ba7c593b60d471)`(const char * reason)` | Createst an instance of nothing aka absent value.
`public inline  `[`Nothing`](#classshogun_1_1Nothing_1a96db52b919c374be04dbd65c85a68972)`(const `[`Nothing`](#classshogun_1_1Nothing)` & other)` | Copies nothing from nothing, inheriting absence reason.

## Members

#### `public const char * `[`m_absence_reason`](#classshogun_1_1Nothing_1abba9fc307ca09db2bdf9a467910b6161) {#classshogun_1_1Nothing_1abba9fc307ca09db2bdf9a467910b6161}

Represents a reason why something is absent. Memory is not managed.

#### `public inline  `[`Nothing`](#classshogun_1_1Nothing_1a04647b4bb1df49b586ba7c593b60d471)`(const char * reason)` {#classshogun_1_1Nothing_1a04647b4bb1df49b586ba7c593b60d471}

Createst an instance of nothing aka absent value.

#### Parameters
* `reason` the reason something is absent

#### `public inline  `[`Nothing`](#classshogun_1_1Nothing_1a96db52b919c374be04dbd65c85a68972)`(const `[`Nothing`](#classshogun_1_1Nothing)` & other)` {#classshogun_1_1Nothing_1a96db52b919c374be04dbd65c85a68972}

Copies nothing from nothing, inheriting absence reason.

#### Parameters
* `other` other instance of nothing

