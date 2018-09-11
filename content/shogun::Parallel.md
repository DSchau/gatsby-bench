---
classname: "shogun::Parallel"
type: "class"
---

# class `shogun::Parallel` {#classshogun_1_1Parallel}

Class [Parallel](#classshogun_1_1Parallel) provides helper functions for multithreading.

For example it can be used to determine the number of CPU cores in your computer and is the place where you define the number of CPUs that shall be used in computations.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  `[`Parallel`](#classshogun_1_1Parallel_1a60e1ff1a24337322472f11d7d6f366ba)`()` | constructor
`public  `[`Parallel`](#classshogun_1_1Parallel_1a39224cb3de9964c60a61cb061ed90f4b)`(const `[`Parallel`](#classshogun_1_1Parallel)` & orig)` | copy constructor
`public virtual  `[`~Parallel`](#classshogun_1_1Parallel_1a5eb93067222b2d952d53994e600758eb)`()` | destructor
`public int32_t `[`get_num_cpus`](#classshogun_1_1Parallel_1a9c928640d6465cd8ab2a6b040a6817d1)`() const` | get num of cpus 
`public void `[`set_num_threads`](#classshogun_1_1Parallel_1a20e0024afa2d89614db967d0b546ee32)`(int32_t n)` | set number of threads 
`public int32_t `[`get_num_threads`](#classshogun_1_1Parallel_1a40a8da077bf8ccdd8fb6cba1cfbc2ec1)`() const` | get number of threads 
`public int32_t `[`ref`](#classshogun_1_1Parallel_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | ref 
`public int32_t `[`ref_count`](#classshogun_1_1Parallel_1a7682f1bc33b51f8f0b9340c6f4df4237)`() const` | get ref count 
`public int32_t `[`unref`](#classshogun_1_1Parallel_1ad99bde1a142a1c07a963169123166e01)`()` | unref 

## Members

#### `public  `[`Parallel`](#classshogun_1_1Parallel_1a60e1ff1a24337322472f11d7d6f366ba)`()` {#classshogun_1_1Parallel_1a60e1ff1a24337322472f11d7d6f366ba}

constructor

#### `public  `[`Parallel`](#classshogun_1_1Parallel_1a39224cb3de9964c60a61cb061ed90f4b)`(const `[`Parallel`](#classshogun_1_1Parallel)` & orig)` {#classshogun_1_1Parallel_1a39224cb3de9964c60a61cb061ed90f4b}

copy constructor

#### `public virtual  `[`~Parallel`](#classshogun_1_1Parallel_1a5eb93067222b2d952d53994e600758eb)`()` {#classshogun_1_1Parallel_1a5eb93067222b2d952d53994e600758eb}

destructor

#### `public int32_t `[`get_num_cpus`](#classshogun_1_1Parallel_1a9c928640d6465cd8ab2a6b040a6817d1)`() const` {#classshogun_1_1Parallel_1a9c928640d6465cd8ab2a6b040a6817d1}

get num of cpus 
#### Returns
number of CPUs

#### `public void `[`set_num_threads`](#classshogun_1_1Parallel_1a20e0024afa2d89614db967d0b546ee32)`(int32_t n)` {#classshogun_1_1Parallel_1a20e0024afa2d89614db967d0b546ee32}

set number of threads 
#### Parameters
* `n` number of threads

#### `public int32_t `[`get_num_threads`](#classshogun_1_1Parallel_1a40a8da077bf8ccdd8fb6cba1cfbc2ec1)`() const` {#classshogun_1_1Parallel_1a40a8da077bf8ccdd8fb6cba1cfbc2ec1}

get number of threads 
#### Returns
number of threads

#### `public int32_t `[`ref`](#classshogun_1_1Parallel_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1Parallel_1ab8c24b912ee57d3f2c81ecccd083582a}

ref 
#### Returns
current ref counter

#### `public int32_t `[`ref_count`](#classshogun_1_1Parallel_1a7682f1bc33b51f8f0b9340c6f4df4237)`() const` {#classshogun_1_1Parallel_1a7682f1bc33b51f8f0b9340c6f4df4237}

get ref count 
#### Returns
current ref counter

#### `public int32_t `[`unref`](#classshogun_1_1Parallel_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1Parallel_1ad99bde1a142a1c07a963169123166e01}

unref 
#### Returns
current ref counter

