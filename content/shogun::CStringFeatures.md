---
classname: "shogun::CStringFeatures"
type: "class"
parents:
   - CFeatures
---

# class `shogun::CStringFeatures` {#classshogun_1_1CStringFeatures}

```
class shogun::CStringFeatures
  : public CFeatures
```

Template class StringFeatures implements a list of strings.

As this class is a template the underlying storage type is quite arbitrary and not limited to character strings, but could also be sequences of floating point numbers etc. Strings differ from matrices (cf. [CDenseFeatures](#classshogun_1_1CDenseFeatures)) in a way that the dimensionality of the feature vectors (i.e. the strings) is not fixed; it may vary between strings.

Most string kernels require StringFeatures but a number of them actually requires strings to have same length.

When preprocessors are attached to string features they may shorten the string, but are not allowed to return strings longer than max_string_length, as some algorithms depend on this.

Also note that string features cannot currently be computed on-the-fly.

(Partly) subset access is supported for this feature type. Simple use the (inherited) [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71), [remove_subset()](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172) functions. If done, all calls that work with features are translated to the subset. See comments to find out whether it is supported for that method. See also [CFeatures](#classshogun_1_1CFeatures) class documentation

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) | io
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) | parallel
`public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) | version
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) | parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) | model selection parameters
`public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) | parameters wrt which we can compute gradients
`public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) | Hash of parameter values
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1af3981c5803cc1481b8cac5f0a7ab91ef)`()` | default constructor
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1afa9617ef957fa4ecccbc0d4c0719de51)`(`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` alpha)` | constructor
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a1857f28eb5d6d748887240b7da69d1f5)`(`[`SGStringList`](#classshogun_1_1SGStringList)`< ST > string_list,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` alpha)` | constructor
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a411fc928305d6a224806366d209a6e6f)`(`[`SGStringList`](#classshogun_1_1SGStringList)`< ST > string_list,`[`CAlphabet`](#classshogun_1_1CAlphabet)` * alpha)` | constructor
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a27dc9b9a3d1f7f7c57070c3083ef3ced)`(`[`CAlphabet`](#classshogun_1_1CAlphabet)` * alpha)` | constructor
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1abe8ee4c991bd1573e0ef40a6c8068576)`(const `[`CStringFeatures`](#classshogun_1_1CStringFeatures)` & orig)` | copy constructor
`public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a520bb0b8b9d06d74b995645b91fa69ba)`(`[`CFile`](#classshogun_1_1CFile)` * loader,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` alpha)` | constructor
`public virtual  `[`~CStringFeatures`](#classshogun_1_1CStringFeatures_1a44d3e600d45c117486fed711e5a6b4dd)`()` | destructor
`public virtual void `[`cleanup`](#classshogun_1_1CStringFeatures_1a4b66d5e31b5dc18b314c8a68163263bd)`()` | cleanup string features.
`public virtual void `[`cleanup_feature_vector`](#classshogun_1_1CStringFeatures_1a73082e442a1c84e69995a6fc6bb03305)`(int32_t num)` | cleanup a single feature vector
`public virtual void `[`cleanup_feature_vectors`](#classshogun_1_1CStringFeatures_1a128339a3051e17cbbb6583b648b86f3d)`(int32_t start,int32_t stop)` | cleanup multiple feature vectors
`public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CStringFeatures_1ae83dd54e69a4e8f1c7a571545fa1c8c1)`() const` | get feature class
`public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CStringFeatures_1ab0a6eabf1ffd31e38a03365bdaaba64d)`() const` | get feature type
`public `[`CAlphabet`](#classshogun_1_1CAlphabet)` * `[`get_alphabet`](#classshogun_1_1CStringFeatures_1a982d8d0f54d9ceaf7d187dba7031a591)`()` | get alphabet used in string features
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`duplicate`](#classshogun_1_1CStringFeatures_1a451c5fd7954842d7a19f1b0faa710e0c)`() const` | duplicate feature object
`public `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_feature_vector`](#classshogun_1_1CStringFeatures_1a21e2db18e15e281b91e4ba6cabe747e9)`(int32_t num)` | get string for selected example num
`public void `[`set_feature_vector`](#classshogun_1_1CStringFeatures_1affd56f6e718d53ead36a9b67e53055cc)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > vector,int32_t num)` | set string for selected example num
`public void `[`enable_on_the_fly_preprocessing`](#classshogun_1_1CStringFeatures_1ae8720f87d0db7b8decdb5611d9af84fe)`()` | call this to preprocess string features upon call to get_feature_vector
`public void `[`disable_on_the_fly_preprocessing`](#classshogun_1_1CStringFeatures_1adb8fca2a3a00f5490e2cdbcec40bd233)`()` | call this to disable on the fly feature preprocessing upon call to get_feature_vector. Useful when you manually apply preprocessors.
`public ST * `[`get_feature_vector`](#classshogun_1_1CStringFeatures_1a16bf23330a09924b5695d4ca7dfbcee9)`(int32_t num,int32_t & len,bool & dofree)` | get feature vector for sample num
`public `[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< ST > * `[`get_transposed`](#classshogun_1_1CStringFeatures_1adbfc72db66ac3ef7d57583349444b969)`()` | get a transposed copy of the features
`public `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`get_transposed`](#classshogun_1_1CStringFeatures_1a486476c6523978e9e0a3650c3ea60bc9)`(int32_t & num_feat,int32_t & num_vec)` | compute and return the transpose of string features matrix which will be prepocessed. num_feat, num_vectors are returned by reference caller has to clean up
`public void `[`free_feature_vector`](#classshogun_1_1CStringFeatures_1a2f79d81ff5b83d247dfc124e0e1f9a0f)`(ST * feat_vec,int32_t num,bool dofree)` | free feature vector
`public void `[`free_feature_vector`](#classshogun_1_1CStringFeatures_1a662229cc7fd6fb86b9f3b11323020ef3)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > feat_vec,int32_t num)` | free feature vector
`public virtual ST `[`get_feature`](#classshogun_1_1CStringFeatures_1a3ec6ee2d63518d13eada2974b8d0fdff)`(int32_t vec_num,int32_t feat_num)` | get feature
`public virtual int32_t `[`get_vector_length`](#classshogun_1_1CStringFeatures_1ae73eebc4d2d287bf5fbf397130c111bf)`(int32_t vec_num)` | get vector length
`public virtual int32_t `[`get_max_vector_length`](#classshogun_1_1CStringFeatures_1ab5615e3fa0e2478079a5af5f150cfdec)`()` | get maximum vector length
`public virtual int32_t `[`get_num_vectors`](#classshogun_1_1CStringFeatures_1a25a45bd4c25c9d7d72826dd195a7c696)`() const` | #### Returns
`public `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_num_symbols`](#classshogun_1_1CStringFeatures_1a3d12833241b07efb89c84fe51c409f7c)`()` | get number of symbols
`public `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_max_num_symbols`](#classshogun_1_1CStringFeatures_1ab8564e65079bcc45e117444488fcfb31)`()` | get maximum number of symbols
`public `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_original_num_symbols`](#classshogun_1_1CStringFeatures_1a827e4186e45b5fca5fb5308675cb0a55)`()` | number of symbols before higher order mapping
`public int32_t `[`get_order`](#classshogun_1_1CStringFeatures_1a768f3ae46d11695373dc33824e9cc586)`()` | order used for higher order mapping
`public ST `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1a7001733fe224942487be9f8715b52a8c)`(ST symbol,uint8_t mask)` | a higher order mapped symbol will be shaped such that the symbols specified by bits in the mask will be returned.
`public ST `[`shift_offset`](#classshogun_1_1CStringFeatures_1ae96e78b74c95f7b25d1e4624b2d5d8a4)`(ST offset,int32_t amount)` | shift offset to the left by amount
`public ST `[`shift_symbol`](#classshogun_1_1CStringFeatures_1ae88ac8772d7c21ce98833c7c2cdefa9c)`(ST symbol,int32_t amount)` | shift symbol to the right by amount (taking care of custom symbol sizes)
`public virtual void `[`load`](#classshogun_1_1CStringFeatures_1a3855e09ef07683f41271b023b6b95e9d)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` | load features from file
`public void `[`load_ascii_file`](#classshogun_1_1CStringFeatures_1a3a4d55be0f1a9e0b4fb385995fc1910d)`(char * fname,bool remap_to_bin,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` ascii_alphabet,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` binary_alphabet)` | load ascii line-based string features from file.
`public bool `[`load_fasta_file`](#classshogun_1_1CStringFeatures_1a2a271323306e65ba097fe1b5e91c862c)`(const char * fname,bool ignore_invalid)` | load fasta file as string features
`public bool `[`load_fastq_file`](#classshogun_1_1CStringFeatures_1afe8b54317b3d56b85004d2c84632e0ca)`(const char * fname,bool ignore_invalid,bool bitremap_in_single_string)` | load fastq file as string features
`public bool `[`load_from_directory`](#classshogun_1_1CStringFeatures_1a62097a72b81d6a256c85a2302f81750a)`(char * dirname)` | load features from directory
`public void `[`set_features`](#classshogun_1_1CStringFeatures_1ac7dd73af410c92b1b62826d33030736b)`(`[`SGStringList`](#classshogun_1_1SGStringList)`< ST > feats)` | set features
`public bool `[`set_features`](#classshogun_1_1CStringFeatures_1a4fdad0274be1a00b81b0c5ed6cac2cab)`(`[`SGString`](#classshogun_1_1SGString)`< ST > * p_features,int32_t p_num_vectors,int32_t p_max_string_length)` | set features
`public bool `[`append_features`](#classshogun_1_1CStringFeatures_1ad81d9b128d2ca029ee7ec65a7619806c)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< ST > * sf)` | append features If the given string features have a subset, only this will be copied
`public bool `[`append_features`](#classshogun_1_1CStringFeatures_1a413d448b8eabaa5704bfa0a5d4407827)`(`[`SGString`](#classshogun_1_1SGString)`< ST > * p_features,int32_t p_num_vectors,int32_t p_max_string_length)` | append features
`public `[`SGStringList`](#classshogun_1_1SGStringList)`< ST > `[`get_features`](#classshogun_1_1CStringFeatures_1afeacc8f3ce2fa5a3f72fe2c0f2471ebb)`()` | get_features 
`public virtual `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`get_features`](#classshogun_1_1CStringFeatures_1ad5daea541f34703b851c2c1a31dd8e0a)`(int32_t & num_str,int32_t & max_str_len)` | get_features
`public virtual `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`copy_features`](#classshogun_1_1CStringFeatures_1a1f4a76767c06fa82d22179adfeb1c8b2)`(int32_t & num_str,int32_t & max_str_len)` | copy_features
`public virtual void `[`get_features`](#classshogun_1_1CStringFeatures_1aebb80574ee50e0cf8ae4b936c5db21b4)`(`[`SGString`](#classshogun_1_1SGString)`< ST > ** dst,int32_t * num_str)` | get_features (swig compatible)
`public virtual void `[`save`](#classshogun_1_1CStringFeatures_1ad3e5050e8b6b2f97e3f8894bb688e1f1)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` | save features to file
`public virtual bool `[`load_compressed`](#classshogun_1_1CStringFeatures_1ac843a07f509e48ccaedd7eb857f11230)`(char * src,bool decompress)` | load compressed features from file
`public virtual bool `[`save_compressed`](#classshogun_1_1CStringFeatures_1a4dc4fbf952dd0e43172a879b967fe6a9)`(char * dest,`[`E_COMPRESSION_TYPE`](#namespaceshogun_1a40ddde55c6601043ad2ade2da936c98f)` compression,int level)` | save compressed features to file
`public int32_t `[`obtain_by_sliding_window`](#classshogun_1_1CStringFeatures_1a78b86f6c8b9ae4ed75330a037d3dcc91)`(int32_t window_size,int32_t step_size,int32_t skip)` | slides a window of size window_size over the current single string step_size is the amount by which the window is shifted. creates (string_len-window_size)/step_size many feature obj if skip is nonzero, skip the first 'skip' characters of each string
`public int32_t `[`obtain_by_position_list`](#classshogun_1_1CStringFeatures_1ac8ab24077fbd94a19f7ad1447e9b9d84)`(int32_t window_size,`[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > * positions,int32_t skip)` | extracts windows of size window_size from first string using the positions in list
`public bool `[`obtain_from_char`](#classshogun_1_1CStringFeatures_1a043ecbf5656c295df1621a4aeac73c47)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< char > * sf,int32_t start,int32_t p_order,int32_t gap,bool rev)` | obtain string features from char features
`public template<>`  <br/>`bool `[`obtain_from_char_features`](#classshogun_1_1CStringFeatures_1add0e22e74e445ced1368f42acafa055b)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< CT > * sf,int32_t start,int32_t p_order,int32_t gap,bool rev)` | template obtain from char features
`public bool `[`have_same_length`](#classshogun_1_1CStringFeatures_1a0941c0a0837b8647d7aa97617b23133b)`(int32_t len)` | check if length of each vector in this feature object equals the given length. if existant, only subset is checked
`public void `[`embed_features`](#classshogun_1_1CStringFeatures_1a0e7ec341f4ccf96f4f25a1e55cf3ee63)`(int32_t p_order)` | embed string features in bit representation in-place
`public void `[`compute_symbol_mask_table`](#classshogun_1_1CStringFeatures_1ad3ea9f6809f80b503f81d6ddbc0aecf6)`(int64_t max_val)` | compute symbol mask table
`public void `[`unembed_word`](#classshogun_1_1CStringFeatures_1aa1b467c0e17ca81bddf2820c3196fc1d)`(ST word,uint8_t * seq,int32_t len)` | remap bit-based word to character sequence
`public ST `[`embed_word`](#classshogun_1_1CStringFeatures_1a1edd7748e963dce5abb30c49453705fc)`(ST * seq,int32_t len)` | embed a single word
`public void `[`determine_maximum_string_length`](#classshogun_1_1CStringFeatures_1aea6761787914a98859736a5a998bea44)`()` | determine new maximum string length
`public virtual void `[`set_feature_vector`](#classshogun_1_1CStringFeatures_1a02191fc2d3023a80b7611a1574bede15)`(int32_t num,ST * string,int32_t len)` | set feature vector for sample num
`public virtual void `[`get_histogram`](#classshogun_1_1CStringFeatures_1a451dc9218ea4aa9c7c3d1bf52fe45eac)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** hist,int32_t * rows,int32_t * cols,bool normalize)` | compute histogram over strings
`public virtual void `[`create_random`](#classshogun_1_1CStringFeatures_1ae0e29f1ce4e8ba243c3c0ffd4981e9b7)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * hist,int32_t rows,int32_t cols,int32_t num_vec)` | create some random strings based on normalized histogram
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_subset`](#classshogun_1_1CStringFeatures_1adf4a1baaff0c06456ceca3b217c46338)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` | Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing copies of the elements which are specified by the provided indices.
`public inline virtual const char * `[`get_name`](#classshogun_1_1CStringFeatures_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` | #### Returns
`public virtual void `[`subset_changed_post`](#classshogun_1_1CStringFeatures_1a401beb1a47c67fc5d23d09e14f39e0f5)`()` | post method when subset is changed
`public template<>`  <br/>`virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CStringFeatures_1a617d0eeddcb6e6eefd24fb33a2e627cd)`() const` | get feature type the LONGREAL feature can deal with
`public template<>`  <br/>`bool `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1af8364b5d13e2c3115606a318c644850b)`(bool symbol,uint8_t mask)` | 
`public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1a0ba409d902d562af7b0b47e14878e3de)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` symbol,uint8_t mask)` | 
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1af585411821670e9ebf79877c104681e0)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` symbol,uint8_t mask)` | 
`public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1aec0bf831702f90a34eb65b71fc0bfaf3)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` symbol,uint8_t mask)` | 
`public template<>`  <br/>`bool `[`shift_offset`](#classshogun_1_1CStringFeatures_1ac97945afaa616f198cc839c240ced773)`(bool symbol,int32_t amount)` | 
`public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`shift_offset`](#classshogun_1_1CStringFeatures_1a9641ce1ede80ca73d451c7566b6f54f8)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` symbol,int32_t amount)` | 
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`shift_offset`](#classshogun_1_1CStringFeatures_1a1d410816d705897c31a18bd59ca7fa1b)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` symbol,int32_t amount)` | 
`public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`shift_offset`](#classshogun_1_1CStringFeatures_1ab62c5acbfa860ebc49c92dc1bb85174b)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` symbol,int32_t amount)` | 
`public template<>`  <br/>`bool `[`shift_symbol`](#classshogun_1_1CStringFeatures_1a1a486831974b0335fa5a5f4d47e9596d)`(bool symbol,int32_t amount)` | 
`public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`shift_symbol`](#classshogun_1_1CStringFeatures_1a78f7a8103d488c2a6f8b3ca77e04bb2d)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` symbol,int32_t amount)` | 
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`shift_symbol`](#classshogun_1_1CStringFeatures_1ad123531444eb42219d5d2d2adb400d50)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` symbol,int32_t amount)` | 
`public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`shift_symbol`](#classshogun_1_1CStringFeatures_1a4b0a37c772cadfe579132df1e5fc140c)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` symbol,int32_t amount)` | 
`public template<>`  <br/>`bool `[`obtain_from_char_features`](#classshogun_1_1CStringFeatures_1aa69a66b08d7c68567437f42b681cecc7)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< CT > * sf,int32_t start,int32_t p_order,int32_t gap,bool rev)` | 
`public template<>`  <br/>`void `[`embed_features`](#classshogun_1_1CStringFeatures_1a744bb3788b2ec0cea700b18261fa4e8a)`(int32_t p_order)` | 
`public template<>`  <br/>`void `[`compute_symbol_mask_table`](#classshogun_1_1CStringFeatures_1a3561231c00505210be6036fc672775b8)`(int64_t max_val)` | 
`public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`embed_word`](#classshogun_1_1CStringFeatures_1a8fa2e26ed1a0ace65a3687c510dbac29)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * seq,int32_t len)` | 
`public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`embed_word`](#classshogun_1_1CStringFeatures_1a3b96479a49f7bb69f7c80226734d223a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * seq,int32_t len)` | 
`public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`embed_word`](#classshogun_1_1CStringFeatures_1addd1555466d72e8f32eb71a0fb5fdb9a)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * seq,int32_t len)` | 
`public template<>`  <br/>`void `[`unembed_word`](#classshogun_1_1CStringFeatures_1a58a25285389c90da7026f3d4664ab1ed)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` word,uint8_t * seq,int32_t len)` | 
`public template<>`  <br/>`void `[`unembed_word`](#classshogun_1_1CStringFeatures_1abc88c03d3adba5765ae4bca857f2bd29)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` word,uint8_t * seq,int32_t len)` | 
`public template<>`  <br/>`void `[`unembed_word`](#classshogun_1_1CStringFeatures_1a9c1f119ec35113bf10542126b5b75bd4)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` word,uint8_t * seq,int32_t len)` | 
`public inline virtual `[`Range`](#classshogun_1_1Range)`< int32_t > `[`index_iterator`](#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd)`() const` | returns an iterator of indices from 0 to [CFeatures::get_num_vectors](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)
`public virtual void `[`add_preprocessor`](#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6)`(`[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * p)` | add preprocessor
`public virtual void `[`del_preprocessor`](#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2)`(int32_t num)` | delete preprocessor from list
`public `[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * `[`get_preprocessor`](#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b)`(int32_t num) const` | get specified preprocessor
`public int32_t `[`get_num_preprocessors`](#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54)`() const` | get number of preprocessors
`public void `[`clean_preprocessors`](#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2)`()` | clears all preprocs
`public void `[`list_preprocessors`](#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147)`()` | print preprocessors
`public int32_t `[`get_cache_size`](#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e)`() const` | get cache size
`public virtual bool `[`reshape`](#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287)`(int32_t num_features,int32_t num_vectors)` | in case there is a feature matrix allow for reshaping
`public void `[`list_feature_obj`](#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7)`() const` | list feature object
`public bool `[`check_feature_compatibility`](#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f) const` | check feature compatibility
`public bool `[`has_property`](#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p) const` | check if features have given property
`public void `[`set_property`](#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` | set property
`public void `[`unset_property`](#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` | unset property
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e)`(`[`CList`](#classshogun_1_1CList)` * others) const` | Takes a list of feature instances and returns a new instance being a concatenation of a copy of this instace's data and the given instancess data. Note that the feature types have to be equal.
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * other) const` | Convenience method for method with same name and list as parameter.
`public virtual void `[`add_subset`](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)
`public virtual void `[`add_subset_in_place`](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` | Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.
`public virtual void `[`remove_subset`](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` | removes that last added subset from subset stack, if existing Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards
`public virtual void `[`remove_all_subsets`](#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` | removes all subsets Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards
`public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253)`()` | returns subset stack
`public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_dimension_subset`](#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > dims)` | Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing only the dimensions of the feature vector which are specified by the provided indices.
`public inline virtual bool `[`support_compatible_class`](#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f)`() const` | does this class support compatible computation bewteen difference classes? for example, this->dot(rhs_prt), can rhs_prt be an instance of a difference class?
`public virtual bool `[`get_feature_class_compatibility`](#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6)`(`[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` rhs) const` | Given a class in right hand side, does this class support compatible computation?
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` | Throws an error, as features are immutable
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be)`(const std::string & name,T * value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` | Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d)`(const std::string & name,T value)` | Typed setter for a non-object class parameter, identified by a name.
`public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`shallow_subset_copy`](#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4)`()` | 
`public int32_t `[`ref`](#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a)`()` | increase reference counter
`public int32_t `[`ref_count`](#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d)`()` | display reference counter
`public int32_t `[`unref`](#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01)`()` | decrement reference counter and deallocate object if refcount is zero before or after decrementing it
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`shallow_copy`](#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4)`() const` | A shallow copy. All the SGObject instance variables will be simply assigned and SG_REF-ed.
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`deep_copy`](#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578)`() const` | A deep copy. All the instance variables will also be copied.
`public virtual bool `[`is_generic`](#classshogun_1_1CSGObject_1a6801eb416eadc35f5499a48436e1cf43)`(EPrimitiveType * generic) const` | If the SGSerializable is a class template then TRUE will be returned and GENERIC is set to the type of the generic.
`public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1ad3463e866082d6707af04276ae8aa477)`()` | set generic type to T
`public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1a9fca24ed1095acc6c52f3c5353156d74)`()` | 
`public inline EPrimitiveType `[`get_generic`](#classshogun_1_1CSGObject_1a3329cfa1654e757472c9098770635530)`() const` | Returns generic type. 
`public void `[`unset_generic`](#classshogun_1_1CSGObject_1aa15afe4277334593139dae884cc951e1)`()` | unset generic type
`public virtual void `[`print_serializable`](#classshogun_1_1CSGObject_1ade3b14c2f62ba4d8f2f6422e08567ae9)`(const char * prefix)` | prints registered parameters out
`public virtual bool `[`save_serializable`](#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | Save this object to file.
`public virtual bool `[`load_serializable`](#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | Load this object from file. If it will fail (returning FALSE) then this object will contain inconsistent data and should not be used!
`public void `[`set_global_io`](#classshogun_1_1CSGObject_1a36d256e2d05357b57e83f31f7e358f69)`(`[`SGIO`](#classshogun_1_1SGIO)` * io)` | set the io object
`public `[`SGIO`](#classshogun_1_1SGIO)` * `[`get_global_io`](#classshogun_1_1CSGObject_1ac6c994717cb550f81c70129e839ea98b)`()` | get the io object
`public void `[`set_global_parallel`](#classshogun_1_1CSGObject_1a9543b75e320e477d12553f2aa8593e8a)`(`[`Parallel`](#classshogun_1_1Parallel)` * parallel)` | set the parallel object
`public `[`Parallel`](#classshogun_1_1Parallel)` * `[`get_global_parallel`](#classshogun_1_1CSGObject_1a2cd3ba36c7e0ef6e5234393cc7e22bb0)`()` | get the parallel object
`public void `[`set_global_version`](#classshogun_1_1CSGObject_1a1ba2ee8842e30d8ceaaf5d44c567efe1)`(`[`Version`](#classshogun_1_1Version)` * version)` | set the version object
`public `[`Version`](#classshogun_1_1Version)` * `[`get_global_version`](#classshogun_1_1CSGObject_1a03ce854ec4f745dbe219533dc36c9e20)`()` | get the version object
`public `[`SGStringList`](#classshogun_1_1SGStringList)`< char > `[`get_modelsel_names`](#classshogun_1_1CSGObject_1a730ecbf7f326b93350f00cc937e59ac0)`()` | #### Returns
`public void `[`print_modsel_params`](#classshogun_1_1CSGObject_1a8dcb739fd760f227b3fa1dc0684f762d)`()` | prints all parameter registered for model selection and their type
`public char * `[`get_modsel_param_descr`](#classshogun_1_1CSGObject_1ac26fd2403c6a5c334f4a2d8094be9833)`(const char * param_name)` | Returns description of a given parameter string, if it exists. SG_ERROR otherwise
`public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_modsel_param_index`](#classshogun_1_1CSGObject_1aeb1f5a55b8170409ff2a94e3a3664c05)`(const char * param_name)` | Returns index of model selection parameter with provided index
`public void `[`build_gradient_parameter_dictionary`](#classshogun_1_1CSGObject_1a17f448c257ccf4083987c4670c86a967)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * dict)` | Builds a dictionary of all parameters in SGObject as well of those of SGObjects that are parameters of this object. Dictionary maps parameters to the objects that own them.
`public bool `[`has`](#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424)`(const std::string & name) const` | Checks if object has a class parameter identified by a name.
`public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1a0ba98fe70db33bb2036e76fd4ec28e04)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & tag) const` | Checks if object has a class parameter identified by a [Tag](#classshogun_1_1Tag).
`public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1ac947804131f9937507db2da99f36e933)`(const std::string & name) const` | Checks if a type exists for a class parameter identified by a name.
`public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a3b1dff76eb6397801f84101060c5956c)`(const std::string & name,T * value)` | Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a98738b2423f4eb9cee078924311a9e04)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` | Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.
`public `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get`](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7)`(const std::string & name)` | Untyped getter for an object class parameter, identified by a name. Will attempt to get specified object of appropriate internal type.
`public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1a081b48e5b14e9ff75e7e56c941870ed5)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag) const` | Getter for a class parameter, identified by a [Tag](#classshogun_1_1Tag). Throws an exception if the class does not have such a parameter.
`public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1adeb49b89495067e83e4208d1d60bea60)`(const std::string & name) const` | Getter for a class parameter, identified by a name. Throws an exception if the class does not have such a parameter.
`public virtual std::string `[`to_string`](#classshogun_1_1CSGObject_1aac993ecccd3d88aafefb6b8e3caa1dee)`() const` | Returns string representation of the object that contains its name and parameters.
`public std::vector< std::string > `[`parameter_names`](#classshogun_1_1CSGObject_1a924f620b4718c3367cf5403c52a30074)`() const` | Returns set of all parameter names of the object.
`public template<>`  <br/>`inline T * `[`as`](#classshogun_1_1CSGObject_1aa4cdefb81ca8c583f1c2ef0d20d8feeb)`()` | Specializes the object to the specified type. Throws exception if the object cannot be specialized.
`public inline `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556)` * `[`get_parameters_observable`](#classshogun_1_1CSGObject_1a539800ba1bbe5a4260df8c5641305afc)`()` | Get parameters observable 
`public void `[`subscribe_to_parameters`](#classshogun_1_1CSGObject_1aeb13a31ffeb912767b6f16f1bc1d3e61)`(`[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface)` * obs)` | Subscribe a parameter observer to watch over params
`public void `[`list_observable_parameters`](#classshogun_1_1CSGObject_1aac0c9d125edd61f235eeba5efed47142)`()` | Print to stdout a list of observable parameters
`public virtual void `[`update_parameter_hash`](#classshogun_1_1CSGObject_1afd6d5beea40c6d1222d361fb706d4651)`()` | Updates the hash of current parameter combination
`public virtual bool `[`parameter_hash_changed`](#classshogun_1_1CSGObject_1aeb270031640bb2f00ec9452c637bfbc2)`()` | #### Returns
`public virtual bool `[`equals`](#classshogun_1_1CSGObject_1afe6a79f0c2c3db09f98ebdbe23a8a5d9)`(const `[`CSGObject`](#classshogun_1_1CSGObject)` * other) const` | Deep comparison of two objects.
`public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`clone`](#classshogun_1_1CSGObject_1a4ae46a8c294896b69fc21384f6d86fad)`()` | Creates a clone of the current object. This is done via recursively traversing all parameters, which corresponds to a deep copy. Calling equals on the cloned object always returns true although none of the memory of both objects overlaps.
`protected `[`CAlphabet`](#classshogun_1_1CAlphabet)` * `[`alphabet`](#classshogun_1_1CStringFeatures_1a88493294578cc18a7dde20cf2b5724e8) | alphabet
`protected int32_t `[`num_vectors`](#classshogun_1_1CStringFeatures_1aa40f93d92d18a300d6175a2ce3b5323d) | number of string vectors (for subset, is updated)
`protected `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`features`](#classshogun_1_1CStringFeatures_1a2f2e5b7c0ed43bb056a6442b14153f89) | this contains the array of features
`protected ST * `[`single_string`](#classshogun_1_1CStringFeatures_1a5fcd702bdd53371d6a153ee3d88776c2) | true when single string / created by sliding window
`protected int32_t `[`length_of_single_string`](#classshogun_1_1CStringFeatures_1a906b9e06301ffb3fcacabdfd4c1a9200) | length of prior single string
`protected int32_t `[`max_string_length`](#classshogun_1_1CStringFeatures_1a637d94815b62628e71969a72fb6974c0) | length of longest string (for subset, is updated)
`protected `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`num_symbols`](#classshogun_1_1CStringFeatures_1a25bc82a714d88505e7ca12db124654ba) | number of used symbols
`protected `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`original_num_symbols`](#classshogun_1_1CStringFeatures_1a3796130f24596ab91fd65aeb01b46787) | original number of used symbols (before higher order mapping)
`protected int32_t `[`order`](#classshogun_1_1CStringFeatures_1a731bcdd52a963edd357941ac5c6fe7fe) | order used in higher order mapping
`protected ST * `[`symbol_mask_table`](#classshogun_1_1CStringFeatures_1a537e7b0449ca873cb190e59dbb76f112) | order used in higher order mapping
`protected int32_t `[`symbol_mask_table_len`](#classshogun_1_1CStringFeatures_1aa0ad4a0d3b52b2dc0bd25195523e94a2) | order used in higher order mapping
`protected bool `[`preprocess_on_get`](#classshogun_1_1CStringFeatures_1ae3f74393763ff7e807e51ef997f07e6f) | preprocess on-the-fly?
`protected `[`CCache`](#classshogun_1_1CCache)`< ST > * `[`feature_cache`](#classshogun_1_1CStringFeatures_1af7e0b906d9c25620bec6b55c76436ce9) | feature cache
`protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328) | subset used for index transformations
`protected virtual ST * `[`compute_feature_vector`](#classshogun_1_1CStringFeatures_1a2a0b220860e7b3c30e9947e212ff7452)`(int32_t num,int32_t & len)` | compute feature vector for sample num if target is set the vector is written to target len is returned by reference
`protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` | 
`protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.
`protected virtual void `[`load_serializable_post`](#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.
`protected virtual void `[`save_serializable_pre`](#classshogun_1_1CSGObject_1a44300a33d16909f1bf7a129d19d4ca41)`()` | Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.
`protected virtual void `[`save_serializable_post`](#classshogun_1_1CSGObject_1ab63af4bfbc71bb737703e48425db1aa2)`()` | Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_POST is called.
`protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ac0fdc76cf24d242d99d8d862475131a6)`(`[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` | Registers a class parameter which is identified by a tag. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.
`protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ad06fb7206a6d3cecfb21fb270cdefbc5)`(const std::string & name,const T & value)` | Registers a class parameter which is identified by a name. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.
`protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a430010070f8439a0b49b647fa6f60296)`(const std::string & name,T * value,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` | Puts a pointer to some parameter into the parameter map.
`protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1ad0e74133e14d5cba696532db034671ec)`(const std::string & name,T ** value,S * len,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` | Puts a pointer to some parameter array into the parameter map.
`protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a7e9db200a31d2d1faaca5a83828aeee5)`(const std::string & name,T ** value,S * rows,S * cols,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` | Puts a pointer to some 2d parameter array (i.e. a matrix) into the parameter map.
`protected template<>`  <br/>`inline void `[`watch_method`](#classshogun_1_1CSGObject_1ad4c5a49c32b7640f955bd3c2ca844b8f)`(const std::string & name,T(S::*)() const method)` | Puts a pointer to a (lazily evaluated) function into the parameter map.
`protected virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`create_empty`](#classshogun_1_1CSGObject_1adf79c57eee99ece954548a61ca38cd80)`() const` | Returns an empty instance of own type.
`protected void `[`observe`](#classshogun_1_1CSGObject_1ab7f66a33081e42252d9c0bb971bbb019)`(const `[`ObservedValue`](#classshogun_1_1ObservedValue)` value)` | Observe a parameter value and emit them to observer. 
`protected void `[`register_observable_param`](#classshogun_1_1CSGObject_1a0fe3525aebc1dd5896191740320e20cd)`(const std::string & name,const `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type,const std::string & description)` | Register which params this object can emit. 
`typedef `[`SGSubject`](#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267) | Definition of observed subject
`typedef `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556) | Definition of observable
`typedef `[`SGSubscriber`](#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8) | Definition of subscriber

## Members

#### `public `[`SGIO`](#classshogun_1_1SGIO)` * `[`io`](#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d) {#classshogun_1_1CSGObject_1ab3ff22f724961ace985100941ba0364d}

io

#### `public `[`Parallel`](#classshogun_1_1Parallel)` * `[`parallel`](#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9) {#classshogun_1_1CSGObject_1a1401044636b5c2353226b974526302e9}

parallel

#### `public `[`Version`](#classshogun_1_1Version)` * `[`version`](#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d) {#classshogun_1_1CSGObject_1afc25f30ab1a6d04798c360a2ce70b87d}

version

#### `public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_parameters`](#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e) {#classshogun_1_1CSGObject_1a70e59038292e669701bad2af7715aa1e}

parameters

#### `public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_model_selection_parameters`](#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b) {#classshogun_1_1CSGObject_1a113f5ae82840ac3f354f94456c10f59b}

model selection parameters

#### `public `[`Parameter`](#classshogun_1_1Parameter)` * `[`m_gradient_parameters`](#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4) {#classshogun_1_1CSGObject_1ac3f51364b93830b9c9d991cb2d5801f4}

parameters wrt which we can compute gradients

#### `public uint32_t `[`m_hash`](#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41) {#classshogun_1_1CSGObject_1a170f14be9561242f924939c56b372a41}

Hash of parameter values

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1af3981c5803cc1481b8cac5f0a7ab91ef)`()` {#classshogun_1_1CStringFeatures_1af3981c5803cc1481b8cac5f0a7ab91ef}

default constructor

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1afa9617ef957fa4ecccbc0d4c0719de51)`(`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` alpha)` {#classshogun_1_1CStringFeatures_1afa9617ef957fa4ecccbc0d4c0719de51}

constructor

#### Parameters
* `alpha` alphabet (type) to use for string features

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a1857f28eb5d6d748887240b7da69d1f5)`(`[`SGStringList`](#classshogun_1_1SGStringList)`< ST > string_list,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` alpha)` {#classshogun_1_1CStringFeatures_1a1857f28eb5d6d748887240b7da69d1f5}

constructor

#### Parameters
* `string_list` 

* `alpha` alphabet (type) to use for string features

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a411fc928305d6a224806366d209a6e6f)`(`[`SGStringList`](#classshogun_1_1SGStringList)`< ST > string_list,`[`CAlphabet`](#classshogun_1_1CAlphabet)` * alpha)` {#classshogun_1_1CStringFeatures_1a411fc928305d6a224806366d209a6e6f}

constructor

#### Parameters
* `string_list` 

* `alpha` an actual alphabet

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a27dc9b9a3d1f7f7c57070c3083ef3ced)`(`[`CAlphabet`](#classshogun_1_1CAlphabet)` * alpha)` {#classshogun_1_1CStringFeatures_1a27dc9b9a3d1f7f7c57070c3083ef3ced}

constructor

#### Parameters
* `alpha` alphabet to use for string features

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1abe8ee4c991bd1573e0ef40a6c8068576)`(const `[`CStringFeatures`](#classshogun_1_1CStringFeatures)` & orig)` {#classshogun_1_1CStringFeatures_1abe8ee4c991bd1573e0ef40a6c8068576}

copy constructor

#### Parameters
* `orig` features to copy

#### `public  `[`CStringFeatures`](#classshogun_1_1CStringFeatures_1a520bb0b8b9d06d74b995645b91fa69ba)`(`[`CFile`](#classshogun_1_1CFile)` * loader,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` alpha)` {#classshogun_1_1CStringFeatures_1a520bb0b8b9d06d74b995645b91fa69ba}

constructor

#### Parameters
* `loader` File object via which to load data 

* `alpha` alphabet (type) to use for string features

#### `public virtual  `[`~CStringFeatures`](#classshogun_1_1CStringFeatures_1a44d3e600d45c117486fed711e5a6b4dd)`()` {#classshogun_1_1CStringFeatures_1a44d3e600d45c117486fed711e5a6b4dd}

destructor

#### `public virtual void `[`cleanup`](#classshogun_1_1CStringFeatures_1a4b66d5e31b5dc18b314c8a68163263bd)`()` {#classshogun_1_1CStringFeatures_1a4b66d5e31b5dc18b314c8a68163263bd}

cleanup string features.

removes any subset before

#### `public virtual void `[`cleanup_feature_vector`](#classshogun_1_1CStringFeatures_1a73082e442a1c84e69995a6fc6bb03305)`(int32_t num)` {#classshogun_1_1CStringFeatures_1a73082e442a1c84e69995a6fc6bb03305}

cleanup a single feature vector

possible with subset

#### Parameters
* `num` number of the vector

#### `public virtual void `[`cleanup_feature_vectors`](#classshogun_1_1CStringFeatures_1a128339a3051e17cbbb6583b648b86f3d)`(int32_t start,int32_t stop)` {#classshogun_1_1CStringFeatures_1a128339a3051e17cbbb6583b648b86f3d}

cleanup multiple feature vectors

possible with subset

#### Parameters
* `start` index of first vector to be cleaned 

* `stop` index of the last vector to be cleaned

#### `public virtual `[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` `[`get_feature_class`](#classshogun_1_1CStringFeatures_1ae83dd54e69a4e8f1c7a571545fa1c8c1)`() const` {#classshogun_1_1CStringFeatures_1ae83dd54e69a4e8f1c7a571545fa1c8c1}

get feature class

#### Returns
feature class STRING

#### `public virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CStringFeatures_1ab0a6eabf1ffd31e38a03365bdaaba64d)`() const` {#classshogun_1_1CStringFeatures_1ab0a6eabf1ffd31e38a03365bdaaba64d}

get feature type

#### Returns
templated feature type

#### `public `[`CAlphabet`](#classshogun_1_1CAlphabet)` * `[`get_alphabet`](#classshogun_1_1CStringFeatures_1a982d8d0f54d9ceaf7d187dba7031a591)`()` {#classshogun_1_1CStringFeatures_1a982d8d0f54d9ceaf7d187dba7031a591}

get alphabet used in string features

#### Returns
alphabet

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`duplicate`](#classshogun_1_1CStringFeatures_1a451c5fd7954842d7a19f1b0faa710e0c)`() const` {#classshogun_1_1CStringFeatures_1a451c5fd7954842d7a19f1b0faa710e0c}

duplicate feature object

#### Returns
feature object

#### `public `[`SGVector`](#classshogun_1_1SGVector)`< ST > `[`get_feature_vector`](#classshogun_1_1CStringFeatures_1a21e2db18e15e281b91e4ba6cabe747e9)`(int32_t num)` {#classshogun_1_1CStringFeatures_1a21e2db18e15e281b91e4ba6cabe747e9}

get string for selected example num

possible with subset

#### Parameters
* `num` index of the string 

#### Returns
the selected string

#### `public void `[`set_feature_vector`](#classshogun_1_1CStringFeatures_1affd56f6e718d53ead36a9b67e53055cc)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > vector,int32_t num)` {#classshogun_1_1CStringFeatures_1affd56f6e718d53ead36a9b67e53055cc}

set string for selected example num

not possible with subset

#### Parameters
* `vector` string to set 

* `num` index of the string

#### `public void `[`enable_on_the_fly_preprocessing`](#classshogun_1_1CStringFeatures_1ae8720f87d0db7b8decdb5611d9af84fe)`()` {#classshogun_1_1CStringFeatures_1ae8720f87d0db7b8decdb5611d9af84fe}

call this to preprocess string features upon call to get_feature_vector

#### `public void `[`disable_on_the_fly_preprocessing`](#classshogun_1_1CStringFeatures_1adb8fca2a3a00f5490e2cdbcec40bd233)`()` {#classshogun_1_1CStringFeatures_1adb8fca2a3a00f5490e2cdbcec40bd233}

call this to disable on the fly feature preprocessing upon call to get_feature_vector. Useful when you manually apply preprocessors.

#### `public ST * `[`get_feature_vector`](#classshogun_1_1CStringFeatures_1a16bf23330a09924b5695d4ca7dfbcee9)`(int32_t num,int32_t & len,bool & dofree)` {#classshogun_1_1CStringFeatures_1a16bf23330a09924b5695d4ca7dfbcee9}

get feature vector for sample num

possible with subset

#### Parameters
* `num` index of feature vector 

* `len` length is returned by reference 

* `dofree` whether returned vector must be freed by caller via free_feature_vector 

#### Returns
feature vector for sample num

#### `public `[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< ST > * `[`get_transposed`](#classshogun_1_1CStringFeatures_1adbfc72db66ac3ef7d57583349444b969)`()` {#classshogun_1_1CStringFeatures_1adbfc72db66ac3ef7d57583349444b969}

get a transposed copy of the features

possible with subset

#### Returns
transposed copy

#### `public `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`get_transposed`](#classshogun_1_1CStringFeatures_1a486476c6523978e9e0a3650c3ea60bc9)`(int32_t & num_feat,int32_t & num_vec)` {#classshogun_1_1CStringFeatures_1a486476c6523978e9e0a3650c3ea60bc9}

compute and return the transpose of string features matrix which will be prepocessed. num_feat, num_vectors are returned by reference caller has to clean up

note that strings all have to have same length

possible with subset

#### Parameters
* `num_feat` number of features in matrix 

* `num_vec` number of vectors in matrix 

#### Returns
transposed string features

#### `public void `[`free_feature_vector`](#classshogun_1_1CStringFeatures_1a2f79d81ff5b83d247dfc124e0e1f9a0f)`(ST * feat_vec,int32_t num,bool dofree)` {#classshogun_1_1CStringFeatures_1a2f79d81ff5b83d247dfc124e0e1f9a0f}

free feature vector

possible with subset

#### Parameters
* `feat_vec` feature vector to free 

* `num` index in feature cache, possibly from subset 

* `dofree` if vector should be really deleted

#### `public void `[`free_feature_vector`](#classshogun_1_1CStringFeatures_1a662229cc7fd6fb86b9f3b11323020ef3)`(`[`SGVector`](#classshogun_1_1SGVector)`< ST > feat_vec,int32_t num)` {#classshogun_1_1CStringFeatures_1a662229cc7fd6fb86b9f3b11323020ef3}

free feature vector

possible with subset

#### Parameters
* `feat_vec` feature vector to free 

* `num` index in feature cache, possibly from subset

#### `public virtual ST `[`get_feature`](#classshogun_1_1CStringFeatures_1a3ec6ee2d63518d13eada2974b8d0fdff)`(int32_t vec_num,int32_t feat_num)` {#classshogun_1_1CStringFeatures_1a3ec6ee2d63518d13eada2974b8d0fdff}

get feature

possible with subset

#### Parameters
* `vec_num` which vector 

* `feat_num` which feature, possibly from subset 

#### Returns
feature

#### `public virtual int32_t `[`get_vector_length`](#classshogun_1_1CStringFeatures_1ae73eebc4d2d287bf5fbf397130c111bf)`(int32_t vec_num)` {#classshogun_1_1CStringFeatures_1ae73eebc4d2d287bf5fbf397130c111bf}

get vector length

possible with subset

#### Parameters
* `vec_num` which vector, possibly from subset 

#### Returns
length of vector

#### `public virtual int32_t `[`get_max_vector_length`](#classshogun_1_1CStringFeatures_1ab5615e3fa0e2478079a5af5f150cfdec)`()` {#classshogun_1_1CStringFeatures_1ab5615e3fa0e2478079a5af5f150cfdec}

get maximum vector length

this one is updated when a subset is set

#### Returns
maximum vector/string length

#### `public virtual int32_t `[`get_num_vectors`](#classshogun_1_1CStringFeatures_1a25a45bd4c25c9d7d72826dd195a7c696)`() const` {#classshogun_1_1CStringFeatures_1a25a45bd4c25c9d7d72826dd195a7c696}

#### Returns
number of vectors, possibly of subset

#### `public `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_num_symbols`](#classshogun_1_1CStringFeatures_1a3d12833241b07efb89c84fe51c409f7c)`()` {#classshogun_1_1CStringFeatures_1a3d12833241b07efb89c84fe51c409f7c}

get number of symbols

Note: floatmax_t sounds weird, but LONG is not long enough

#### Returns
number of symbols

#### `public `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_max_num_symbols`](#classshogun_1_1CStringFeatures_1ab8564e65079bcc45e117444488fcfb31)`()` {#classshogun_1_1CStringFeatures_1ab8564e65079bcc45e117444488fcfb31}

get maximum number of symbols

Note: floatmax_t sounds weird, but int64_t is not long enough (and there is no int128_t type)

#### Returns
maximum number of symbols

#### `public `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_original_num_symbols`](#classshogun_1_1CStringFeatures_1a827e4186e45b5fca5fb5308675cb0a55)`()` {#classshogun_1_1CStringFeatures_1a827e4186e45b5fca5fb5308675cb0a55}

number of symbols before higher order mapping

#### Returns
original number of symbols

#### `public int32_t `[`get_order`](#classshogun_1_1CStringFeatures_1a768f3ae46d11695373dc33824e9cc586)`()` {#classshogun_1_1CStringFeatures_1a768f3ae46d11695373dc33824e9cc586}

order used for higher order mapping

#### Returns
order

#### `public ST `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1a7001733fe224942487be9f8715b52a8c)`(ST symbol,uint8_t mask)` {#classshogun_1_1CStringFeatures_1a7001733fe224942487be9f8715b52a8c}

a higher order mapped symbol will be shaped such that the symbols specified by bits in the mask will be returned.

#### Parameters
* `symbol` symbol to mask 

* `mask` mask to apply 

#### Returns
masked symbol

#### `public ST `[`shift_offset`](#classshogun_1_1CStringFeatures_1ae96e78b74c95f7b25d1e4624b2d5d8a4)`(ST offset,int32_t amount)` {#classshogun_1_1CStringFeatures_1ae96e78b74c95f7b25d1e4624b2d5d8a4}

shift offset to the left by amount

#### Parameters
* `offset` offset to shift 

* `amount` amount to shift the offset 

#### Returns
shifted offset

#### `public ST `[`shift_symbol`](#classshogun_1_1CStringFeatures_1ae88ac8772d7c21ce98833c7c2cdefa9c)`(ST symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1ae88ac8772d7c21ce98833c7c2cdefa9c}

shift symbol to the right by amount (taking care of custom symbol sizes)

#### Parameters
* `symbol` symbol to shift 

* `amount` amount to shift the symbol 

#### Returns
shifted symbol

#### `public virtual void `[`load`](#classshogun_1_1CStringFeatures_1a3855e09ef07683f41271b023b6b95e9d)`(`[`CFile`](#classshogun_1_1CFile)` * loader)` {#classshogun_1_1CStringFeatures_1a3855e09ef07683f41271b023b6b95e9d}

load features from file

#### Parameters
* `loader` File object via which to load data

#### `public void `[`load_ascii_file`](#classshogun_1_1CStringFeatures_1a3a4d55be0f1a9e0b4fb385995fc1910d)`(char * fname,bool remap_to_bin,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` ascii_alphabet,`[`EAlphabet`](#namespaceshogun_1a7fffbfce3d76cf49bde3916d23186b03)` binary_alphabet)` {#classshogun_1_1CStringFeatures_1a3a4d55be0f1a9e0b4fb385995fc1910d}

load ascii line-based string features from file.

any subset is removed before

#### Parameters
* `fname` filename to load from 

* `remap_to_bin` if translation to other binary alphabet should be performed 

* `ascii_alphabet` src alphabet 

* `binary_alphabet` alphabet to translate to

#### `public bool `[`load_fasta_file`](#classshogun_1_1CStringFeatures_1a2a271323306e65ba097fe1b5e91c862c)`(const char * fname,bool ignore_invalid)` {#classshogun_1_1CStringFeatures_1a2a271323306e65ba097fe1b5e91c862c}

load fasta file as string features

any subset is removed before

#### Parameters
* `fname` filename to load from 

* `ignore_invalid` if set to true, characters other than A,C,G,T are converted to A 

#### Returns
if loading was successful

#### `public bool `[`load_fastq_file`](#classshogun_1_1CStringFeatures_1afe8b54317b3d56b85004d2c84632e0ca)`(const char * fname,bool ignore_invalid,bool bitremap_in_single_string)` {#classshogun_1_1CStringFeatures_1afe8b54317b3d56b85004d2c84632e0ca}

load fastq file as string features

removes subset beforehand

#### Parameters
* `fname` filename to load from 

* `ignore_invalid` if set to true, characters other than A,C,G,T are converted to A 

* `bitremap_in_single_string` if set to true, do binary embedding of symbols 

#### Returns
if loading was successful

#### `public bool `[`load_from_directory`](#classshogun_1_1CStringFeatures_1a62097a72b81d6a256c85a2302f81750a)`(char * dirname)` {#classshogun_1_1CStringFeatures_1a62097a72b81d6a256c85a2302f81750a}

load features from directory

removes subset before

#### Parameters
* `dirname` directory name to load from 

#### Returns
if loading was successful

#### `public void `[`set_features`](#classshogun_1_1CStringFeatures_1ac7dd73af410c92b1b62826d33030736b)`(`[`SGStringList`](#classshogun_1_1SGStringList)`< ST > feats)` {#classshogun_1_1CStringFeatures_1ac7dd73af410c92b1b62826d33030736b}

set features

not possible with subset

#### `public bool `[`set_features`](#classshogun_1_1CStringFeatures_1a4fdad0274be1a00b81b0c5ed6cac2cab)`(`[`SGString`](#classshogun_1_1SGString)`< ST > * p_features,int32_t p_num_vectors,int32_t p_max_string_length)` {#classshogun_1_1CStringFeatures_1a4fdad0274be1a00b81b0c5ed6cac2cab}

set features

not possible with subset

#### Parameters
* `p_features` new features 

* `p_num_vectors` number of vectors 

* `p_max_string_length` maximum string length 

#### Returns
if setting was successful

#### `public bool `[`append_features`](#classshogun_1_1CStringFeatures_1ad81d9b128d2ca029ee7ec65a7619806c)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< ST > * sf)` {#classshogun_1_1CStringFeatures_1ad81d9b128d2ca029ee7ec65a7619806c}

append features If the given string features have a subset, only this will be copied

not possible with subset

#### Parameters
* `sf` features to append 

#### Returns
if setting was successful

#### `public bool `[`append_features`](#classshogun_1_1CStringFeatures_1a413d448b8eabaa5704bfa0a5d4407827)`(`[`SGString`](#classshogun_1_1SGString)`< ST > * p_features,int32_t p_num_vectors,int32_t p_max_string_length)` {#classshogun_1_1CStringFeatures_1a413d448b8eabaa5704bfa0a5d4407827}

append features

not possible with subset

#### Parameters
* `p_features` features to append 

* `p_num_vectors` number of vectors 

* `p_max_string_length` maximum string length

note that p_features will be SG_FREE()'d on success

#### Returns
if setting was successful

#### `public `[`SGStringList`](#classshogun_1_1SGStringList)`< ST > `[`get_features`](#classshogun_1_1CStringFeatures_1afeacc8f3ce2fa5a3f72fe2c0f2471ebb)`()` {#classshogun_1_1CStringFeatures_1afeacc8f3ce2fa5a3f72fe2c0f2471ebb}

get_features 
#### Returns
features

#### `public virtual `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`get_features`](#classshogun_1_1CStringFeatures_1ad5daea541f34703b851c2c1a31dd8e0a)`(int32_t & num_str,int32_t & max_str_len)` {#classshogun_1_1CStringFeatures_1ad5daea541f34703b851c2c1a31dd8e0a}

get_features

not possible with subset

#### Parameters
* `num_str` number of strings (returned) 

* `max_str_len` maximal string length (returned) 

#### Returns
string features

#### `public virtual `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`copy_features`](#classshogun_1_1CStringFeatures_1a1f4a76767c06fa82d22179adfeb1c8b2)`(int32_t & num_str,int32_t & max_str_len)` {#classshogun_1_1CStringFeatures_1a1f4a76767c06fa82d22179adfeb1c8b2}

copy_features

possible with subset

#### Parameters
* `num_str` number of strings (returned) 

* `max_str_len` maximal string length (returned) 

#### Returns
string features

#### `public virtual void `[`get_features`](#classshogun_1_1CStringFeatures_1aebb80574ee50e0cf8ae4b936c5db21b4)`(`[`SGString`](#classshogun_1_1SGString)`< ST > ** dst,int32_t * num_str)` {#classshogun_1_1CStringFeatures_1aebb80574ee50e0cf8ae4b936c5db21b4}

get_features (swig compatible)

possible with subset

#### Parameters
* `dst` string features (returned) 

* `num_str` number of strings (returned)

#### `public virtual void `[`save`](#classshogun_1_1CStringFeatures_1ad3e5050e8b6b2f97e3f8894bb688e1f1)`(`[`CFile`](#classshogun_1_1CFile)` * writer)` {#classshogun_1_1CStringFeatures_1ad3e5050e8b6b2f97e3f8894bb688e1f1}

save features to file

not possible with subset

#### Parameters
* `writer` File object via which to save data

#### `public virtual bool `[`load_compressed`](#classshogun_1_1CStringFeatures_1ac843a07f509e48ccaedd7eb857f11230)`(char * src,bool decompress)` {#classshogun_1_1CStringFeatures_1ac843a07f509e48ccaedd7eb857f11230}

load compressed features from file

any subset is removed before

#### Parameters
* `src` filename to load from 

* `decompress` whether to decompress on loading 

#### Returns
if loading was successful

#### `public virtual bool `[`save_compressed`](#classshogun_1_1CStringFeatures_1a4dc4fbf952dd0e43172a879b967fe6a9)`(char * dest,`[`E_COMPRESSION_TYPE`](#namespaceshogun_1a40ddde55c6601043ad2ade2da936c98f)` compression,int level)` {#classshogun_1_1CStringFeatures_1a4dc4fbf952dd0e43172a879b967fe6a9}

save compressed features to file

not possible with subset

#### Parameters
* `dest` filename to save to 

* `compression` compressor to use 

* `level` compression level to use (1-9) 

#### Returns
if saving was successful

#### `public int32_t `[`obtain_by_sliding_window`](#classshogun_1_1CStringFeatures_1a78b86f6c8b9ae4ed75330a037d3dcc91)`(int32_t window_size,int32_t step_size,int32_t skip)` {#classshogun_1_1CStringFeatures_1a78b86f6c8b9ae4ed75330a037d3dcc91}

slides a window of size window_size over the current single string step_size is the amount by which the window is shifted. creates (string_len-window_size)/step_size many feature obj if skip is nonzero, skip the first 'skip' characters of each string

not implemented for subset

#### Parameters
* `window_size` window size 

* `step_size` step size 

* `skip` skip 

#### Returns
something inty

#### `public int32_t `[`obtain_by_position_list`](#classshogun_1_1CStringFeatures_1ac8ab24077fbd94a19f7ad1447e9b9d84)`(int32_t window_size,`[`CDynamicArray`](#classshogun_1_1CDynamicArray)`< int32_t > * positions,int32_t skip)` {#classshogun_1_1CStringFeatures_1ac8ab24077fbd94a19f7ad1447e9b9d84}

extracts windows of size window_size from first string using the positions in list

not implemented for subset

#### Parameters
* `window_size` window size 

* `positions` positions 

* `skip` skip 

#### Returns
something inty

#### `public bool `[`obtain_from_char`](#classshogun_1_1CStringFeatures_1a043ecbf5656c295df1621a4aeac73c47)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< char > * sf,int32_t start,int32_t p_order,int32_t gap,bool rev)` {#classshogun_1_1CStringFeatures_1a043ecbf5656c295df1621a4aeac73c47}

obtain string features from char features

wrapper for template method

any subset is removed before, subset of parameter sf is possible

#### Parameters
* `sf` string features 

* `start` start 

* `p_order` order 

* `gap` gap 

* `rev` reverse 

#### Returns
if obtaining was successful

#### `public template<>`  <br/>`bool `[`obtain_from_char_features`](#classshogun_1_1CStringFeatures_1add0e22e74e445ced1368f42acafa055b)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< CT > * sf,int32_t start,int32_t p_order,int32_t gap,bool rev)` {#classshogun_1_1CStringFeatures_1add0e22e74e445ced1368f42acafa055b}

template obtain from char features

any subset is removed before, subset of parameter sf is possible

#### Parameters
* `sf` string features 

* `start` start 

* `p_order` order 

* `gap` gap 

* `rev` reverse 

#### Returns
if obtaining was successful

#### `public bool `[`have_same_length`](#classshogun_1_1CStringFeatures_1a0941c0a0837b8647d7aa97617b23133b)`(int32_t len)` {#classshogun_1_1CStringFeatures_1a0941c0a0837b8647d7aa97617b23133b}

check if length of each vector in this feature object equals the given length. if existant, only subset is checked

possible for subset

#### Parameters
* `len` vector length to check against 

#### Returns
if length of each vector in this feature object equals the given length.

#### `public void `[`embed_features`](#classshogun_1_1CStringFeatures_1a0e7ec341f4ccf96f4f25a1e55cf3ee63)`(int32_t p_order)` {#classshogun_1_1CStringFeatures_1a0e7ec341f4ccf96f4f25a1e55cf3ee63}

embed string features in bit representation in-place

not implemented for subset

#### `public void `[`compute_symbol_mask_table`](#classshogun_1_1CStringFeatures_1ad3ea9f6809f80b503f81d6ddbc0aecf6)`(int64_t max_val)` {#classshogun_1_1CStringFeatures_1ad3ea9f6809f80b503f81d6ddbc0aecf6}

compute symbol mask table

required to access bit-based symbols

not implemented for subset

#### `public void `[`unembed_word`](#classshogun_1_1CStringFeatures_1aa1b467c0e17ca81bddf2820c3196fc1d)`(ST word,uint8_t * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1aa1b467c0e17ca81bddf2820c3196fc1d}

remap bit-based word to character sequence

#### Parameters
* `word` word to remap 

* `seq` sequence of size len that remapped characters are written to 

* `len` length of sequence and word

#### `public ST `[`embed_word`](#classshogun_1_1CStringFeatures_1a1edd7748e963dce5abb30c49453705fc)`(ST * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1a1edd7748e963dce5abb30c49453705fc}

embed a single word

#### Parameters
* `seq` sequence of size len in a bitfield 

* `len`

#### `public void `[`determine_maximum_string_length`](#classshogun_1_1CStringFeatures_1aea6761787914a98859736a5a998bea44)`()` {#classshogun_1_1CStringFeatures_1aea6761787914a98859736a5a998bea44}

determine new maximum string length

possible with subset

#### `public virtual void `[`set_feature_vector`](#classshogun_1_1CStringFeatures_1a02191fc2d3023a80b7611a1574bede15)`(int32_t num,ST * string,int32_t len)` {#classshogun_1_1CStringFeatures_1a02191fc2d3023a80b7611a1574bede15}

set feature vector for sample num

possible with subset

#### Parameters
* `num` index of feature vector 

* `string` string with the feature vector's content 

* `len` length of the string

#### `public virtual void `[`get_histogram`](#classshogun_1_1CStringFeatures_1a451dc9218ea4aa9c7c3d1bf52fe45eac)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** hist,int32_t * rows,int32_t * cols,bool normalize)` {#classshogun_1_1CStringFeatures_1a451dc9218ea4aa9c7c3d1bf52fe45eac}

compute histogram over strings

possible with subset

#### `public virtual void `[`create_random`](#classshogun_1_1CStringFeatures_1ae0e29f1ce4e8ba243c3c0ffd4981e9b7)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * hist,int32_t rows,int32_t cols,int32_t num_vec)` {#classshogun_1_1CStringFeatures_1ae0e29f1ce4e8ba243c3c0ffd4981e9b7}

create some random strings based on normalized histogram

not possible with subset

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_subset`](#classshogun_1_1CStringFeatures_1adf4a1baaff0c06456ceca3b217c46338)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > indices)` {#classshogun_1_1CStringFeatures_1adf4a1baaff0c06456ceca3b217c46338}

Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing copies of the elements which are specified by the provided indices.

possible with subset

#### Parameters
* `indices` indices of feature elements to copy 

#### Returns
new [CFeatures](#classshogun_1_1CFeatures) instance with copies of feature data

#### `public inline virtual const char * `[`get_name`](#classshogun_1_1CStringFeatures_1a9cb485686dd7a1e6f7103cf42e87717e)`() const` {#classshogun_1_1CStringFeatures_1a9cb485686dd7a1e6f7103cf42e87717e}

#### Returns
object name

#### `public virtual void `[`subset_changed_post`](#classshogun_1_1CStringFeatures_1a401beb1a47c67fc5d23d09e14f39e0f5)`()` {#classshogun_1_1CStringFeatures_1a401beb1a47c67fc5d23d09e14f39e0f5}

post method when subset is changed

#### `public template<>`  <br/>`virtual `[`EFeatureType`](#namespaceshogun_1a064eec90e91f56435546d77f38c0b618)` `[`get_feature_type`](#classshogun_1_1CStringFeatures_1a617d0eeddcb6e6eefd24fb33a2e627cd)`() const` {#classshogun_1_1CStringFeatures_1a617d0eeddcb6e6eefd24fb33a2e627cd}

get feature type the LONGREAL feature can deal with

#### Returns
feature type LONGREAL

#### `public template<>`  <br/>`bool `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1af8364b5d13e2c3115606a318c644850b)`(bool symbol,uint8_t mask)` {#classshogun_1_1CStringFeatures_1af8364b5d13e2c3115606a318c644850b}

#### `public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1a0ba409d902d562af7b0b47e14878e3de)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` symbol,uint8_t mask)` {#classshogun_1_1CStringFeatures_1a0ba409d902d562af7b0b47e14878e3de}

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1af585411821670e9ebf79877c104681e0)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` symbol,uint8_t mask)` {#classshogun_1_1CStringFeatures_1af585411821670e9ebf79877c104681e0}

#### `public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`get_masked_symbols`](#classshogun_1_1CStringFeatures_1aec0bf831702f90a34eb65b71fc0bfaf3)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` symbol,uint8_t mask)` {#classshogun_1_1CStringFeatures_1aec0bf831702f90a34eb65b71fc0bfaf3}

#### `public template<>`  <br/>`bool `[`shift_offset`](#classshogun_1_1CStringFeatures_1ac97945afaa616f198cc839c240ced773)`(bool symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1ac97945afaa616f198cc839c240ced773}

#### `public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`shift_offset`](#classshogun_1_1CStringFeatures_1a9641ce1ede80ca73d451c7566b6f54f8)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1a9641ce1ede80ca73d451c7566b6f54f8}

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`shift_offset`](#classshogun_1_1CStringFeatures_1a1d410816d705897c31a18bd59ca7fa1b)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1a1d410816d705897c31a18bd59ca7fa1b}

#### `public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`shift_offset`](#classshogun_1_1CStringFeatures_1ab62c5acbfa860ebc49c92dc1bb85174b)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1ab62c5acbfa860ebc49c92dc1bb85174b}

#### `public template<>`  <br/>`bool `[`shift_symbol`](#classshogun_1_1CStringFeatures_1a1a486831974b0335fa5a5f4d47e9596d)`(bool symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1a1a486831974b0335fa5a5f4d47e9596d}

#### `public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`shift_symbol`](#classshogun_1_1CStringFeatures_1a78f7a8103d488c2a6f8b3ca77e04bb2d)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1a78f7a8103d488c2a6f8b3ca77e04bb2d}

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`shift_symbol`](#classshogun_1_1CStringFeatures_1ad123531444eb42219d5d2d2adb400d50)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1ad123531444eb42219d5d2d2adb400d50}

#### `public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`shift_symbol`](#classshogun_1_1CStringFeatures_1a4b0a37c772cadfe579132df1e5fc140c)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` symbol,int32_t amount)` {#classshogun_1_1CStringFeatures_1a4b0a37c772cadfe579132df1e5fc140c}

#### `public template<>`  <br/>`bool `[`obtain_from_char_features`](#classshogun_1_1CStringFeatures_1aa69a66b08d7c68567437f42b681cecc7)`(`[`CStringFeatures`](#classshogun_1_1CStringFeatures)`< CT > * sf,int32_t start,int32_t p_order,int32_t gap,bool rev)` {#classshogun_1_1CStringFeatures_1aa69a66b08d7c68567437f42b681cecc7}

#### `public template<>`  <br/>`void `[`embed_features`](#classshogun_1_1CStringFeatures_1a744bb3788b2ec0cea700b18261fa4e8a)`(int32_t p_order)` {#classshogun_1_1CStringFeatures_1a744bb3788b2ec0cea700b18261fa4e8a}

#### `public template<>`  <br/>`void `[`compute_symbol_mask_table`](#classshogun_1_1CStringFeatures_1a3561231c00505210be6036fc672775b8)`(int64_t max_val)` {#classshogun_1_1CStringFeatures_1a3561231c00505210be6036fc672775b8}

#### `public template<>`  <br/>[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` `[`embed_word`](#classshogun_1_1CStringFeatures_1a8fa2e26ed1a0ace65a3687c510dbac29)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1a8fa2e26ed1a0ace65a3687c510dbac29}

#### `public template<>`  <br/>[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`embed_word`](#classshogun_1_1CStringFeatures_1a3b96479a49f7bb69f7c80226734d223a)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1a3b96479a49f7bb69f7c80226734d223a}

#### `public template<>`  <br/>[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`embed_word`](#classshogun_1_1CStringFeatures_1addd1555466d72e8f32eb71a0fb5fdb9a)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1addd1555466d72e8f32eb71a0fb5fdb9a}

#### `public template<>`  <br/>`void `[`unembed_word`](#classshogun_1_1CStringFeatures_1a58a25285389c90da7026f3d4664ab1ed)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` word,uint8_t * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1a58a25285389c90da7026f3d4664ab1ed}

#### `public template<>`  <br/>`void `[`unembed_word`](#classshogun_1_1CStringFeatures_1abc88c03d3adba5765ae4bca857f2bd29)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` word,uint8_t * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1abc88c03d3adba5765ae4bca857f2bd29}

#### `public template<>`  <br/>`void `[`unembed_word`](#classshogun_1_1CStringFeatures_1a9c1f119ec35113bf10542126b5b75bd4)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` word,uint8_t * seq,int32_t len)` {#classshogun_1_1CStringFeatures_1a9c1f119ec35113bf10542126b5b75bd4}

#### `public inline virtual `[`Range`](#classshogun_1_1Range)`< int32_t > `[`index_iterator`](#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd)`() const` {#classshogun_1_1CFeatures_1a71bb6f4167a24d55e8e12fca77baabcd}

returns an iterator of indices from 0 to [CFeatures::get_num_vectors](#classshogun_1_1CFeatures_1a91f8bf82dad4bb05accdc606d85a0da3)

Should be used in algorithms in the following way: 
```cpp
for (auto idx : features->index_iterator()) { ... }
```

#### `public virtual void `[`add_preprocessor`](#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6)`(`[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * p)` {#classshogun_1_1CFeatures_1a53d5b6b17d8e4b44117d404b119faca6}

add preprocessor

#### Parameters
* `p` preprocessor to set

#### `public virtual void `[`del_preprocessor`](#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2)`(int32_t num)` {#classshogun_1_1CFeatures_1af2ad4fb4c64ea892dc73a288f1be27a2}

delete preprocessor from list

#### Parameters
* `num` index of preprocessor in list

#### `public `[`CPreprocessor`](#classshogun_1_1CPreprocessor)` * `[`get_preprocessor`](#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b)`(int32_t num) const` {#classshogun_1_1CFeatures_1a16a2c185a1d7059892ef6ffb2d09f19b}

get specified preprocessor

#### Parameters
* `num` index of preprocessor in list

#### `public int32_t `[`get_num_preprocessors`](#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54)`() const` {#classshogun_1_1CFeatures_1aa1b9b05b4535ba2c8c888aa107321c54}

get number of preprocessors

#### Returns
number of preprocessors

#### `public void `[`clean_preprocessors`](#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2)`()` {#classshogun_1_1CFeatures_1aa6b20826d18617fc3bc0482c73908fb2}

clears all preprocs

#### `public void `[`list_preprocessors`](#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147)`()` {#classshogun_1_1CFeatures_1a476493a28014c60a6006106f3d846147}

print preprocessors

#### `public int32_t `[`get_cache_size`](#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e)`() const` {#classshogun_1_1CFeatures_1a6b599085eff3dab5a66cce6f133ae47e}

get cache size

#### Returns
cache size

#### `public virtual bool `[`reshape`](#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287)`(int32_t num_features,int32_t num_vectors)` {#classshogun_1_1CFeatures_1ad2a12e099e61e61e3872253a13cc0287}

in case there is a feature matrix allow for reshaping

NOT IMPLEMENTED!

#### Parameters
* `num_features` new number of features 

* `num_vectors` new number of vectors 

#### Returns
if reshaping was successful

#### `public void `[`list_feature_obj`](#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7)`() const` {#classshogun_1_1CFeatures_1aff469383824e5b8736c191cd4e4476b7}

list feature object

#### `public bool `[`check_feature_compatibility`](#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * f) const` {#classshogun_1_1CFeatures_1a7fe9c8b9c4e4474b1893f837ea29fa21}

check feature compatibility

#### Parameters
* `f` features to check for compatibility 

#### Returns
if features are compatible

#### `public bool `[`has_property`](#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p) const` {#classshogun_1_1CFeatures_1af181de39b142f32c3bb00a19bea32bcc}

check if features have given property

#### Parameters
* `p` feature property 

#### Returns
if features have given property

#### `public void `[`set_property`](#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` {#classshogun_1_1CFeatures_1a732ec5df91b2d7d80ae25a79fe068055}

set property

#### Parameters
* `p` kernel property to set

#### `public void `[`unset_property`](#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e)`(`[`EFeatureProperty`](#namespaceshogun_1add4a728b32cf3898a63b2ef4564c1925)` p)` {#classshogun_1_1CFeatures_1affaad72e745ecc61e93d676d78705b1e}

unset property

#### Parameters
* `p` kernel property to unset

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e)`(`[`CList`](#classshogun_1_1CList)` * others) const` {#classshogun_1_1CFeatures_1abba142f59793094f4f324787d43e0b4e}

Takes a list of feature instances and returns a new instance being a concatenation of a copy of this instace's data and the given instancess data. Note that the feature types have to be equal.

NOT IMPLEMENTED!

#### Parameters
* `others` list of feature objects to append 

#### Returns
new feature object which contains copy of data of this instance and given ones

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`create_merged_copy`](#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769)`(`[`CFeatures`](#classshogun_1_1CFeatures)` * other) const` {#classshogun_1_1CFeatures_1aef378f04b4eb3b6a21752a5400260769}

Convenience method for method with same name and list as parameter.

NOT IMPLEMENTED!

#### Parameters
* `other` feature object to append 

#### Returns
new feature object which contains copy of data of this instance and of given one

#### `public virtual void `[`add_subset`](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71}

Adds a subset of indices on top of the current subsets (possibly subset of subset). Every call causes a new active index vector to be stored. Added subsets can be removed one-by-one. If this is not needed, [add_subset_in_place()](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31) should be used (does not store intermediate index vectors)

Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### Parameters
* `subset` subset of indices to add

#### `public virtual void `[`add_subset_in_place`](#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > subset)` {#classshogun_1_1CFeatures_1a6dabbf53b34ca64a7645191b8ea04e31}

Sets/changes latest added subset. This allows to add multiple subsets with in-place memory requirements. They cannot be removed one-by-one afterwards, only the latest active can. If this is needed, use [add_subset()](#classshogun_1_1CFeatures_1acb58d8008e2ef9bb83e6b5fc5fb42f71). If no subset is active, this just adds.

Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### Parameters
* `subset` subset of indices to replace the latest one with.

#### `public virtual void `[`remove_subset`](#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172)`()` {#classshogun_1_1CFeatures_1a5c8a113b96b3d3a2d565ed9fffeed172}

removes that last added subset from subset stack, if existing Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### `public virtual void `[`remove_all_subsets`](#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61)`()` {#classshogun_1_1CFeatures_1a434b4feb76767ed0adc9ccdd55a3ef61}

removes all subsets Calls [subset_changed_post()](#classshogun_1_1CFeatures_1a29da7ff7f79717e53ae762891124a4a7) afterwards

#### `public virtual `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`get_subset_stack`](#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253)`()` {#classshogun_1_1CFeatures_1a47944f23a63a0eed56ff3d0bba40d253}

returns subset stack

#### Returns
subset stack

#### `public virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`copy_dimension_subset`](#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5)`(`[`SGVector](#classshogun_1_1SGVector)< [index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` > dims)` {#classshogun_1_1CFeatures_1ab5e4da6272e74503f9ac4405d8ac92b5}

Creates a new [CFeatures](#classshogun_1_1CFeatures) instance containing only the dimensions of the feature vector which are specified by the provided indices.

This method is needed for feature selection tasks NOT IMPLEMENTED!

#### Parameters
* `dims` indices of feature dimensions to copy 

#### Returns
new [CFeatures](#classshogun_1_1CFeatures) instance with copies of specified features

#### `public inline virtual bool `[`support_compatible_class`](#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f)`() const` {#classshogun_1_1CFeatures_1a0e8af4cc2f64bde8fe2b3dd4557e9a4f}

does this class support compatible computation bewteen difference classes? for example, this->dot(rhs_prt), can rhs_prt be an instance of a difference class?

#### Returns
whether this class supports compatible computation

#### `public virtual bool `[`get_feature_class_compatibility`](#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6)`(`[`EFeatureClass`](#namespaceshogun_1a9e2a4d8b86b9e061779c3fdbcda57c3b)` rhs) const` {#classshogun_1_1CFeatures_1a3f98caf024a0a4713f5201f44b71dcd6}

Given a class in right hand side, does this class support compatible computation?

for example, is this->dot(rhs_prt) valid, where rhs_prt is the class in right hand side

#### Parameters
* `rhs` the class in right hand side 

#### Returns
whether this class supports compatible computation

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` {#classshogun_1_1CFeatures_1ad3711d9770e4b96ae8e89a99c9f530f7}

Throws an error, as features are immutable

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be)`(const std::string & name,T * value)` {#classshogun_1_1CSGObject_1ade486add69a3fb33395968d9ad8fc4be}

Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` {#classshogun_1_1CSGObject_1a7c9acb98546f6fab79715f3c151b0de4}

Typed setter for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public template<>`  <br/>`inline void `[`put`](#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d)`(const std::string & name,T value)` {#classshogun_1_1CSGObject_1a21240124c06dd6296b254555e15cbf2d}

Typed setter for a non-object class parameter, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter along with type information

#### `public inline virtual `[`CFeatures`](#classshogun_1_1CFeatures)` * `[`shallow_subset_copy`](#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4)`()` {#classshogun_1_1CFeatures_1a896eb199c1413950bbf9a89226817fb4}

#### `public int32_t `[`ref`](#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a)`()` {#classshogun_1_1CSGObject_1ab8c24b912ee57d3f2c81ecccd083582a}

increase reference counter

#### Returns
reference count

#### `public int32_t `[`ref_count`](#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d)`()` {#classshogun_1_1CSGObject_1a6401d138f63be4c245f1f556f197689d}

display reference counter

#### Returns
reference count

#### `public int32_t `[`unref`](#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01)`()` {#classshogun_1_1CSGObject_1ad99bde1a142a1c07a963169123166e01}

decrement reference counter and deallocate object if refcount is zero before or after decrementing it

#### Returns
reference count

#### `public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`shallow_copy`](#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4)`() const` {#classshogun_1_1CSGObject_1a3a25f61e5062adfce5df46be45e7e8c4}

A shallow copy. All the SGObject instance variables will be simply assigned and SG_REF-ed.

#### `public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`deep_copy`](#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578)`() const` {#classshogun_1_1CSGObject_1afa9949a366159a39ab8118918b57f578}

A deep copy. All the instance variables will also be copied.

#### `public virtual bool `[`is_generic`](#classshogun_1_1CSGObject_1a6801eb416eadc35f5499a48436e1cf43)`(EPrimitiveType * generic) const` {#classshogun_1_1CSGObject_1a6801eb416eadc35f5499a48436e1cf43}

If the SGSerializable is a class template then TRUE will be returned and GENERIC is set to the type of the generic.

#### Parameters
* `generic` set to the type of the generic if returning TRUE

#### Returns
TRUE if a class template.

#### `public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1ad3463e866082d6707af04276ae8aa477)`()` {#classshogun_1_1CSGObject_1ad3463e866082d6707af04276ae8aa477}

set generic type to T

#### `public template<>`  <br/>`void `[`set_generic`](#classshogun_1_1CSGObject_1a9fca24ed1095acc6c52f3c5353156d74)`()` {#classshogun_1_1CSGObject_1a9fca24ed1095acc6c52f3c5353156d74}

#### `public inline EPrimitiveType `[`get_generic`](#classshogun_1_1CSGObject_1a3329cfa1654e757472c9098770635530)`() const` {#classshogun_1_1CSGObject_1a3329cfa1654e757472c9098770635530}

Returns generic type. 
#### Returns
generic type of this object

#### `public void `[`unset_generic`](#classshogun_1_1CSGObject_1aa15afe4277334593139dae884cc951e1)`()` {#classshogun_1_1CSGObject_1aa15afe4277334593139dae884cc951e1}

unset generic type

this has to be called in classes specializing a template class

#### `public virtual void `[`print_serializable`](#classshogun_1_1CSGObject_1ade3b14c2f62ba4d8f2f6422e08567ae9)`(const char * prefix)` {#classshogun_1_1CSGObject_1ade3b14c2f62ba4d8f2f6422e08567ae9}

prints registered parameters out

#### Parameters
* `prefix` prefix for members

#### `public virtual bool `[`save_serializable`](#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#classshogun_1_1CSGObject_1aa9787e341533c4970885ce6d3022a935}

Save this object to file.

#### Parameters
* `file` where to save the object; will be closed during returning if PREFIX is an empty string. 

* `prefix` prefix for members 

#### Returns
TRUE if done, otherwise FALSE

#### `public virtual bool `[`load_serializable`](#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#classshogun_1_1CSGObject_1ad67e38ad80d4152151081f838c0a13e1}

Load this object from file. If it will fail (returning FALSE) then this object will contain inconsistent data and should not be used!

#### Parameters
* `file` where to load from 

* `prefix` prefix for members

#### Returns
TRUE if done, otherwise FALSE

#### `public void `[`set_global_io`](#classshogun_1_1CSGObject_1a36d256e2d05357b57e83f31f7e358f69)`(`[`SGIO`](#classshogun_1_1SGIO)` * io)` {#classshogun_1_1CSGObject_1a36d256e2d05357b57e83f31f7e358f69}

set the io object

#### Parameters
* `io` io object to use

#### `public `[`SGIO`](#classshogun_1_1SGIO)` * `[`get_global_io`](#classshogun_1_1CSGObject_1ac6c994717cb550f81c70129e839ea98b)`()` {#classshogun_1_1CSGObject_1ac6c994717cb550f81c70129e839ea98b}

get the io object

#### Returns
io object

#### `public void `[`set_global_parallel`](#classshogun_1_1CSGObject_1a9543b75e320e477d12553f2aa8593e8a)`(`[`Parallel`](#classshogun_1_1Parallel)` * parallel)` {#classshogun_1_1CSGObject_1a9543b75e320e477d12553f2aa8593e8a}

set the parallel object

#### Parameters
* `parallel` parallel object to use

#### `public `[`Parallel`](#classshogun_1_1Parallel)` * `[`get_global_parallel`](#classshogun_1_1CSGObject_1a2cd3ba36c7e0ef6e5234393cc7e22bb0)`()` {#classshogun_1_1CSGObject_1a2cd3ba36c7e0ef6e5234393cc7e22bb0}

get the parallel object

#### Returns
parallel object

#### `public void `[`set_global_version`](#classshogun_1_1CSGObject_1a1ba2ee8842e30d8ceaaf5d44c567efe1)`(`[`Version`](#classshogun_1_1Version)` * version)` {#classshogun_1_1CSGObject_1a1ba2ee8842e30d8ceaaf5d44c567efe1}

set the version object

#### Parameters
* `version` version object to use

#### `public `[`Version`](#classshogun_1_1Version)` * `[`get_global_version`](#classshogun_1_1CSGObject_1a03ce854ec4f745dbe219533dc36c9e20)`()` {#classshogun_1_1CSGObject_1a03ce854ec4f745dbe219533dc36c9e20}

get the version object

#### Returns
version object

#### `public `[`SGStringList`](#classshogun_1_1SGStringList)`< char > `[`get_modelsel_names`](#classshogun_1_1CSGObject_1a730ecbf7f326b93350f00cc937e59ac0)`()` {#classshogun_1_1CSGObject_1a730ecbf7f326b93350f00cc937e59ac0}

#### Returns
vector of names of all parameters which are registered for model selection

#### `public void `[`print_modsel_params`](#classshogun_1_1CSGObject_1a8dcb739fd760f227b3fa1dc0684f762d)`()` {#classshogun_1_1CSGObject_1a8dcb739fd760f227b3fa1dc0684f762d}

prints all parameter registered for model selection and their type

#### `public char * `[`get_modsel_param_descr`](#classshogun_1_1CSGObject_1ac26fd2403c6a5c334f4a2d8094be9833)`(const char * param_name)` {#classshogun_1_1CSGObject_1ac26fd2403c6a5c334f4a2d8094be9833}

Returns description of a given parameter string, if it exists. SG_ERROR otherwise

#### Parameters
* `param_name` name of the parameter 

#### Returns
description of the parameter

#### `public `[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` `[`get_modsel_param_index`](#classshogun_1_1CSGObject_1aeb1f5a55b8170409ff2a94e3a3664c05)`(const char * param_name)` {#classshogun_1_1CSGObject_1aeb1f5a55b8170409ff2a94e3a3664c05}

Returns index of model selection parameter with provided index

#### Parameters
* `param_name` name of model selection parameter 

#### Returns
index of model selection parameter with provided name, -1 if there is no such

#### `public void `[`build_gradient_parameter_dictionary`](#classshogun_1_1CSGObject_1a17f448c257ccf4083987c4670c86a967)`(`[`CMap](#classshogun_1_1CMap)< [TParameter](#structshogun_1_1TParameter) *, [CSGObject`](#classshogun_1_1CSGObject)` *> * dict)` {#classshogun_1_1CSGObject_1a17f448c257ccf4083987c4670c86a967}

Builds a dictionary of all parameters in SGObject as well of those of SGObjects that are parameters of this object. Dictionary maps parameters to the objects that own them.

#### Parameters
* `dict` dictionary of parameters to be built.

#### `public bool `[`has`](#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424)`(const std::string & name) const` {#classshogun_1_1CSGObject_1aa911ba3ef90e0b3179e0a8dc10586424}

Checks if object has a class parameter identified by a name.

#### Parameters
* `name` name of the parameter 

#### Returns
true if the parameter exists with the input name

#### `public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1a0ba98fe70db33bb2036e76fd4ec28e04)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & tag) const` {#classshogun_1_1CSGObject_1a0ba98fe70db33bb2036e76fd4ec28e04}

Checks if object has a class parameter identified by a [Tag](#classshogun_1_1Tag).

#### Parameters
* `tag` tag of the parameter containing name and type information 

#### Returns
true if the parameter exists with the input tag

#### `public template<>`  <br/>`inline bool `[`has`](#classshogun_1_1CSGObject_1ac947804131f9937507db2da99f36e933)`(const std::string & name) const` {#classshogun_1_1CSGObject_1ac947804131f9937507db2da99f36e933}

Checks if a type exists for a class parameter identified by a name.

#### Parameters
* `name` name of the parameter 

#### Returns
true if the parameter exists with the input name and type

#### `public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a3b1dff76eb6397801f84101060c5956c)`(const std::string & name,T * value)` {#classshogun_1_1CSGObject_1a3b1dff76eb6397801f84101060c5956c}

Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public template<>`  <br/>`inline void `[`add`](#classshogun_1_1CSGObject_1a98738b2423f4eb9cee078924311a9e04)`(const std::string & name,`[`Some`](#classshogun_1_1Some)`< T > value)` {#classshogun_1_1CSGObject_1a98738b2423f4eb9cee078924311a9e04}

Typed appender for an object class parameter of a [Shogun](#classShogun) base class type, identified by a name.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter

#### `public `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get`](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7)`(const std::string & name)` {#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7}

Untyped getter for an object class parameter, identified by a name. Will attempt to get specified object of appropriate internal type.

#### Parameters
* `name` name of the parameter 

#### Returns
object parameter

#### `public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1a081b48e5b14e9ff75e7e56c941870ed5)`(const `[`Tag`](#classshogun_1_1Tag)`< T > & _tag) const` {#classshogun_1_1CSGObject_1a081b48e5b14e9ff75e7e56c941870ed5}

Getter for a class parameter, identified by a [Tag](#classshogun_1_1Tag). Throws an exception if the class does not have such a parameter.

#### Parameters
* `_tag` name and type information of parameter 

#### Returns
value of the parameter identified by the input tag

#### `public template<>`  <br/>`inline T `[`get`](#classshogun_1_1CSGObject_1adeb49b89495067e83e4208d1d60bea60)`(const std::string & name) const` {#classshogun_1_1CSGObject_1adeb49b89495067e83e4208d1d60bea60}

Getter for a class parameter, identified by a name. Throws an exception if the class does not have such a parameter.

#### Parameters
* `name` name of the parameter 

#### Returns
value of the parameter corresponding to the input name and type

#### `public virtual std::string `[`to_string`](#classshogun_1_1CSGObject_1aac993ecccd3d88aafefb6b8e3caa1dee)`() const` {#classshogun_1_1CSGObject_1aac993ecccd3d88aafefb6b8e3caa1dee}

Returns string representation of the object that contains its name and parameters.

#### `public std::vector< std::string > `[`parameter_names`](#classshogun_1_1CSGObject_1a924f620b4718c3367cf5403c52a30074)`() const` {#classshogun_1_1CSGObject_1a924f620b4718c3367cf5403c52a30074}

Returns set of all parameter names of the object.

#### `public template<>`  <br/>`inline T * `[`as`](#classshogun_1_1CSGObject_1aa4cdefb81ca8c583f1c2ef0d20d8feeb)`()` {#classshogun_1_1CSGObject_1aa4cdefb81ca8c583f1c2ef0d20d8feeb}

Specializes the object to the specified type. Throws exception if the object cannot be specialized.

#### Returns
The requested type

#### `public inline `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556)` * `[`get_parameters_observable`](#classshogun_1_1CSGObject_1a539800ba1bbe5a4260df8c5641305afc)`()` {#classshogun_1_1CSGObject_1a539800ba1bbe5a4260df8c5641305afc}

Get parameters observable 
#### Returns
RxCpp observable

#### `public void `[`subscribe_to_parameters`](#classshogun_1_1CSGObject_1aeb13a31ffeb912767b6f16f1bc1d3e61)`(`[`ParameterObserverInterface`](#classshogun_1_1ParameterObserverInterface)` * obs)` {#classshogun_1_1CSGObject_1aeb13a31ffeb912767b6f16f1bc1d3e61}

Subscribe a parameter observer to watch over params

#### `public void `[`list_observable_parameters`](#classshogun_1_1CSGObject_1aac0c9d125edd61f235eeba5efed47142)`()` {#classshogun_1_1CSGObject_1aac0c9d125edd61f235eeba5efed47142}

Print to stdout a list of observable parameters

#### `public virtual void `[`update_parameter_hash`](#classshogun_1_1CSGObject_1afd6d5beea40c6d1222d361fb706d4651)`()` {#classshogun_1_1CSGObject_1afd6d5beea40c6d1222d361fb706d4651}

Updates the hash of current parameter combination

#### `public virtual bool `[`parameter_hash_changed`](#classshogun_1_1CSGObject_1aeb270031640bb2f00ec9452c637bfbc2)`()` {#classshogun_1_1CSGObject_1aeb270031640bb2f00ec9452c637bfbc2}

#### Returns
whether parameter combination has changed since last update

#### `public virtual bool `[`equals`](#classshogun_1_1CSGObject_1afe6a79f0c2c3db09f98ebdbe23a8a5d9)`(const `[`CSGObject`](#classshogun_1_1CSGObject)` * other) const` {#classshogun_1_1CSGObject_1afe6a79f0c2c3db09f98ebdbe23a8a5d9}

Deep comparison of two objects.

#### Parameters
* `other` object to compare with 

#### Returns
true if all parameters are equal

#### `public virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`clone`](#classshogun_1_1CSGObject_1a4ae46a8c294896b69fc21384f6d86fad)`()` {#classshogun_1_1CSGObject_1a4ae46a8c294896b69fc21384f6d86fad}

Creates a clone of the current object. This is done via recursively traversing all parameters, which corresponds to a deep copy. Calling equals on the cloned object always returns true although none of the memory of both objects overlaps.

#### Returns
an identical copy of the given object, which is disjoint in memory. NULL if the clone fails. Note that the returned object is SG_REF'ed

#### `protected `[`CAlphabet`](#classshogun_1_1CAlphabet)` * `[`alphabet`](#classshogun_1_1CStringFeatures_1a88493294578cc18a7dde20cf2b5724e8) {#classshogun_1_1CStringFeatures_1a88493294578cc18a7dde20cf2b5724e8}

alphabet

#### `protected int32_t `[`num_vectors`](#classshogun_1_1CStringFeatures_1aa40f93d92d18a300d6175a2ce3b5323d) {#classshogun_1_1CStringFeatures_1aa40f93d92d18a300d6175a2ce3b5323d}

number of string vectors (for subset, is updated)

#### `protected `[`SGString`](#classshogun_1_1SGString)`< ST > * `[`features`](#classshogun_1_1CStringFeatures_1a2f2e5b7c0ed43bb056a6442b14153f89) {#classshogun_1_1CStringFeatures_1a2f2e5b7c0ed43bb056a6442b14153f89}

this contains the array of features

#### `protected ST * `[`single_string`](#classshogun_1_1CStringFeatures_1a5fcd702bdd53371d6a153ee3d88776c2) {#classshogun_1_1CStringFeatures_1a5fcd702bdd53371d6a153ee3d88776c2}

true when single string / created by sliding window

#### `protected int32_t `[`length_of_single_string`](#classshogun_1_1CStringFeatures_1a906b9e06301ffb3fcacabdfd4c1a9200) {#classshogun_1_1CStringFeatures_1a906b9e06301ffb3fcacabdfd4c1a9200}

length of prior single string

#### `protected int32_t `[`max_string_length`](#classshogun_1_1CStringFeatures_1a637d94815b62628e71969a72fb6974c0) {#classshogun_1_1CStringFeatures_1a637d94815b62628e71969a72fb6974c0}

length of longest string (for subset, is updated)

#### `protected `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`num_symbols`](#classshogun_1_1CStringFeatures_1a25bc82a714d88505e7ca12db124654ba) {#classshogun_1_1CStringFeatures_1a25bc82a714d88505e7ca12db124654ba}

number of used symbols

#### `protected `[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` `[`original_num_symbols`](#classshogun_1_1CStringFeatures_1a3796130f24596ab91fd65aeb01b46787) {#classshogun_1_1CStringFeatures_1a3796130f24596ab91fd65aeb01b46787}

original number of used symbols (before higher order mapping)

#### `protected int32_t `[`order`](#classshogun_1_1CStringFeatures_1a731bcdd52a963edd357941ac5c6fe7fe) {#classshogun_1_1CStringFeatures_1a731bcdd52a963edd357941ac5c6fe7fe}

order used in higher order mapping

#### `protected ST * `[`symbol_mask_table`](#classshogun_1_1CStringFeatures_1a537e7b0449ca873cb190e59dbb76f112) {#classshogun_1_1CStringFeatures_1a537e7b0449ca873cb190e59dbb76f112}

order used in higher order mapping

#### `protected int32_t `[`symbol_mask_table_len`](#classshogun_1_1CStringFeatures_1aa0ad4a0d3b52b2dc0bd25195523e94a2) {#classshogun_1_1CStringFeatures_1aa0ad4a0d3b52b2dc0bd25195523e94a2}

order used in higher order mapping

#### `protected bool `[`preprocess_on_get`](#classshogun_1_1CStringFeatures_1ae3f74393763ff7e807e51ef997f07e6f) {#classshogun_1_1CStringFeatures_1ae3f74393763ff7e807e51ef997f07e6f}

preprocess on-the-fly?

#### `protected `[`CCache`](#classshogun_1_1CCache)`< ST > * `[`feature_cache`](#classshogun_1_1CStringFeatures_1af7e0b906d9c25620bec6b55c76436ce9) {#classshogun_1_1CStringFeatures_1af7e0b906d9c25620bec6b55c76436ce9}

feature cache

#### `protected `[`CSubsetStack`](#classshogun_1_1CSubsetStack)` * `[`m_subset_stack`](#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328) {#classshogun_1_1CFeatures_1ac406fc1620ad5a8714a1c34c935ae328}

subset used for index transformations

#### `protected virtual ST * `[`compute_feature_vector`](#classshogun_1_1CStringFeatures_1a2a0b220860e7b3c30e9947e212ff7452)`(int32_t num,int32_t & len)` {#classshogun_1_1CStringFeatures_1a2a0b220860e7b3c30e9947e212ff7452}

compute feature vector for sample num if target is set the vector is written to target len is returned by reference

possible with subset

#### Parameters
* `num` which vector 

* `len` length of vector 

#### Returns
feature vector

#### `protected template<>`  <br/>`inline `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`get_sgobject_type_dispatcher`](#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1)`(const std::string & name)` {#classshogun_1_1CSGObject_1a7de7c1e11c3d4322d74a9a8cf5cc13f1}

#### `protected virtual void `[`load_serializable_pre`](#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790)`()` {#classshogun_1_1CSGObject_1a7361535fc1a8b13beb9dd0b4ac2dd790}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected virtual void `[`load_serializable_post`](#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2)`()` {#classshogun_1_1CSGObject_1a4c8da771d1ddf319cabc6b9e896326f2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::LOAD_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected virtual void `[`save_serializable_pre`](#classshogun_1_1CSGObject_1a44300a33d16909f1bf7a129d19d4ca41)`()` {#classshogun_1_1CSGObject_1a44300a33d16909f1bf7a129d19d4ca41}

Can (optionally) be overridden to pre-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_PRE is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected virtual void `[`save_serializable_post`](#classshogun_1_1CSGObject_1ab63af4bfbc71bb737703e48425db1aa2)`()` {#classshogun_1_1CSGObject_1ab63af4bfbc71bb737703e48425db1aa2}

Can (optionally) be overridden to post-initialize some member variables which are not PARAMETER::ADD'ed. Make sure that at first the overridden method BASE_CLASS::SAVE_SERIALIZABLE_POST is called.

#### Exceptions
* `[ShogunException](#classshogun_1_1ShogunException)` will be thrown if an error occurs.

#### `protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ac0fdc76cf24d242d99d8d862475131a6)`(`[`Tag`](#classshogun_1_1Tag)`< T > & _tag,const T & value)` {#classshogun_1_1CSGObject_1ac0fdc76cf24d242d99d8d862475131a6}

Registers a class parameter which is identified by a tag. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.

#### Parameters
* `_tag` name and type information of parameter 

* `value` value of the parameter

#### `protected template<>`  <br/>`inline void `[`register_param`](#classshogun_1_1CSGObject_1ad06fb7206a6d3cecfb21fb270cdefbc5)`(const std::string & name,const T & value)` {#classshogun_1_1CSGObject_1ad06fb7206a6d3cecfb21fb270cdefbc5}

Registers a class parameter which is identified by a name. This enables the parameter to be modified by [put()](#classshogun_1_1CSGObject_1ad3711d9770e4b96ae8e89a99c9f530f7) and retrieved by [get()](#classshogun_1_1CSGObject_1a4de6e15966500093d2c04db29bbf4ac7). Parameters can be registered in the constructor of the class.

#### Parameters
* `name` name of the parameter 

* `value` value of the parameter along with type information

#### `protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a430010070f8439a0b49b647fa6f60296)`(const std::string & name,T * value,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` {#classshogun_1_1CSGObject_1a430010070f8439a0b49b647fa6f60296}

Puts a pointer to some parameter into the parameter map.

#### Parameters
* `name` name of the parameter 

* `value` pointer to the parameter value 

* `properties` properties of the parameter (e.g. if model selection is supported)

#### `protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1ad0e74133e14d5cba696532db034671ec)`(const std::string & name,T ** value,S * len,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` {#classshogun_1_1CSGObject_1ad0e74133e14d5cba696532db034671ec}

Puts a pointer to some parameter array into the parameter map.

#### Parameters
* `name` name of the parameter array 

* `value` pointer to the first element of the parameter array 

* `len` number of elements in the array 

* `properties` properties of the parameter (e.g. if model selection is supported)

#### `protected template<>`  <br/>`inline void `[`watch_param`](#classshogun_1_1CSGObject_1a7e9db200a31d2d1faaca5a83828aeee5)`(const std::string & name,T ** value,S * rows,S * cols,`[`AnyParameterProperties`](#classshogun_1_1AnyParameterProperties)` properties)` {#classshogun_1_1CSGObject_1a7e9db200a31d2d1faaca5a83828aeee5}

Puts a pointer to some 2d parameter array (i.e. a matrix) into the parameter map.

#### Parameters
* `name` name of the parameter array 

* `value` pointer to the first element of the parameter array 

* `rows` number of rows in the array 

* `cols` number of columns in the array 

* `properties` properties of the parameter (e.g. if model selection is supported)

#### `protected template<>`  <br/>`inline void `[`watch_method`](#classshogun_1_1CSGObject_1ad4c5a49c32b7640f955bd3c2ca844b8f)`(const std::string & name,T(S::*)() const method)` {#classshogun_1_1CSGObject_1ad4c5a49c32b7640f955bd3c2ca844b8f}

Puts a pointer to a (lazily evaluated) function into the parameter map.

#### Parameters
* `name` name of the parameter 

* `method` pointer to the method

#### `protected virtual `[`CSGObject`](#classshogun_1_1CSGObject)` * `[`create_empty`](#classshogun_1_1CSGObject_1adf79c57eee99ece954548a61ca38cd80)`() const` {#classshogun_1_1CSGObject_1adf79c57eee99ece954548a61ca38cd80}

Returns an empty instance of own type.

When inheriting from [CSGObject](#classshogun_1_1CSGObject) from outside the main source tree (i.e. customized classes, or in a unit test), then this method has to be overloaded manually to return an empty instance. [Shogun](#classShogun) can only instantiate empty class instances from its source tree.

#### Returns
empty instance of own type

#### `protected void `[`observe`](#classshogun_1_1CSGObject_1ab7f66a33081e42252d9c0bb971bbb019)`(const `[`ObservedValue`](#classshogun_1_1ObservedValue)` value)` {#classshogun_1_1CSGObject_1ab7f66a33081e42252d9c0bb971bbb019}

Observe a parameter value and emit them to observer. 
#### Parameters
* `value` Observed parameter's value

#### `protected void `[`register_observable_param`](#classshogun_1_1CSGObject_1a0fe3525aebc1dd5896191740320e20cd)`(const std::string & name,const `[`SG_OBS_VALUE_TYPE`](#namespaceshogun_1adcef34436f03207dcc3b97db8b4794d9)` type,const std::string & description)` {#classshogun_1_1CSGObject_1a0fe3525aebc1dd5896191740320e20cd}

Register which params this object can emit. 
#### Parameters
* `name` the param name 

* `type` the param type 

* `description` a user oriented description

#### `typedef `[`SGSubject`](#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267) {#classshogun_1_1CSGObject_1a52509313192ce488ae91f9d7e2b16267}

Definition of observed subject

#### `typedef `[`SGObservable`](#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556) {#classshogun_1_1CSGObject_1a3f344a622ab6c3e0dd73b5dd3f7aa556}

Definition of observable

#### `typedef `[`SGSubscriber`](#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8) {#classshogun_1_1CSGObject_1a658eb47ba606529e8ffc5090d36e34e8}

Definition of subscriber

