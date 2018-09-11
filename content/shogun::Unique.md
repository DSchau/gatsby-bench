---
classname: "shogun::Unique"
type: "class"
---

# class `shogun::Unique` {#classshogun_1_1Unique}

Holds unique pointer that is deleted once this holder is deleted. Its main usage is to hold a pointer to implementation (pimpl idiom):

class Self; Unique<Self> self;

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  `[`Unique`](#classshogun_1_1Unique_1a02a6188a4357f4010ab5db2d663a7803)`()` | Creates an instance of something unique.
`public inline  `[`~Unique`](#classshogun_1_1Unique_1af90f6aa07fa9825ba4b49086286c42af)`()` | 
`public  `[`Unique`](#classshogun_1_1Unique_1aa3635d72c2e3c4e4cde65bfd42c79ede)`(const `[`Unique`](#classshogun_1_1Unique)` &)` | Not implemented copy constructor
`public `[`Unique`](#classshogun_1_1Unique)` & `[`operator=`](#classshogun_1_1Unique_1a6b32e2dfb32e64e77cf9ec654b7f8652)`(const `[`Unique`](#classshogun_1_1Unique)` & other)` | Not implemented assignment operator
`public inline T * `[`operator->`](#classshogun_1_1Unique_1a5c1735ebb61cb9b40f6d0ed30be8a288)`() const` | Access underlying unique object as a raw pointer

## Members

#### `public inline  `[`Unique`](#classshogun_1_1Unique_1a02a6188a4357f4010ab5db2d663a7803)`()` {#classshogun_1_1Unique_1a02a6188a4357f4010ab5db2d663a7803}

Creates an instance of something unique.

Calls default constructor of type T.

#### `public inline  `[`~Unique`](#classshogun_1_1Unique_1af90f6aa07fa9825ba4b49086286c42af)`()` {#classshogun_1_1Unique_1af90f6aa07fa9825ba4b49086286c42af}

#### `public  `[`Unique`](#classshogun_1_1Unique_1aa3635d72c2e3c4e4cde65bfd42c79ede)`(const `[`Unique`](#classshogun_1_1Unique)` &)` {#classshogun_1_1Unique_1aa3635d72c2e3c4e4cde65bfd42c79ede}

Not implemented copy constructor

#### `public `[`Unique`](#classshogun_1_1Unique)` & `[`operator=`](#classshogun_1_1Unique_1a6b32e2dfb32e64e77cf9ec654b7f8652)`(const `[`Unique`](#classshogun_1_1Unique)` & other)` {#classshogun_1_1Unique_1a6b32e2dfb32e64e77cf9ec654b7f8652}

Not implemented assignment operator

#### `public inline T * `[`operator->`](#classshogun_1_1Unique_1a5c1735ebb61cb9b40f6d0ed30be8a288)`() const` {#classshogun_1_1Unique_1a5c1735ebb61cb9b40f6d0ed30be8a288}

Access underlying unique object as a raw pointer

