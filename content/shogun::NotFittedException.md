---
classname: "shogun::NotFittedException"
type: "class"
parents:
   - ShogunException
---

# class `shogun::NotFittedException` {#classshogun_1_1NotFittedException}

```
class shogun::NotFittedException
  : public ShogunException
```

Class [NotFittedException](#classshogun_1_1NotFittedException) defines an exception which is thrown whenever a machine or a transformer in [Shogun](#classShogun) used but haven't be fitted.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  explicit `[`NotFittedException`](#classshogun_1_1NotFittedException_1a23f100039b47a8978af9635732931c08)`(const std::string & what_arg)` | constructor
`public inline  explicit `[`NotFittedException`](#classshogun_1_1NotFittedException_1a911bf2045829e61265ccb928b69393e8)`(const char * what_arg)` | constructor
`public virtual const char * `[`what`](#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70)`() const` | 

## Members

#### `public inline  explicit `[`NotFittedException`](#classshogun_1_1NotFittedException_1a23f100039b47a8978af9635732931c08)`(const std::string & what_arg)` {#classshogun_1_1NotFittedException_1a23f100039b47a8978af9635732931c08}

constructor

#### Parameters
* `str` exception string

#### `public inline  explicit `[`NotFittedException`](#classshogun_1_1NotFittedException_1a911bf2045829e61265ccb928b69393e8)`(const char * what_arg)` {#classshogun_1_1NotFittedException_1a911bf2045829e61265ccb928b69393e8}

constructor

#### Parameters
* `str` exception string

#### `public virtual const char * `[`what`](#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70)`() const` {#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70}

