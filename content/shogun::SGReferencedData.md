---
classname: "shogun::SGReferencedData"
type: "class"
---

# class `shogun::SGReferencedData` {#classshogun_1_1SGReferencedData}

shogun reference count managed data

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`SGReferencedData`](#classshogun_1_1SGReferencedData_1a251c16e01c08c9e3a404305614167fe5)`(bool ref_counting)` | default constructor
`public  `[`SGReferencedData`](#classshogun_1_1SGReferencedData_1a7ec749b31069f16d7911cc73e0312f50)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy constructor
`public `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & `[`operator=`](#classshogun_1_1SGReferencedData_1ac08e52d159b98eed3fc40505a4f69e09)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | override assignment operator to increase refcount on assignments
`public virtual  `[`~SGReferencedData`](#classshogun_1_1SGReferencedData_1ab5870798f7d324e9b61fe57215957c3f)`()` | empty destructor
`public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | copy refcount
`protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`protected void `[`copy_data`](#classshogun_1_1SGReferencedData_1a70b54faf04d4496ca809546cc4df8d50)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` | needs to be overridden to copy data
`protected void `[`init_data`](#classshogun_1_1SGReferencedData_1afb75308572a7352e429516247a1e52d4)`()` | needs to be overridden to initialize empty data
`protected void `[`free_data`](#classshogun_1_1SGReferencedData_1ab12b730eab4bf9f3119816242d6dbbf5)`()` | needs to be overridden to free data

## Members

#### `public  `[`SGReferencedData`](#classshogun_1_1SGReferencedData_1a251c16e01c08c9e3a404305614167fe5)`(bool ref_counting)` {#classshogun_1_1SGReferencedData_1a251c16e01c08c9e3a404305614167fe5}

default constructor

#### `public  `[`SGReferencedData`](#classshogun_1_1SGReferencedData_1a7ec749b31069f16d7911cc73e0312f50)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGReferencedData_1a7ec749b31069f16d7911cc73e0312f50}

copy constructor

#### `public `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & `[`operator=`](#classshogun_1_1SGReferencedData_1ac08e52d159b98eed3fc40505a4f69e09)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGReferencedData_1ac08e52d159b98eed3fc40505a4f69e09}

override assignment operator to increase refcount on assignments

#### `public virtual  `[`~SGReferencedData`](#classshogun_1_1SGReferencedData_1ab5870798f7d324e9b61fe57215957c3f)`()` {#classshogun_1_1SGReferencedData_1ab5870798f7d324e9b61fe57215957c3f}

empty destructor

NOTE: [unref()](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01) has to be called in derived classes to avoid memory leaks.

#### `public int32_t `[`ref_count`](#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1SGReferencedData_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `protected void `[`copy_refcount`](#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGReferencedData_1a253175a13e8af17d4f2a2cfd9e14dd63}

copy refcount

#### `protected int32_t `[`ref`](#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1SGReferencedData_1ab8c24b912ee57d3f2c81ecccd083582a}

increase reference counter

#### Returns
reference count

#### `protected int32_t `[`unref`](#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1SGReferencedData_1ad99bde1a142a1c07a963169123166e01}

decrement reference counter and deallocate object if refcount is zero before or after decrementing it

#### Returns
reference count

#### `protected void `[`copy_data`](#classshogun_1_1SGReferencedData_1a70b54faf04d4496ca809546cc4df8d50)`(const `[`SGReferencedData`](#classshogun_1_1SGReferencedData)` & orig)` {#classshogun_1_1SGReferencedData_1a70b54faf04d4496ca809546cc4df8d50}

needs to be overridden to copy data

#### `protected void `[`init_data`](#classshogun_1_1SGReferencedData_1afb75308572a7352e429516247a1e52d4)`()` {#classshogun_1_1SGReferencedData_1afb75308572a7352e429516247a1e52d4}

needs to be overridden to initialize empty data

#### `protected void `[`free_data`](#classshogun_1_1SGReferencedData_1ab12b730eab4bf9f3119816242d6dbbf5)`()` {#classshogun_1_1SGReferencedData_1ab12b730eab4bf9f3119816242d6dbbf5}

needs to be overridden to free data

