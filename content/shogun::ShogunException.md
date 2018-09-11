---
classname: "shogun::ShogunException"
type: "class"
parents:
   - exception
---

# class `shogun::ShogunException` {#classshogun_1_1ShogunException}

```
class shogun::ShogunException
  : public exception
```

Class [ShogunException](#classshogun_1_1ShogunException) defines an exception which is thrown whenever an error inside of shogun occurs.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  explicit `[`ShogunException`](#classshogun_1_1ShogunException_1ac00af3e7d53532b0c7c97983903fde09)`(const std::string & what_arg)` | constructor
`public  explicit `[`ShogunException`](#classshogun_1_1ShogunException_1acb23d4ba1e9d9013463bea0633e9111e)`(const char * what_arg)` | constructor
`public  `[`ShogunException`](#classshogun_1_1ShogunException_1a32fd6242ead810a428d2b9163ed16ef2)`(const `[`ShogunException`](#classshogun_1_1ShogunException)` & orig)` | copy constructor
`public virtual  `[`~ShogunException`](#classshogun_1_1ShogunException_1ad26afc9c2ffb21f5a092409820d12154)`()` | destructor
`public virtual const char * `[`what`](#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70)`() const` | 

## Members

#### `public  explicit `[`ShogunException`](#classshogun_1_1ShogunException_1ac00af3e7d53532b0c7c97983903fde09)`(const std::string & what_arg)` {#classshogun_1_1ShogunException_1ac00af3e7d53532b0c7c97983903fde09}

constructor

#### Parameters
* `str` exception string

#### `public  explicit `[`ShogunException`](#classshogun_1_1ShogunException_1acb23d4ba1e9d9013463bea0633e9111e)`(const char * what_arg)` {#classshogun_1_1ShogunException_1acb23d4ba1e9d9013463bea0633e9111e}

constructor

#### Parameters
* `str` exception string

#### `public  `[`ShogunException`](#classshogun_1_1ShogunException_1a32fd6242ead810a428d2b9163ed16ef2)`(const `[`ShogunException`](#classshogun_1_1ShogunException)` & orig)` {#classshogun_1_1ShogunException_1a32fd6242ead810a428d2b9163ed16ef2}

copy constructor

#### Parameters
* `orig` source object

#### `public virtual  `[`~ShogunException`](#classshogun_1_1ShogunException_1ad26afc9c2ffb21f5a092409820d12154)`()` {#classshogun_1_1ShogunException_1ad26afc9c2ffb21f5a092409820d12154}

destructor

#### `public virtual const char * `[`what`](#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70)`() const` {#classshogun_1_1ShogunException_1abf843cbb29dec939d0731e491bab6f70}

