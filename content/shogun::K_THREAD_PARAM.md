---
classname: "shogun::K_THREAD_PARAM"
type: "struct"
---

# struct `shogun::K_THREAD_PARAM` {#structshogun_1_1K__THREAD__PARAM}

kernel thread parameters

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`CKernel`](#classshogun_1_1CKernel)` * `[`kernel`](#structshogun_1_1K__THREAD__PARAM_1a4065c466d501ac67871c0f79e37b648a) | kernel
`public int32_t `[`start`](#structshogun_1_1K__THREAD__PARAM_1adcc785ba5ec45d3748f1f666744d18e0) | start (unit row)
`public int32_t `[`end`](#structshogun_1_1K__THREAD__PARAM_1aca3605df056ce6ed54953f8bf803862f) | end (unit row)
`public int64_t `[`total_start`](#structshogun_1_1K__THREAD__PARAM_1a163459d0ed5afe422bc8ca475cb5c162) | start (unit number of elements)
`public int32_t `[`m`](#structshogun_1_1K__THREAD__PARAM_1a2a026ba1ee4c03db17e04d7bd0f60975) | m
`public int32_t `[`n`](#structshogun_1_1K__THREAD__PARAM_1a4e34aefb3cc5403a07c020131077100a) | n
`public T * `[`result`](#structshogun_1_1K__THREAD__PARAM_1a3b79f7194220808c43539b3644bb63f7) | result
`public bool `[`symmetric`](#structshogun_1_1K__THREAD__PARAM_1a00729cbf099b7095d2af82e297fb2206) | kernel matrix k(i,j)=k(j,i)
`public bool `[`verbose`](#structshogun_1_1K__THREAD__PARAM_1ab3f078684998b83967d507d0f453f454) | output progress
`public `[`PRange`](#classshogun_1_1PRange)`< int64_t > * `[`pb`](#structshogun_1_1K__THREAD__PARAM_1a6658232cea0f6e2051904a4dab3b4ac6) | 

## Members

#### `public `[`CKernel`](#classshogun_1_1CKernel)` * `[`kernel`](#structshogun_1_1K__THREAD__PARAM_1a4065c466d501ac67871c0f79e37b648a) {#structshogun_1_1K__THREAD__PARAM_1a4065c466d501ac67871c0f79e37b648a}

kernel

#### `public int32_t `[`start`](#structshogun_1_1K__THREAD__PARAM_1adcc785ba5ec45d3748f1f666744d18e0) {#structshogun_1_1K__THREAD__PARAM_1adcc785ba5ec45d3748f1f666744d18e0}

start (unit row)

#### `public int32_t `[`end`](#structshogun_1_1K__THREAD__PARAM_1aca3605df056ce6ed54953f8bf803862f) {#structshogun_1_1K__THREAD__PARAM_1aca3605df056ce6ed54953f8bf803862f}

end (unit row)

#### `public int64_t `[`total_start`](#structshogun_1_1K__THREAD__PARAM_1a163459d0ed5afe422bc8ca475cb5c162) {#structshogun_1_1K__THREAD__PARAM_1a163459d0ed5afe422bc8ca475cb5c162}

start (unit number of elements)

#### `public int32_t `[`m`](#structshogun_1_1K__THREAD__PARAM_1a2a026ba1ee4c03db17e04d7bd0f60975) {#structshogun_1_1K__THREAD__PARAM_1a2a026ba1ee4c03db17e04d7bd0f60975}

m

#### `public int32_t `[`n`](#structshogun_1_1K__THREAD__PARAM_1a4e34aefb3cc5403a07c020131077100a) {#structshogun_1_1K__THREAD__PARAM_1a4e34aefb3cc5403a07c020131077100a}

n

#### `public T * `[`result`](#structshogun_1_1K__THREAD__PARAM_1a3b79f7194220808c43539b3644bb63f7) {#structshogun_1_1K__THREAD__PARAM_1a3b79f7194220808c43539b3644bb63f7}

result

#### `public bool `[`symmetric`](#structshogun_1_1K__THREAD__PARAM_1a00729cbf099b7095d2af82e297fb2206) {#structshogun_1_1K__THREAD__PARAM_1a00729cbf099b7095d2af82e297fb2206}

kernel matrix k(i,j)=k(j,i)

#### `public bool `[`verbose`](#structshogun_1_1K__THREAD__PARAM_1ab3f078684998b83967d507d0f453f454) {#structshogun_1_1K__THREAD__PARAM_1ab3f078684998b83967d507d0f453f454}

output progress

#### `public `[`PRange`](#classshogun_1_1PRange)`< int64_t > * `[`pb`](#structshogun_1_1K__THREAD__PARAM_1a6658232cea0f6e2051904a4dab3b4ac6) {#structshogun_1_1K__THREAD__PARAM_1a6658232cea0f6e2051904a4dab3b4ac6}

