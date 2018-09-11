---
classname: "shogun::Maybe"
type: "class"
---

# class `shogun::Maybe` {#classshogun_1_1Maybe}

Holder that represents an object that can be either present or absent. Quite simllar to std::optional introduced in C++14, but provides a way to pass the reason of absence (e.g. "incorrect parameter").

Essentially, instances are created via 
**See also**: [Just](#classshogun_1_1Maybe_1a30eeb133bed1815573e24bc73b8a6516) or 

**See also**: [Nothing](#classshogun_1_1Nothing)

```cpp
Maybe<int> absent_value = Nothing();
Maybe<int> present_value = Just(3);
```

To check whether value is present, regular implicit cast to bool is used:

```cpp
if (maybe_value)
{
    // value exists!
}
else
{
    // value doesn't exist!
}
```

To obtain value, 
**See also**: [value](#classshogun_1_1Maybe_1a464298ad7afeafebbb149f566ecabbab) is used:

```cpp
// may throw an exception
int value = unreliable.value();
```

To provide default values, 
**See also**: [value_or](#classshogun_1_1Maybe_1a784b1e1b9c46169e030e8d5d24f34a46) is used:

```cpp
int value = unreliable.value_or(9);
```

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`Maybe`](#classshogun_1_1Maybe_1af182a419686a74b35c5e689f168b886d)`(const `[`Nothing`](#classshogun_1_1Nothing)` & nothing)` | Creates an instance from nothing resulting in absent value.
`public inline  `[`Maybe`](#classshogun_1_1Maybe_1a593a39dc4cabe121d0b292edb2891b8b)`(const `[`Maybe`](#classshogun_1_1Maybe)`< T > & other)` | Copy constructor.
`public inline  `[`operator bool`](#classshogun_1_1Maybe_1a67b76affb3b5d35fa419ac234144038b)`() const` | Evaluates to true when object is present, false otherwise.
`public inline T & `[`value`](#classshogun_1_1Maybe_1a464298ad7afeafebbb149f566ecabbab)`()` | Returns value if it is present, fails otherwise.
`public inline T & `[`value_or`](#classshogun_1_1Maybe_1a784b1e1b9c46169e030e8d5d24f34a46)`(T & v)` | Returns value if it is present, or the provided default value.
`public inline bool `[`is_absent`](#classshogun_1_1Maybe_1a8945a836c59f9fca1f1a8b26977886c6)`() const` | Returns true if value is absent, false otherwise.
`public inline bool `[`is_present`](#classshogun_1_1Maybe_1a938f26ad0fcaddf2860be786ee3d793b)`() const` | Returns true if value is present, false otherwise.

## Members

#### `public inline  `[`Maybe`](#classshogun_1_1Maybe_1af182a419686a74b35c5e689f168b886d)`(const `[`Nothing`](#classshogun_1_1Nothing)` & nothing)` {#classshogun_1_1Maybe_1af182a419686a74b35c5e689f168b886d}

Creates an instance from nothing resulting in absent value.

#### Parameters
* `nothing` instance of nothing

#### `public inline  `[`Maybe`](#classshogun_1_1Maybe_1a593a39dc4cabe121d0b292edb2891b8b)`(const `[`Maybe`](#classshogun_1_1Maybe)`< T > & other)` {#classshogun_1_1Maybe_1a593a39dc4cabe121d0b292edb2891b8b}

Copy constructor.

#### Parameters
* `other` other instance of [Maybe](#classshogun_1_1Maybe) for the same type

#### `public inline  `[`operator bool`](#classshogun_1_1Maybe_1a67b76affb3b5d35fa419ac234144038b)`() const` {#classshogun_1_1Maybe_1a67b76affb3b5d35fa419ac234144038b}

Evaluates to true when object is present, false otherwise.

Equivalent to 
**See also**: [is_present()](#classshogun_1_1Maybe_1a938f26ad0fcaddf2860be786ee3d793b)

#### `public inline T & `[`value`](#classshogun_1_1Maybe_1a464298ad7afeafebbb149f566ecabbab)`()` {#classshogun_1_1Maybe_1a464298ad7afeafebbb149f566ecabbab}

Returns value if it is present, fails otherwise.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` if retrieved value is absent

#### `public inline T & `[`value_or`](#classshogun_1_1Maybe_1a784b1e1b9c46169e030e8d5d24f34a46)`(T & v)` {#classshogun_1_1Maybe_1a784b1e1b9c46169e030e8d5d24f34a46}

Returns value if it is present, or the provided default value.

Doesn't throw any exception.

#### `public inline bool `[`is_absent`](#classshogun_1_1Maybe_1a8945a836c59f9fca1f1a8b26977886c6)`() const` {#classshogun_1_1Maybe_1a8945a836c59f9fca1f1a8b26977886c6}

Returns true if value is absent, false otherwise.

Doesn't throw any exception.

#### `public inline bool `[`is_present`](#classshogun_1_1Maybe_1a938f26ad0fcaddf2860be786ee3d793b)`() const` {#classshogun_1_1Maybe_1a938f26ad0fcaddf2860be786ee3d793b}

Returns true if value is present, false otherwise.

Doesn't throw any exception.

