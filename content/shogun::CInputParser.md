---
classname: "shogun::CInputParser"
type: "class"
---

# class `shogun::CInputParser` {#classshogun_1_1CInputParser}

Class [CInputParser](#classshogun_1_1CInputParser) is a templated class used to maintain the reading/parsing/providing of examples.

Parsing is done in a thread separate from the learner.

Note that parsing is not done directly by this class, but by the Streaming*File classes. This class only calls the required get_vector* functions from the StreamingFile object. (Exactly which function should be called is set through the set_read_vector* functions)

The template type should be the type of feature vector the parser should return. Eg. [CInputParser<float32_t>](#classshogun_1_1CInputParser) means it will expect a float32_t* vector to be returned from the get_vector function. Other parameters returned are length of feature vector and the label, if applicable.

If the vectors cannot be directly represented as say float32_t* one can instantiate eg. CInputParser<VwExample> and it looks for a get_vector function which returns a VwExample, which may contain any kind of data, including label, vector, weights, etc. It is then up to the external algorithm to handle such objects.

The parser should first be started with a call to the [start_parser()](#classshogun_1_1CInputParser_1add2dbd5435810c2243f18502c09b3815) function which starts a new thread for continuous parsing of examples.

Parsing is done through the [CParseBuffer](#classshogun_1_1CParseBuffer) object, which in its current implementation is a ring of a specified number of examples. It is the task of the [CInputParser](#classshogun_1_1CInputParser) object to ensure that this ring is being updated with new parsed examples.

[CInputParser](#classshogun_1_1CInputParser) provides mainly the get_next_example function which returns the next example from the [CParseBuffer](#classshogun_1_1CParseBuffer) object to the caller (usually a StreamingFeatures object). When one is done using the example, [finalize_example()](#classshogun_1_1CInputParser_1aea04cc7c5c7207e26a4616932a1f7121) should be called, leaving the spot free for a new example to be loaded.

The parsing thread should be joined with a call to [end_parser()](#classshogun_1_1CInputParser_1abe675af9c171a8bc0cecd7db93bd477e). [exit_parser()](#classshogun_1_1CInputParser_1a64acdb31d2a0d299d9b484eec4cb0d29) may be used to cancel the parse thread if needed.

Options are provided for automatic SG_FREEing of example objects after each [finalize_example()](#classshogun_1_1CInputParser_1aea04cc7c5c7207e26a4616932a1f7121) and also on [CInputParser](#classshogun_1_1CInputParser) destruction. They are set through the set_free_vector* functions. Do not free vectors on [finalize_example()](#classshogun_1_1CInputParser_1aea04cc7c5c7207e26a4616932a1f7121) if you intend to reuse the same vector memory locations for different examples. Do not free vectors on destruction if you are bound to free them manually later.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public bool `[`parsing_done`](#classshogun_1_1CInputParser_1ad468303bfb3ed5725a023a81b2bba331) | true if all input is parsed
`public bool `[`reading_done`](#classshogun_1_1CInputParser_1afcb198504c85035b753a5ed2563c8646) | true if all examples are fetched
`public `[`E_EXAMPLE_TYPE`](#namespaceshogun_1ae875449f4a4a39610d61f785132aadeb)` `[`example_type`](#classshogun_1_1CInputParser_1aef0c79ba1132b2151ef0ccce56cf110a) | LABELLED or UNLABELLED
`public  `[`CInputParser`](#classshogun_1_1CInputParser_1ad91e5e5f85c1113ffbd0d94852f86184)`()` | Constructor
`public  `[`~CInputParser`](#classshogun_1_1CInputParser_1ab6ade70a434e26fe7f23e400194e8d84)`()` | Destructor
`public void `[`init`](#classshogun_1_1CInputParser_1a49a3cbb471aa8f1f8c79c0e3ee917803)`(`[`CStreamingFile`](#classshogun_1_1CStreamingFile)` * input_file,bool is_labelled,int32_t size)` | Initializer
`public bool `[`is_running`](#classshogun_1_1CInputParser_1a61da580fc69a74f3ef17956ba5fd88a0)`()` | Test if parser is running.
`public inline int32_t `[`get_number_of_features`](#classshogun_1_1CInputParser_1a5cd6db4ae6b3e0bd8f0e13d109e4211a)`()` | Get number of features from example. Currently reads first line of input to infer.
`public void `[`set_read_vector`](#classshogun_1_1CInputParser_1a487d6a262b1817d571f767d05260ba5b)`(void(CStreamingFile::*)(T *&vec, int32_t &len) func_ptr)` | Sets the function used for reading a vector from the file.
`public void `[`set_read_vector_and_label`](#classshogun_1_1CInputParser_1a3eded81c9e80901b565f147e03ba0a49)`(void(CStreamingFile::*)(T *&vec, int32_t &len, `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4) &label)` func_ptr)` | Sets the function used for reading a vector and label from the file.
`public int32_t `[`get_vector_and_label`](#classshogun_1_1CInputParser_1ac94345e45c037929bee681583c78ec27)`(T *& feature_vector,int32_t & length,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & label)` | Gets feature vector, length and label. Sets their values by reference. Uses method for reading the vector defined in [CStreamingFile](#classshogun_1_1CStreamingFile).
`public int32_t `[`get_vector_only`](#classshogun_1_1CInputParser_1ae6fdbada6241afc94537f812c2ba2324)`(T *& feature_vector,int32_t & length)` | Gets feature vector and length by reference. Assumes examples are unlabelled. Uses method for reading the vector defined in [CStreamingFile](#classshogun_1_1CStreamingFile).
`public void `[`set_free_vector_after_release`](#classshogun_1_1CInputParser_1ab5abe4523997cd4dd6473e3833803472)`(bool free_vec)` | Sets whether to SG_FREE() the vector explicitly after it has been used
`public void `[`set_free_vectors_on_destruct`](#classshogun_1_1CInputParser_1aacc307397f6873bcd94acbf3e209ffbf)`(bool destroy)` | Sets whether to free all vectors that were allocated in the ring upon destruction of the ring.
`public void `[`start_parser`](#classshogun_1_1CInputParser_1add2dbd5435810c2243f18502c09b3815)`()` | Starts the parser, creating a new thread.
`public void * `[`main_parse_loop`](#classshogun_1_1CInputParser_1a25b23cd7b3ad8f976238c4230ee0749a)`(void * params)` | Main parsing loop. Reads examples from source and stores them in the buffer.
`public void `[`copy_example_into_buffer`](#classshogun_1_1CInputParser_1a619a87dd026f2e1528d7f18bb8690a7b)`(`[`Example`](#classshogun_1_1Example)`< T > * ex)` | Copy example into the buffer.
`public `[`Example`](#classshogun_1_1Example)`< T > * `[`retrieve_example`](#classshogun_1_1CInputParser_1a382a2c640e80484df31eb06b3d11d100)`()` | Retrieves the next example from the buffer.
`public int32_t `[`get_next_example`](#classshogun_1_1CInputParser_1a3024b642cdcff2e661fb658bb1d3e629)`(T *& feature_vector,int32_t & length,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & label)` | Gets the next example, assuming it to be labelled.
`public int32_t `[`get_next_example`](#classshogun_1_1CInputParser_1a859bad3f913ec4e65dea45185319c892)`(T *& feature_vector,int32_t & length)` | Gets the next example, assuming it to be unlabelled.
`public void `[`finalize_example`](#classshogun_1_1CInputParser_1aea04cc7c5c7207e26a4616932a1f7121)`()` | Finalize the current example, indicating that the buffer position it occupies may be overwritten by the parser.
`public void `[`end_parser`](#classshogun_1_1CInputParser_1abe675af9c171a8bc0cecd7db93bd477e)`()` | End the parser, waiting for the parse thread to complete.
`public void `[`exit_parser`](#classshogun_1_1CInputParser_1a64acdb31d2a0d299d9b484eec4cb0d29)`()` | Terminates the parsing thread
`public inline int32_t `[`get_ring_size`](#classshogun_1_1CInputParser_1a72bf7c6ed7824bb5cc2a343ebde238d7)`()` | Returns the size of the examples ring
`protected void(CStreamingFile::* `[`read_vector`](#classshogun_1_1CInputParser_1a502eaee993969fa116d486dd3c607403) | This is the function pointer to the function to read a vector from the input.
`protected void(CStreamingFile::* `[`read_vector_and_label`](#classshogun_1_1CInputParser_1ab0a6d06c26a9f7bb6357d98b2639c22b) | This is the function pointer to the function to read a vector and label from the input.
`protected `[`CStreamingFile`](#classshogun_1_1CStreamingFile)` * `[`input_source`](#classshogun_1_1CInputParser_1a09cf646d494550b243e2fc1e9fdb9787) | Input source, [CStreamingFile](#classshogun_1_1CStreamingFile) object.
`protected std::thread `[`parse_thread`](#classshogun_1_1CInputParser_1a3f3a9cc3b5e80f9878c6577abc4fd29b) | Thread in which the parser runs.
`protected `[`CParseBuffer`](#classshogun_1_1CParseBuffer)`< T > * `[`examples_ring`](#classshogun_1_1CInputParser_1ae373cda9fa4c81686436601a26ba7934) | The ring of examples, stored as they are parsed.
`protected int32_t `[`number_of_features`](#classshogun_1_1CInputParser_1a6d1a41cd79d6e8cfd1aeac8723464ee6) | Number of features in dataset (max of 'seen' features upto point of access)
`protected int32_t `[`number_of_vectors_parsed`](#classshogun_1_1CInputParser_1aba7e682c3a66b2f82558e07cd74f4d22) | Number of vectors parsed.
`protected int32_t `[`number_of_vectors_read`](#classshogun_1_1CInputParser_1acebe204742485f849f8e46ff93925c42) | Number of vectors used by external algorithm.
`protected `[`Example`](#classshogun_1_1Example)`< T > * `[`current_example`](#classshogun_1_1CInputParser_1a6943b83df2406f005eaafa62250817ca) | [Example](#classshogun_1_1Example) currently being used.
`protected T * `[`current_feature_vector`](#classshogun_1_1CInputParser_1ac7ee7448fbdc79f09dc8b74b0df0e4f7) | Feature vector of current example.
`protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`current_label`](#classshogun_1_1CInputParser_1a90646e7bbc955ee24e0e658afa121978) | Label of current example.
`protected int32_t `[`current_len`](#classshogun_1_1CInputParser_1abbf8f1c7f91ce335835852979ef31c86) | Number of features in current example.
`protected bool `[`free_after_release`](#classshogun_1_1CInputParser_1a5301b566b9becc3a75882cda3be8393c) | Whether to SG_FREE() vector after it is used.
`protected int32_t `[`ring_size`](#classshogun_1_1CInputParser_1a75da208fbc8e142d48c6cbe1e72c9b1c) | Size of the ring of examples.
`protected std::mutex `[`examples_state_lock`](#classshogun_1_1CInputParser_1a7c80acba65b0e7c36adcc8137c4d71ba) | Mutex which is used when getting/setting state of examples (whether a new example is ready)
`protected std::condition_variable `[`examples_state_changed`](#classshogun_1_1CInputParser_1a0f8fe83bbba4bb386a2e7d7de36dda9b) | Condition variable to indicate change of state of examples.
`protected std::atomic_bool `[`keep_running`](#classshogun_1_1CInputParser_1a8128f0049027be51735da7de1f3a75cc) | Flag that indicate that the parsing thread should continue reading.

## Members

#### `public bool `[`parsing_done`](#classshogun_1_1CInputParser_1ad468303bfb3ed5725a023a81b2bba331) {#classshogun_1_1CInputParser_1ad468303bfb3ed5725a023a81b2bba331}

true if all input is parsed

#### `public bool `[`reading_done`](#classshogun_1_1CInputParser_1afcb198504c85035b753a5ed2563c8646) {#classshogun_1_1CInputParser_1afcb198504c85035b753a5ed2563c8646}

true if all examples are fetched

#### `public `[`E_EXAMPLE_TYPE`](#namespaceshogun_1ae875449f4a4a39610d61f785132aadeb)` `[`example_type`](#classshogun_1_1CInputParser_1aef0c79ba1132b2151ef0ccce56cf110a) {#classshogun_1_1CInputParser_1aef0c79ba1132b2151ef0ccce56cf110a}

LABELLED or UNLABELLED

#### `public  `[`CInputParser`](#classshogun_1_1CInputParser_1ad91e5e5f85c1113ffbd0d94852f86184)`()` {#classshogun_1_1CInputParser_1ad91e5e5f85c1113ffbd0d94852f86184}

Constructor

#### `public  `[`~CInputParser`](#classshogun_1_1CInputParser_1ab6ade70a434e26fe7f23e400194e8d84)`()` {#classshogun_1_1CInputParser_1ab6ade70a434e26fe7f23e400194e8d84}

Destructor

#### `public void `[`init`](#classshogun_1_1CInputParser_1a49a3cbb471aa8f1f8c79c0e3ee917803)`(`[`CStreamingFile`](#classshogun_1_1CStreamingFile)` * input_file,bool is_labelled,int32_t size)` {#classshogun_1_1CInputParser_1a49a3cbb471aa8f1f8c79c0e3ee917803}

Initializer

Sets initial or default values for members. is_example_used is initialized to EMPTY. example_type is LABELLED by default.

#### Parameters
* `input_file` [CStreamingFile](#classshogun_1_1CStreamingFile) object 

* `is_labelled` Whether example is labelled or not (bool), optional 

* `size` Size of the buffer in number of examples

#### `public bool `[`is_running`](#classshogun_1_1CInputParser_1a61da580fc69a74f3ef17956ba5fd88a0)`()` {#classshogun_1_1CInputParser_1a61da580fc69a74f3ef17956ba5fd88a0}

Test if parser is running.

#### Returns
true if running, false otherwise.

#### `public inline int32_t `[`get_number_of_features`](#classshogun_1_1CInputParser_1a5cd6db4ae6b3e0bd8f0e13d109e4211a)`()` {#classshogun_1_1CInputParser_1a5cd6db4ae6b3e0bd8f0e13d109e4211a}

Get number of features from example. Currently reads first line of input to infer.

#### Returns
Number of features

#### `public void `[`set_read_vector`](#classshogun_1_1CInputParser_1a487d6a262b1817d571f767d05260ba5b)`(void(CStreamingFile::*)(T *&vec, int32_t &len) func_ptr)` {#classshogun_1_1CInputParser_1a487d6a262b1817d571f767d05260ba5b}

Sets the function used for reading a vector from the file.

The function must be a member of [CStreamingFile](#classshogun_1_1CStreamingFile), taking a T* as input for the vector, and an int for length, setting both by reference. The function returns void.

The argument is a function pointer to that function.

#### `public void `[`set_read_vector_and_label`](#classshogun_1_1CInputParser_1a3eded81c9e80901b565f147e03ba0a49)`(void(CStreamingFile::*)(T *&vec, int32_t &len, `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4) &label)` func_ptr)` {#classshogun_1_1CInputParser_1a3eded81c9e80901b565f147e03ba0a49}

Sets the function used for reading a vector and label from the file.

The function must be a member of [CStreamingFile](#classshogun_1_1CStreamingFile), taking a T* as input for the vector, an int for length, and a float for the label, setting all by reference. The function returns void.

The argument is a function pointer to that function.

#### `public int32_t `[`get_vector_and_label`](#classshogun_1_1CInputParser_1ac94345e45c037929bee681583c78ec27)`(T *& feature_vector,int32_t & length,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & label)` {#classshogun_1_1CInputParser_1ac94345e45c037929bee681583c78ec27}

Gets feature vector, length and label. Sets their values by reference. Uses method for reading the vector defined in [CStreamingFile](#classshogun_1_1CStreamingFile).

#### Parameters
* `feature_vector` Pointer to feature vector 

* `length` Features in vector 

* `label` Label of example

#### Returns
1 on success, 0 on failure.

#### `public int32_t `[`get_vector_only`](#classshogun_1_1CInputParser_1ae6fdbada6241afc94537f812c2ba2324)`(T *& feature_vector,int32_t & length)` {#classshogun_1_1CInputParser_1ae6fdbada6241afc94537f812c2ba2324}

Gets feature vector and length by reference. Assumes examples are unlabelled. Uses method for reading the vector defined in [CStreamingFile](#classshogun_1_1CStreamingFile).

#### Parameters
* `feature_vector` Pointer to feature vector 

* `length` Features in vector

#### Returns
1 on success, 0 on failure

#### `public void `[`set_free_vector_after_release`](#classshogun_1_1CInputParser_1ab5abe4523997cd4dd6473e3833803472)`(bool free_vec)` {#classshogun_1_1CInputParser_1ab5abe4523997cd4dd6473e3833803472}

Sets whether to SG_FREE() the vector explicitly after it has been used

#### Parameters
* `free_vec` whether to SG_FREE() or not, bool

#### `public void `[`set_free_vectors_on_destruct`](#classshogun_1_1CInputParser_1aacc307397f6873bcd94acbf3e209ffbf)`(bool destroy)` {#classshogun_1_1CInputParser_1aacc307397f6873bcd94acbf3e209ffbf}

Sets whether to free all vectors that were allocated in the ring upon destruction of the ring.

#### Parameters
* `destroy` free all vectors on destruction

#### `public void `[`start_parser`](#classshogun_1_1CInputParser_1add2dbd5435810c2243f18502c09b3815)`()` {#classshogun_1_1CInputParser_1add2dbd5435810c2243f18502c09b3815}

Starts the parser, creating a new thread.

main_parse_loop is the parsing method.

#### `public void * `[`main_parse_loop`](#classshogun_1_1CInputParser_1a25b23cd7b3ad8f976238c4230ee0749a)`(void * params)` {#classshogun_1_1CInputParser_1a25b23cd7b3ad8f976238c4230ee0749a}

Main parsing loop. Reads examples from source and stores them in the buffer.

#### Parameters
* `params` 'this' object

#### Returns
NULL

#### `public void `[`copy_example_into_buffer`](#classshogun_1_1CInputParser_1a619a87dd026f2e1528d7f18bb8690a7b)`(`[`Example`](#classshogun_1_1Example)`< T > * ex)` {#classshogun_1_1CInputParser_1a619a87dd026f2e1528d7f18bb8690a7b}

Copy example into the buffer.

#### Parameters
* `ex` [Example](#classshogun_1_1Example) to be copied.

#### `public `[`Example`](#classshogun_1_1Example)`< T > * `[`retrieve_example`](#classshogun_1_1CInputParser_1a382a2c640e80484df31eb06b3d11d100)`()` {#classshogun_1_1CInputParser_1a382a2c640e80484df31eb06b3d11d100}

Retrieves the next example from the buffer.

#### Returns
The example pointer.

#### `public int32_t `[`get_next_example`](#classshogun_1_1CInputParser_1a3024b642cdcff2e661fb658bb1d3e629)`(T *& feature_vector,int32_t & length,`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` & label)` {#classshogun_1_1CInputParser_1a3024b642cdcff2e661fb658bb1d3e629}

Gets the next example, assuming it to be labelled.

Waits till retrieve_example returns a valid example, or returns if reading is done already.

#### Parameters
* `feature_vector` Feature vector pointer 

* `length` Length of feature vector 

* `label` Label of example

#### Returns
1 if an example could be fetched, 0 otherwise

#### `public int32_t `[`get_next_example`](#classshogun_1_1CInputParser_1a859bad3f913ec4e65dea45185319c892)`(T *& feature_vector,int32_t & length)` {#classshogun_1_1CInputParser_1a859bad3f913ec4e65dea45185319c892}

Gets the next example, assuming it to be unlabelled.

#### Parameters
* `feature_vector` 

* `length` 

#### Returns
1 if an example could be fetched, 0 otherwise

#### `public void `[`finalize_example`](#classshogun_1_1CInputParser_1aea04cc7c5c7207e26a4616932a1f7121)`()` {#classshogun_1_1CInputParser_1aea04cc7c5c7207e26a4616932a1f7121}

Finalize the current example, indicating that the buffer position it occupies may be overwritten by the parser.

Should be called when the example has been processed by the external algorithm.

#### `public void `[`end_parser`](#classshogun_1_1CInputParser_1abe675af9c171a8bc0cecd7db93bd477e)`()` {#classshogun_1_1CInputParser_1abe675af9c171a8bc0cecd7db93bd477e}

End the parser, waiting for the parse thread to complete.

#### `public void `[`exit_parser`](#classshogun_1_1CInputParser_1a64acdb31d2a0d299d9b484eec4cb0d29)`()` {#classshogun_1_1CInputParser_1a64acdb31d2a0d299d9b484eec4cb0d29}

Terminates the parsing thread

#### `public inline int32_t `[`get_ring_size`](#classshogun_1_1CInputParser_1a72bf7c6ed7824bb5cc2a343ebde238d7)`()` {#classshogun_1_1CInputParser_1a72bf7c6ed7824bb5cc2a343ebde238d7}

Returns the size of the examples ring

#### Returns
ring size in terms of number of examples

#### `protected void(CStreamingFile::* `[`read_vector`](#classshogun_1_1CInputParser_1a502eaee993969fa116d486dd3c607403) {#classshogun_1_1CInputParser_1a502eaee993969fa116d486dd3c607403}

This is the function pointer to the function to read a vector from the input.

It is called while reading a vector.

#### `protected void(CStreamingFile::* `[`read_vector_and_label`](#classshogun_1_1CInputParser_1ab0a6d06c26a9f7bb6357d98b2639c22b) {#classshogun_1_1CInputParser_1ab0a6d06c26a9f7bb6357d98b2639c22b}

This is the function pointer to the function to read a vector and label from the input.

It is called while reading a vector and a label.

#### `protected `[`CStreamingFile`](#classshogun_1_1CStreamingFile)` * `[`input_source`](#classshogun_1_1CInputParser_1a09cf646d494550b243e2fc1e9fdb9787) {#classshogun_1_1CInputParser_1a09cf646d494550b243e2fc1e9fdb9787}

Input source, [CStreamingFile](#classshogun_1_1CStreamingFile) object.

#### `protected std::thread `[`parse_thread`](#classshogun_1_1CInputParser_1a3f3a9cc3b5e80f9878c6577abc4fd29b) {#classshogun_1_1CInputParser_1a3f3a9cc3b5e80f9878c6577abc4fd29b}

Thread in which the parser runs.

#### `protected `[`CParseBuffer`](#classshogun_1_1CParseBuffer)`< T > * `[`examples_ring`](#classshogun_1_1CInputParser_1ae373cda9fa4c81686436601a26ba7934) {#classshogun_1_1CInputParser_1ae373cda9fa4c81686436601a26ba7934}

The ring of examples, stored as they are parsed.

#### `protected int32_t `[`number_of_features`](#classshogun_1_1CInputParser_1a6d1a41cd79d6e8cfd1aeac8723464ee6) {#classshogun_1_1CInputParser_1a6d1a41cd79d6e8cfd1aeac8723464ee6}

Number of features in dataset (max of 'seen' features upto point of access)

#### `protected int32_t `[`number_of_vectors_parsed`](#classshogun_1_1CInputParser_1aba7e682c3a66b2f82558e07cd74f4d22) {#classshogun_1_1CInputParser_1aba7e682c3a66b2f82558e07cd74f4d22}

Number of vectors parsed.

#### `protected int32_t `[`number_of_vectors_read`](#classshogun_1_1CInputParser_1acebe204742485f849f8e46ff93925c42) {#classshogun_1_1CInputParser_1acebe204742485f849f8e46ff93925c42}

Number of vectors used by external algorithm.

#### `protected `[`Example`](#classshogun_1_1Example)`< T > * `[`current_example`](#classshogun_1_1CInputParser_1a6943b83df2406f005eaafa62250817ca) {#classshogun_1_1CInputParser_1a6943b83df2406f005eaafa62250817ca}

[Example](#classshogun_1_1Example) currently being used.

#### `protected T * `[`current_feature_vector`](#classshogun_1_1CInputParser_1ac7ee7448fbdc79f09dc8b74b0df0e4f7) {#classshogun_1_1CInputParser_1ac7ee7448fbdc79f09dc8b74b0df0e4f7}

Feature vector of current example.

#### `protected `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`current_label`](#classshogun_1_1CInputParser_1a90646e7bbc955ee24e0e658afa121978) {#classshogun_1_1CInputParser_1a90646e7bbc955ee24e0e658afa121978}

Label of current example.

#### `protected int32_t `[`current_len`](#classshogun_1_1CInputParser_1abbf8f1c7f91ce335835852979ef31c86) {#classshogun_1_1CInputParser_1abbf8f1c7f91ce335835852979ef31c86}

Number of features in current example.

#### `protected bool `[`free_after_release`](#classshogun_1_1CInputParser_1a5301b566b9becc3a75882cda3be8393c) {#classshogun_1_1CInputParser_1a5301b566b9becc3a75882cda3be8393c}

Whether to SG_FREE() vector after it is used.

#### `protected int32_t `[`ring_size`](#classshogun_1_1CInputParser_1a75da208fbc8e142d48c6cbe1e72c9b1c) {#classshogun_1_1CInputParser_1a75da208fbc8e142d48c6cbe1e72c9b1c}

Size of the ring of examples.

#### `protected std::mutex `[`examples_state_lock`](#classshogun_1_1CInputParser_1a7c80acba65b0e7c36adcc8137c4d71ba) {#classshogun_1_1CInputParser_1a7c80acba65b0e7c36adcc8137c4d71ba}

Mutex which is used when getting/setting state of examples (whether a new example is ready)

#### `protected std::condition_variable `[`examples_state_changed`](#classshogun_1_1CInputParser_1a0f8fe83bbba4bb386a2e7d7de36dda9b) {#classshogun_1_1CInputParser_1a0f8fe83bbba4bb386a2e7d7de36dda9b}

Condition variable to indicate change of state of examples.

#### `protected std::atomic_bool `[`keep_running`](#classshogun_1_1CInputParser_1a8128f0049027be51735da7de1f3a75cc) {#classshogun_1_1CInputParser_1a8128f0049027be51735da7de1f3a75cc}

Flag that indicate that the parsing thread should continue reading.

