---
classname: "shogun::InvalidStateException"
type: "class"
parents:
   - ShogunException
---

# class `shogun::InvalidStateException` {#classshogun_1_1InvalidStateException}

```
class shogun::InvalidStateException
  : public ShogunException
```

Class [InvalidStateException](#classshogun_1_1InvalidStateException) defines an exception which is thrown whenever an object in [Shogun](#classShogun) in invalid state is used.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public inline  explicit `[`InvalidStateException`](#classshogun_1_1InvalidStateException_1ad99eea6e41d0410995b0044dea6fc4ef)`(const std::string & what_arg)` | constructor
`public inline  explicit `[`InvalidStateException`](#classshogun_1_1InvalidStateException_1abfd3d796fbdd3a2e4231ac9527b93af4)`(const char * what_arg)` | constructor
`public virtual const char * `[`what`](#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70)`() const` | 

## Members

#### `public inline  explicit `[`InvalidStateException`](#classshogun_1_1InvalidStateException_1ad99eea6e41d0410995b0044dea6fc4ef)`(const std::string & what_arg)` {#classshogun_1_1InvalidStateException_1ad99eea6e41d0410995b0044dea6fc4ef}

constructor

#### Parameters
* `str` exception string

#### `public inline  explicit `[`InvalidStateException`](#classshogun_1_1InvalidStateException_1abfd3d796fbdd3a2e4231ac9527b93af4)`(const char * what_arg)` {#classshogun_1_1InvalidStateException_1abfd3d796fbdd3a2e4231ac9527b93af4}

constructor

#### Parameters
* `str` exception string

#### `public virtual const char * `[`what`](#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70)`() const` {#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70}

