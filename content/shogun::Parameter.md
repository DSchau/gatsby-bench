---
classname: "shogun::Parameter"
type: "class"
---

# class `shogun::Parameter` {#classshogun_1_1Parameter}

[Parameter](#classshogun_1_1Parameter) class.

Must not be an [CSGObject](#classshogun_1_1CSGObject) to prevent a recursive call of constructors.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public  explicit `[`Parameter`](#classshogun_1_1Parameter_1a722d0b273a6e3633c189fb21eaaa483c)`()` | explicit constructor
`public virtual  `[`~Parameter`](#classshogun_1_1Parameter_1a615c436bf6b0250e3518ba91a5d88f66)`()` | destructor
`public virtual void `[`print`](#classshogun_1_1Parameter_1acfb5f363d75656e9b4686794fa9a18f9)`(const char * prefix)` | print 
`public virtual bool `[`save`](#classshogun_1_1Parameter_1af5f394df0bf09bc2409808804f7e8c8b)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | save to serializable file 
`public virtual bool `[`load`](#classshogun_1_1Parameter_1aec99d1d4b0e9cd1d10a61734a3d148db)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` | load from serializable file 
`public inline virtual int32_t `[`get_num_parameters`](#classshogun_1_1Parameter_1a281773525d07066cd375200e4e9b0343)`()` | getter for number of parameters 
`public void `[`set_from_parameters`](#classshogun_1_1Parameter_1a319607870236422bfa3f20492d3792fb)`(`[`Parameter`](#classshogun_1_1Parameter)` * params)` | Takes another [Parameter](#classshogun_1_1Parameter) instance and sets all parameters of this instance (with equal name) to the values of the provided one. (Note that if CSGObjects are replaced, the old ones are SG_UNREFed and the new ones are SG_REFed) Currently only works for any float64_t and [CSGObject](#classshogun_1_1CSGObject) type.
`public void `[`add_parameters`](#classshogun_1_1Parameter_1accfb3267cfc3be7e522222834c7bf97a)`(`[`Parameter`](#classshogun_1_1Parameter)` * params)` | Adds all parameters from another instance to this one
`public bool `[`contains_parameter`](#classshogun_1_1Parameter_1ada86508a07c3b1f9925d76ba2859e6e4)`(const char * name)` | Checks if a parameter with the spcified name is included
`public inline `[`TParameter`](#structshogun_1_1TParameter)` * `[`get_parameter`](#classshogun_1_1Parameter_1ae799d9b45c025d413ae7eaa64f3fa60f)`(int32_t idx)` | Getter for [TParameter](#structshogun_1_1TParameter) elements (Does not to bound checking)
`public inline `[`TParameter`](#structshogun_1_1TParameter)` * `[`get_parameter`](#classshogun_1_1Parameter_1a1e1f74e1a371fe81238b156d7a4e8f88)`(const char * name)` | Getter for Tparameter elements by name
`public void `[`add`](#classshogun_1_1Parameter_1aed985c0dd1c9371011fe55a886f6509e)`(bool * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a0d96606c59aa511676ad45cc77ef034e)`(char * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a1e7256db3dfb707a45104ca3b3b759b5)`(int8_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a8c8f87241053622951dd39d8e8a6fe55)`(uint8_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ad72ab58d211a1bbdcc81126e169e128b)`(int16_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a1b1dab3539a3616147d9b8e318668bf6)`(uint16_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a61fb381d826ba60093d3059924391146)`(int32_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a4f20e152743422b62e4563fc7dc4fe62)`(uint32_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a985fed39723a94bbfc4a8ca216baed5b)`(int64_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ab47f26a6b94d420aaa8ed8c914052229)`(uint64_t * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a3d507f6688e145b1857f78f9836fd3e9)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1aaede968e962eeb31a76ca7d66878b6c6)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a16abfd639bd4d7e860522ea85d4d39f1)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a7537cc6313f7719967d5ba5c2f0790ca)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1aa5142718df7be9ee8002ad10d71ed8f4)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** param,const char * name,const char * description)` | add param 
`public template<>`  <br/>`inline void `[`add`](#classshogun_1_1Parameter_1a53d794bfcf703304a9ed20faf246f6ca)`(T ** param,const char * name,const char * description)` | 
`public void `[`add`](#classshogun_1_1Parameter_1a551db7b5cc77f36fe8987accc5c20d7c)`(`[`SGString`](#classshogun_1_1SGString)`< bool > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ab18095a28aa93dce34896525dedc4b70)`(`[`SGString`](#classshogun_1_1SGString)`< char > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a69ffbd43ac4afd5fd1054cd4a07cefb7)`(`[`SGString`](#classshogun_1_1SGString)`< int8_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a7ca8f580196531846d2f9071a7aebe28)`(`[`SGString`](#classshogun_1_1SGString)`< uint8_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a5104386a1b061b369a5062e311f384e2)`(`[`SGString`](#classshogun_1_1SGString)`< int16_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a44c70ff203e11f09d7f40a7638157469)`(`[`SGString`](#classshogun_1_1SGString)`< uint16_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a5bf0e39a91f72c9792bb092a07c6750d)`(`[`SGString`](#classshogun_1_1SGString)`< int32_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a6aaa57d33a9f993380e5631586fc350b)`(`[`SGString`](#classshogun_1_1SGString)`< uint32_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ae22a9bea9d852ea6290a74866d5df27f)`(`[`SGString`](#classshogun_1_1SGString)`< int64_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ad83560361d462e53040888fd4271a5ff)`(`[`SGString`](#classshogun_1_1SGString)`< uint64_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a202c04796f25d249a7b0e06a845d3969)`(`[`SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a065181fbab3e720b86492742e8b4ef26)`(`[`SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a04a8d73fa6afd46bde3483d0287fec21)`(`[`SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a094f8dbc5a8f4bef5397a571c46c5b3e)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a8c63b0c6673021c315cf7605e0d66671)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a225425f2ae014e6ef6829b1483ad32e4)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ae63c1e10be670b780e90aab18e39b604)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a55e6aeede77cd3a9d2250d7b2ec76369)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1afbf1f6b711e529ab68b04e4e0e723c26)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a96533ce108774d154043a37635d871af)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a90648b4e3a6afebe0476b00117c995ff)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1abb34f4aa8e405a8346f7a18f3f5c651a)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a3423c0791966ed61d6c5eab94d711f8c)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1ab188260f2bf5224a04d3724133e7442c)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a25663e9896d018e6bb36e2990ea33358)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1aa5e0b17845e0e75d6da50c8ab3b3bee2)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` | add param 
`public void `[`add`](#classshogun_1_1Parameter_1a545763e4c87bff998e3d3e9e11904c75)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` | add param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a6511853487ee5bba1bbe5847e7cff88b)`(bool ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a967264e32c011c1e50df851b9f11d85c)`(char ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1ab92c1ac5ff8e86fab100e0f079e49e54)`(int8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1ac6d88f65dc48b9a10591676109e88541)`(uint8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a32255f2fc8644a35aeebefd2f29b12ef)`(int16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a8fc88390ce4a4afa344a2a4416b0d1d7)`(uint16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a0f6a1e097c35074ea74373b716c07e9c)`(int32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1ae1f70f88bcd23505874473bdbde38fe5)`(uint32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a9b942b6cabddc8a3a57d1d1ac772bbe6)`(int64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a705d903dd1486f5c697d7b758b3b1c20)`(uint64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1af077bd514812ef09e12ab9e939d76155)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1af5401104d6d2508f0958bd0041bcf2fa)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a6512f6bc352e0a54d7db27ee3ba9c4fd)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a9040dd0b23a724feb9e8a45954cebfc6)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1add1b82097b7e3fb6c85d5f37087d18a5)`(`[`CSGObject`](#classshogun_1_1CSGObject)` *** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a23de4894a32a6df9c8c45d7eb16b4836)`(`[`SGString`](#classshogun_1_1SGString)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1aa56e1ce658944d927d8257bd29b3148d)`(`[`SGString`](#classshogun_1_1SGString)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a12a9643c74a8a59bc6c98e433dc8b7bd)`(`[`SGString`](#classshogun_1_1SGString)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a58ad5b5f5e9348c129afc8fc5bd84751)`(`[`SGString`](#classshogun_1_1SGString)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a582120aaf99a547c7114ba0d6680df83)`(`[`SGString`](#classshogun_1_1SGString)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a027a94f702fc34923a4a1f5959e485a0)`(`[`SGString`](#classshogun_1_1SGString)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a848131a04e546cd9155c3a7ceb41eaca)`(`[`SGString`](#classshogun_1_1SGString)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a0c6e11b6b12f3536fce390a30ecbf43f)`(`[`SGString`](#classshogun_1_1SGString)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1aad2b58dced7f28f67b201812b0b31ab2)`(`[`SGString`](#classshogun_1_1SGString)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a7a94be9baa229ff3e9a710cbdb105954)`(`[`SGString`](#classshogun_1_1SGString)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a0300bc9c3512b29193462121944b2df5)`(`[`SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a7e1eef6d71302ae984685fb7cf0b0363)`(`[`SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a3053a377ed4515213b9e65b155de54d8)`(`[`SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1aad47a1c6d6bfefbb7158e6029924ab3a)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1ad17a06e9b4571f50953b431a15b333ee)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1ab691e27b602e8a9cf35830687e6d4b00)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a85cd7faa6c1da29b41247cd623bdba4e)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1aedfb900ed7b9fb279f233209874f6884)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a24e2772b9e2a849daafa0ff20913adfd)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1abdf8a53728828fde58b3e95770942626)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a3a8b8ecff99898b989cc2328a59b4138)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1aec281c039af44d42b3b66e41d674b4a5)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a205b313a75f1e342559865c498cee9b6)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1abc856ee435e4d976149b3ec14c9886c2)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a8ce6573d3474907e98494be7211f66e0)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a394ee07ea748efbb610b01e038c6ba5c)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add_vector`](#classshogun_1_1Parameter_1a41b524b8bab53505f1987d2b95280385)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1af20520106322d07fa83127547cdfed6e)`(`[`SGVector`](#classshogun_1_1SGVector)`< bool > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ab845e42b815f3b59ca308916b3a07248)`(`[`SGVector`](#classshogun_1_1SGVector)`< char > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a2629fcc4b0535dff252ec8d6b4a4f155)`(`[`SGVector`](#classshogun_1_1SGVector)`< int8_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a3a2f10cdc6d1598bd4a171eb92a7865c)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint8_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a0443dcdfcecef289891748834f22511a)`(`[`SGVector`](#classshogun_1_1SGVector)`< int16_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a463d2b97bb2893d89a71ed9f5242ede3)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint16_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1af0947d9a2b0e6bdc27e006d6a6d9a6e7)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ae5df84abcd2784841469f417e74a778d)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint32_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ace7515285a14ab766e107e71a79d3b73)`(`[`SGVector`](#classshogun_1_1SGVector)`< int64_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a07ab81e0770bf1f7c26742dab652558a)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint64_t > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a5abd8a21320384505712beab12346242)`(`[`SGVector](#classshogun_1_1SGVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a16bf903fbdb4baeaf543a4e96be78348)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ab547372bfbc64990e3319631c942b8f8)`(`[`SGVector](#classshogun_1_1SGVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a11e09e4005563a89d0335fed4b186ea1)`(`[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a21587f844e350cb3bae1f946e2672a20)`(`[`SGVector](#classshogun_1_1SGVector)< [CSGObject`](#classshogun_1_1CSGObject)` *> * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a1f216e87be28d7458b2b32576e56a37e)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< bool > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a6201a57a1880c85905cc4379a98d0a4f)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< char > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a0abf62a4a7253a6d8d62cf2724db4780)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int8_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a8eeada1a844635ca1e359ff1300f749c)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint8_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ae833db60d9470be8e8b85bfc525e8feb)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int16_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a469996a531daee2620e4911fcc280236)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint16_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ab068efaaee397fffa73af2543175cec1)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int32_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a98ba03ab2ff582cafad5c22e994df46c)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint32_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1af34584bc9472542bcd2489f17f496261)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int64_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a75c427e7c3429416e8dce408d3d33724)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint64_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a55b5d61c4a95f823950761fa2b830668)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ad5e299d05855104f50d915b5047188ca)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a184c1c32cfbdec5954d9eca82a638dcc)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a25e8904c32345a244d4720008c79f3af)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ae1da4f2ea4c34c925af5f4b5226c56f0)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ae119da3c96988c4e185475d15dc98ac1)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ae846f437abfbfaffffd820d162f22b0f)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a55395d120b7012277340b9e9a95e9387)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ae9dd2baf91a721116a597bddbdfc7ad2)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1ad56ac6e16278b6baa01d4c44d70b477c)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a7145bba337451de491ea248096411e5d)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1afd02c33d0a243fe5dd400fc71296cfa1)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a0716dbb992bcd3c4d2a6c4d954159346)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a1659cd370a5b28ff093268db31822f34)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a27d7dea9c36dacdda0778d2d25bac2cb)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a420b576a99229b23ae82f3107a6dfe6e)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add`](#classshogun_1_1Parameter_1a9180255c87d43c7208b9787f8e39fb0b)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > > * param,const char * name,const char * description)` | add vector param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a99c6cb84d23a8b9798871944bc3e598c)`(bool ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a759e9acafa0e20f39370eb6372bbab11)`(char ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a5e01b7d96ed92b7bee2bb71c55be581e)`(int8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1aa5c11fd4a516e2a752a6e223c908cfc9)`(uint8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a9980bc979427240ae8e85efc22a8b213)`(int16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1ad8aa15bfad196f4fd3867e9098a6cd1f)`(uint16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a5eaf2639b87a94a81144f367e85984d4)`(int32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1ad11781307f38c35eeaf3fb7f28a78a5a)`(uint32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1acdbfb22a12a284802353f3776a4f2185)`(int64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a56bff8627127d0929c26b9b8b8a58d63)`(uint64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a6f6e97cbb3c106b470d982e0e5fba159)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1afeca39211a0c8f4902583b087cd270b4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1abd68485eaf8985213c134a2af39cf97c)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1aa9bed8e484f4c17042d644b8f6b76f21)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a4c4b4f1f6f5e9e9bf4e0a6fdb159da78)`(`[`CSGObject`](#classshogun_1_1CSGObject)` *** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a89dd70971ff27136ec5782f7db6a2a89)`(`[`SGString`](#classshogun_1_1SGString)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1adc0edb79768c0aad766d20d08653bea5)`(`[`SGString`](#classshogun_1_1SGString)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a783d466af4736e127aa69b020bcb11b3)`(`[`SGString`](#classshogun_1_1SGString)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a1c83cb831303e5a6175356540dfb02dd)`(`[`SGString`](#classshogun_1_1SGString)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1acfa9178ebc95f1f3ade075e6d00cb3df)`(`[`SGString`](#classshogun_1_1SGString)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a0f677258ae02443888cc814ed14715bb)`(`[`SGString`](#classshogun_1_1SGString)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a928f95a69bd9a0815b7c58eadb0776fd)`(`[`SGString`](#classshogun_1_1SGString)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a5bb886825c3c266697721222a4fde44a)`(`[`SGString`](#classshogun_1_1SGString)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1aa43b62c33386e166d91534dc03833706)`(`[`SGString`](#classshogun_1_1SGString)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a4fd89ea079feea6fd9093b492cfebf18)`(`[`SGString`](#classshogun_1_1SGString)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a74c1fef94729d4352ac26123a89ce846)`(`[`SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a7cf82b927fb631fcb857a5020bd93802)`(`[`SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a1a6e323eb0786ebc4be5e519b8f5669d)`(`[`SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a2f353ea085fd5b78e1f0e0d444b76c72)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a247692a3f9b35e35ff3ff6cdfc7fce8a)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a0609ffd5a3a29db161270797416c96a0)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1ae0b22f14b3e0d07bcb5c4292744892ad)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a51455117274de3a5d81cbd8fb9b93370)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1ae97e214e9f55dfaa50d1fed49b544042)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a2c55bc4cbb476a1e50213d63401c9bed)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a92f4e79eb50adff9800e2d8460c764b3)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1a2389775100e24de128d81c6a37f16886)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1af1aedbd047eadf956e04ee24fa81d32d)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1ada59ae2a130415961c78dbc8b6860777)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1aee33b3b57cd4a5afa17e359f145ffd3e)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1aead47c41bbe49b6b72930bf80d44d526)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add_matrix`](#classshogun_1_1Parameter_1ad2c42d9240e9b052f9a4521b5df803e7)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a46f0301db2db9fd7e22e007ed9ec570f)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a7376f3432122f21b31597b7ca2ec40df)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< char > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ab0826f32098647d7cf4b6b32fd1a1844)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int8_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a4b156572e6f38de23b85cebc6e3e846d)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint8_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a69ab639b8df650c891fac73352d1b0cd)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int16_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a207c0959917ea56052aa7d7bb8a9417a)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint16_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a0524d1dfc18cd93d5b9cca960124a8d6)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a4e781f01c6fa69c73462b80da15969b0)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint32_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a5c611cb2a9502f7d3bb48b36d59fc7e8)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int64_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a95643ad859905498adc65f3f34c6dec8)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint64_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aced2db64755e06410daa2948a7a7ba13)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a4646a8edaa6780e68df47c11cc10efeb)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aefdb466d3ed95f8b9a1e6232aa83acc2)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aa9692e73974f02c1ed776943f348b63c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a59dd091d6448fb46f96c359af880a5cf)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [CSGObject`](#classshogun_1_1CSGObject)` *> * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ae04ad7e38ec464214105c638827c990c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< bool > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aa6785872fdbda058e0a3779114128e6c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< char > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1abfcff6ba7dca8e9810bc5e02ed373f7b)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int8_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ab5d7835ccb51c06c19963e02c7b0b1d8)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint8_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a4ae011cb1c7c7641529b15e5c3a86f15)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int16_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1abd0e2dbd734d8a9856b3f47987a89265)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint16_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a3e6bdd05e6bda51eb95c7a7bb2eb9a79)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int32_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a3be1a15b6e5f5baa11d2ad35a41cbe2e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint32_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a30882bc5ea58101361a12ab7ed67f225)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int64_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ad8b55580bbdaa3f3b154acd83a9aabf4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint64_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a1ee27de715b7a796747e9f129343fa85)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aacd132e07ff29667400098c310991821)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ad01dc6aab08a90865cd0ac3eb7444a5e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a638fb356f638a0a62c5f2831aafc5a18)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a2e4f13bf29962fcec9fde2abf9e6c8b4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a8ccbcd20869f91db5d380f7d470a2ed4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1acc2e9801c6421c3053696a40ff18f452)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a90ca1bef6cc5807e20d94cb409ac6e3c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a6c950defbdd55fcfd66a71d7e492dc06)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1afd5e308492c45cbfe61ab0c3a2fad7ac)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a313a6957ceb3706fca6ccda132f7552a)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a6402d74ca0ff2f844f84423325ab359f)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a22b4938f128f6413985e45ee2f26de85)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ac2374ffc0ebd281ab21852fedae3bc17)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ab614f8ad64f2fbc9199e61d422e55f86)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a4aa02fe85325ae7d50efc47daedcbf31)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a847a3a386ccc5b390c7d181bff51e62c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a975b17e482a9588de972ddd34e871d12)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< bool > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aea9206df60fa836d1b8ce7bf0d8229aa)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< char > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a5852b1a3c79a9757bdfe77726995e62a)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int8_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aea28efc49f8847d9c7599f479b8e86ae)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint8_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1aecc935095b109cfe015388a03c75d938)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int16_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1affc3bd50a7efa85bf6bbf4d0d860c859)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint16_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a4fcf0077e96eb22e4dcfb0e9de207046)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int32_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a2276e9afced4dbcf893bbcf78182c622)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint32_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a1669daabdd5401580a9d8b878a2e50c0)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int64_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ab0b9f37601cd6f8b8f60ee2f3bba1fe0)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint64_t > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a129d07acca46eac10eb0bb1bd10baf97)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ad8ed504425869cf9822b0e98b2686abe)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1ad5f5fb54beb459ac060f2ad749562462)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a9d412290659a94be75db2a4e773538e0)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` | add matrix param 
`public void `[`add`](#classshogun_1_1Parameter_1a2e76a8889309e20d48f3dee8f625eb7c)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [CSGObject`](#classshogun_1_1CSGObject)` *> * param,const char * name,const char * description)` | add matrix param 
`protected `[`DynArray](#classshogun_1_1DynArray)< [TParameter`](#structshogun_1_1TParameter)` * > `[`m_params`](#classshogun_1_1Parameter_1a74840f2c3a094c65840041da2fcad2d8) | array of parameters
`protected virtual void `[`add_type`](#classshogun_1_1Parameter_1ad9b0009eed07489043dc344ceb5b3055)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` * type,void * param,const char * name,const char * description)` | add new type 

## Members

#### `public  explicit `[`Parameter`](#classshogun_1_1Parameter_1a722d0b273a6e3633c189fb21eaaa483c)`()` {#classshogun_1_1Parameter_1a722d0b273a6e3633c189fb21eaaa483c}

explicit constructor

#### `public virtual  `[`~Parameter`](#classshogun_1_1Parameter_1a615c436bf6b0250e3518ba91a5d88f66)`()` {#classshogun_1_1Parameter_1a615c436bf6b0250e3518ba91a5d88f66}

destructor

#### `public virtual void `[`print`](#classshogun_1_1Parameter_1acfb5f363d75656e9b4686794fa9a18f9)`(const char * prefix)` {#classshogun_1_1Parameter_1acfb5f363d75656e9b4686794fa9a18f9}

print 
#### Parameters
* `prefix` prefix

#### `public virtual bool `[`save`](#classshogun_1_1Parameter_1af5f394df0bf09bc2409808804f7e8c8b)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#classshogun_1_1Parameter_1af5f394df0bf09bc2409808804f7e8c8b}

save to serializable file 
#### Parameters
* `file` destination file 

* `prefix` prefix

#### `public virtual bool `[`load`](#classshogun_1_1Parameter_1aec99d1d4b0e9cd1d10a61734a3d148db)`(`[`CSerializableFile`](#classshogun_1_1CSerializableFile)` * file,const char * prefix)` {#classshogun_1_1Parameter_1aec99d1d4b0e9cd1d10a61734a3d148db}

load from serializable file 
#### Parameters
* `file` source file 

* `prefix` prefix

#### `public inline virtual int32_t `[`get_num_parameters`](#classshogun_1_1Parameter_1a281773525d07066cd375200e4e9b0343)`()` {#classshogun_1_1Parameter_1a281773525d07066cd375200e4e9b0343}

getter for number of parameters 
#### Returns
number of parameters

#### `public void `[`set_from_parameters`](#classshogun_1_1Parameter_1a319607870236422bfa3f20492d3792fb)`(`[`Parameter`](#classshogun_1_1Parameter)` * params)` {#classshogun_1_1Parameter_1a319607870236422bfa3f20492d3792fb}

Takes another [Parameter](#classshogun_1_1Parameter) instance and sets all parameters of this instance (with equal name) to the values of the provided one. (Note that if CSGObjects are replaced, the old ones are SG_UNREFed and the new ones are SG_REFed) Currently only works for any float64_t and [CSGObject](#classshogun_1_1CSGObject) type.

#### Parameters
* `params` another [Parameter](#classshogun_1_1Parameter) instance

#### `public void `[`add_parameters`](#classshogun_1_1Parameter_1accfb3267cfc3be7e522222834c7bf97a)`(`[`Parameter`](#classshogun_1_1Parameter)` * params)` {#classshogun_1_1Parameter_1accfb3267cfc3be7e522222834c7bf97a}

Adds all parameters from another instance to this one

#### Parameters
* `params` another [Parameter](#classshogun_1_1Parameter) instance

#### `public bool `[`contains_parameter`](#classshogun_1_1Parameter_1ada86508a07c3b1f9925d76ba2859e6e4)`(const char * name)` {#classshogun_1_1Parameter_1ada86508a07c3b1f9925d76ba2859e6e4}

Checks if a parameter with the spcified name is included

#### Returns
true if parameter with name is included

#### `public inline `[`TParameter`](#structshogun_1_1TParameter)` * `[`get_parameter`](#classshogun_1_1Parameter_1ae799d9b45c025d413ae7eaa64f3fa60f)`(int32_t idx)` {#classshogun_1_1Parameter_1ae799d9b45c025d413ae7eaa64f3fa60f}

Getter for [TParameter](#structshogun_1_1TParameter) elements (Does not to bound checking)

#### Parameters
* `idx` desired index 

#### Returns
pointer to the [TParameter](#structshogun_1_1TParameter) with the specified index

#### `public inline `[`TParameter`](#structshogun_1_1TParameter)` * `[`get_parameter`](#classshogun_1_1Parameter_1a1e1f74e1a371fe81238b156d7a4e8f88)`(const char * name)` {#classshogun_1_1Parameter_1a1e1f74e1a371fe81238b156d7a4e8f88}

Getter for Tparameter elements by name

#### Parameters
* `name` name of desired parameter 

#### Returns
parameter with desired name, NULL if non such found

#### `public void `[`add`](#classshogun_1_1Parameter_1aed985c0dd1c9371011fe55a886f6509e)`(bool * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aed985c0dd1c9371011fe55a886f6509e}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a0d96606c59aa511676ad45cc77ef034e)`(char * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0d96606c59aa511676ad45cc77ef034e}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a1e7256db3dfb707a45104ca3b3b759b5)`(int8_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1e7256db3dfb707a45104ca3b3b759b5}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a8c8f87241053622951dd39d8e8a6fe55)`(uint8_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a8c8f87241053622951dd39d8e8a6fe55}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad72ab58d211a1bbdcc81126e169e128b)`(int16_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad72ab58d211a1bbdcc81126e169e128b}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a1b1dab3539a3616147d9b8e318668bf6)`(uint16_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1b1dab3539a3616147d9b8e318668bf6}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a61fb381d826ba60093d3059924391146)`(int32_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a61fb381d826ba60093d3059924391146}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4f20e152743422b62e4563fc7dc4fe62)`(uint32_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4f20e152743422b62e4563fc7dc4fe62}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a985fed39723a94bbfc4a8ca216baed5b)`(int64_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a985fed39723a94bbfc4a8ca216baed5b}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab47f26a6b94d420aaa8ed8c914052229)`(uint64_t * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab47f26a6b94d420aaa8ed8c914052229}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a3d507f6688e145b1857f78f9836fd3e9)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3d507f6688e145b1857f78f9836fd3e9}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aaede968e962eeb31a76ca7d66878b6c6)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aaede968e962eeb31a76ca7d66878b6c6}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a16abfd639bd4d7e860522ea85d4d39f1)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a16abfd639bd4d7e860522ea85d4d39f1}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a7537cc6313f7719967d5ba5c2f0790ca)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7537cc6313f7719967d5ba5c2f0790ca}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aa5142718df7be9ee8002ad10d71ed8f4)`(`[`CSGObject`](#classshogun_1_1CSGObject)` ** param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa5142718df7be9ee8002ad10d71ed8f4}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public template<>`  <br/>`inline void `[`add`](#classshogun_1_1Parameter_1a53d794bfcf703304a9ed20faf246f6ca)`(T ** param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a53d794bfcf703304a9ed20faf246f6ca}

#### `public void `[`add`](#classshogun_1_1Parameter_1a551db7b5cc77f36fe8987accc5c20d7c)`(`[`SGString`](#classshogun_1_1SGString)`< bool > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a551db7b5cc77f36fe8987accc5c20d7c}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab18095a28aa93dce34896525dedc4b70)`(`[`SGString`](#classshogun_1_1SGString)`< char > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab18095a28aa93dce34896525dedc4b70}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a69ffbd43ac4afd5fd1054cd4a07cefb7)`(`[`SGString`](#classshogun_1_1SGString)`< int8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a69ffbd43ac4afd5fd1054cd4a07cefb7}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a7ca8f580196531846d2f9071a7aebe28)`(`[`SGString`](#classshogun_1_1SGString)`< uint8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7ca8f580196531846d2f9071a7aebe28}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a5104386a1b061b369a5062e311f384e2)`(`[`SGString`](#classshogun_1_1SGString)`< int16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5104386a1b061b369a5062e311f384e2}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a44c70ff203e11f09d7f40a7638157469)`(`[`SGString`](#classshogun_1_1SGString)`< uint16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a44c70ff203e11f09d7f40a7638157469}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a5bf0e39a91f72c9792bb092a07c6750d)`(`[`SGString`](#classshogun_1_1SGString)`< int32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5bf0e39a91f72c9792bb092a07c6750d}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a6aaa57d33a9f993380e5631586fc350b)`(`[`SGString`](#classshogun_1_1SGString)`< uint32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6aaa57d33a9f993380e5631586fc350b}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae22a9bea9d852ea6290a74866d5df27f)`(`[`SGString`](#classshogun_1_1SGString)`< int64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae22a9bea9d852ea6290a74866d5df27f}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad83560361d462e53040888fd4271a5ff)`(`[`SGString`](#classshogun_1_1SGString)`< uint64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad83560361d462e53040888fd4271a5ff}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a202c04796f25d249a7b0e06a845d3969)`(`[`SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a202c04796f25d249a7b0e06a845d3969}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a065181fbab3e720b86492742e8b4ef26)`(`[`SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a065181fbab3e720b86492742e8b4ef26}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a04a8d73fa6afd46bde3483d0287fec21)`(`[`SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a04a8d73fa6afd46bde3483d0287fec21}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a094f8dbc5a8f4bef5397a571c46c5b3e)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a094f8dbc5a8f4bef5397a571c46c5b3e}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a8c63b0c6673021c315cf7605e0d66671)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a8c63b0c6673021c315cf7605e0d66671}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a225425f2ae014e6ef6829b1483ad32e4)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a225425f2ae014e6ef6829b1483ad32e4}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae63c1e10be670b780e90aab18e39b604)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae63c1e10be670b780e90aab18e39b604}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a55e6aeede77cd3a9d2250d7b2ec76369)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a55e6aeede77cd3a9d2250d7b2ec76369}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1afbf1f6b711e529ab68b04e4e0e723c26)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1afbf1f6b711e529ab68b04e4e0e723c26}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a96533ce108774d154043a37635d871af)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a96533ce108774d154043a37635d871af}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a90648b4e3a6afebe0476b00117c995ff)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a90648b4e3a6afebe0476b00117c995ff}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1abb34f4aa8e405a8346f7a18f3f5c651a)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1abb34f4aa8e405a8346f7a18f3f5c651a}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a3423c0791966ed61d6c5eab94d711f8c)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3423c0791966ed61d6c5eab94d711f8c}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab188260f2bf5224a04d3724133e7442c)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab188260f2bf5224a04d3724133e7442c}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a25663e9896d018e6bb36e2990ea33358)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a25663e9896d018e6bb36e2990ea33358}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aa5e0b17845e0e75d6da50c8ab3b3bee2)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa5e0b17845e0e75d6da50c8ab3b3bee2}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a545763e4c87bff998e3d3e9e11904c75)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a545763e4c87bff998e3d3e9e11904c75}

add param 
#### Parameters
* `param` parameter itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a6511853487ee5bba1bbe5847e7cff88b)`(bool ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6511853487ee5bba1bbe5847e7cff88b}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a967264e32c011c1e50df851b9f11d85c)`(char ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a967264e32c011c1e50df851b9f11d85c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1ab92c1ac5ff8e86fab100e0f079e49e54)`(int8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab92c1ac5ff8e86fab100e0f079e49e54}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1ac6d88f65dc48b9a10591676109e88541)`(uint8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1ac6d88f65dc48b9a10591676109e88541}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a32255f2fc8644a35aeebefd2f29b12ef)`(int16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a32255f2fc8644a35aeebefd2f29b12ef}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a8fc88390ce4a4afa344a2a4416b0d1d7)`(uint16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a8fc88390ce4a4afa344a2a4416b0d1d7}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a0f6a1e097c35074ea74373b716c07e9c)`(int32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0f6a1e097c35074ea74373b716c07e9c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1ae1f70f88bcd23505874473bdbde38fe5)`(uint32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae1f70f88bcd23505874473bdbde38fe5}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a9b942b6cabddc8a3a57d1d1ac772bbe6)`(int64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a9b942b6cabddc8a3a57d1d1ac772bbe6}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a705d903dd1486f5c697d7b758b3b1c20)`(uint64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a705d903dd1486f5c697d7b758b3b1c20}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1af077bd514812ef09e12ab9e939d76155)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1af077bd514812ef09e12ab9e939d76155}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1af5401104d6d2508f0958bd0041bcf2fa)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1af5401104d6d2508f0958bd0041bcf2fa}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a6512f6bc352e0a54d7db27ee3ba9c4fd)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6512f6bc352e0a54d7db27ee3ba9c4fd}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a9040dd0b23a724feb9e8a45954cebfc6)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a9040dd0b23a724feb9e8a45954cebfc6}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1add1b82097b7e3fb6c85d5f37087d18a5)`(`[`CSGObject`](#classshogun_1_1CSGObject)` *** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1add1b82097b7e3fb6c85d5f37087d18a5}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a23de4894a32a6df9c8c45d7eb16b4836)`(`[`SGString`](#classshogun_1_1SGString)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a23de4894a32a6df9c8c45d7eb16b4836}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1aa56e1ce658944d927d8257bd29b3148d)`(`[`SGString`](#classshogun_1_1SGString)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa56e1ce658944d927d8257bd29b3148d}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a12a9643c74a8a59bc6c98e433dc8b7bd)`(`[`SGString`](#classshogun_1_1SGString)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a12a9643c74a8a59bc6c98e433dc8b7bd}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a58ad5b5f5e9348c129afc8fc5bd84751)`(`[`SGString`](#classshogun_1_1SGString)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a58ad5b5f5e9348c129afc8fc5bd84751}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a582120aaf99a547c7114ba0d6680df83)`(`[`SGString`](#classshogun_1_1SGString)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a582120aaf99a547c7114ba0d6680df83}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a027a94f702fc34923a4a1f5959e485a0)`(`[`SGString`](#classshogun_1_1SGString)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a027a94f702fc34923a4a1f5959e485a0}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a848131a04e546cd9155c3a7ceb41eaca)`(`[`SGString`](#classshogun_1_1SGString)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a848131a04e546cd9155c3a7ceb41eaca}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a0c6e11b6b12f3536fce390a30ecbf43f)`(`[`SGString`](#classshogun_1_1SGString)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0c6e11b6b12f3536fce390a30ecbf43f}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1aad2b58dced7f28f67b201812b0b31ab2)`(`[`SGString`](#classshogun_1_1SGString)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1aad2b58dced7f28f67b201812b0b31ab2}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a7a94be9baa229ff3e9a710cbdb105954)`(`[`SGString`](#classshogun_1_1SGString)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7a94be9baa229ff3e9a710cbdb105954}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a0300bc9c3512b29193462121944b2df5)`(`[`SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0300bc9c3512b29193462121944b2df5}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a7e1eef6d71302ae984685fb7cf0b0363)`(`[`SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7e1eef6d71302ae984685fb7cf0b0363}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a3053a377ed4515213b9e65b155de54d8)`(`[`SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3053a377ed4515213b9e65b155de54d8}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1aad47a1c6d6bfefbb7158e6029924ab3a)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1aad47a1c6d6bfefbb7158e6029924ab3a}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1ad17a06e9b4571f50953b431a15b333ee)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad17a06e9b4571f50953b431a15b333ee}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1ab691e27b602e8a9cf35830687e6d4b00)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab691e27b602e8a9cf35830687e6d4b00}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a85cd7faa6c1da29b41247cd623bdba4e)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a85cd7faa6c1da29b41247cd623bdba4e}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1aedfb900ed7b9fb279f233209874f6884)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1aedfb900ed7b9fb279f233209874f6884}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a24e2772b9e2a849daafa0ff20913adfd)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a24e2772b9e2a849daafa0ff20913adfd}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1abdf8a53728828fde58b3e95770942626)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1abdf8a53728828fde58b3e95770942626}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a3a8b8ecff99898b989cc2328a59b4138)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3a8b8ecff99898b989cc2328a59b4138}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1aec281c039af44d42b3b66e41d674b4a5)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1aec281c039af44d42b3b66e41d674b4a5}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a205b313a75f1e342559865c498cee9b6)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a205b313a75f1e342559865c498cee9b6}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1abc856ee435e4d976149b3ec14c9886c2)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1abc856ee435e4d976149b3ec14c9886c2}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a8ce6573d3474907e98494be7211f66e0)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a8ce6573d3474907e98494be7211f66e0}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a394ee07ea748efbb610b01e038c6ba5c)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a394ee07ea748efbb610b01e038c6ba5c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_vector`](#classshogun_1_1Parameter_1a41b524b8bab53505f1987d2b95280385)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length,const char * name,const char * description)` {#classshogun_1_1Parameter_1a41b524b8bab53505f1987d2b95280385}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `length` length of vector 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1af20520106322d07fa83127547cdfed6e)`(`[`SGVector`](#classshogun_1_1SGVector)`< bool > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1af20520106322d07fa83127547cdfed6e}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab845e42b815f3b59ca308916b3a07248)`(`[`SGVector`](#classshogun_1_1SGVector)`< char > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab845e42b815f3b59ca308916b3a07248}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a2629fcc4b0535dff252ec8d6b4a4f155)`(`[`SGVector`](#classshogun_1_1SGVector)`< int8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2629fcc4b0535dff252ec8d6b4a4f155}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a3a2f10cdc6d1598bd4a171eb92a7865c)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3a2f10cdc6d1598bd4a171eb92a7865c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a0443dcdfcecef289891748834f22511a)`(`[`SGVector`](#classshogun_1_1SGVector)`< int16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0443dcdfcecef289891748834f22511a}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a463d2b97bb2893d89a71ed9f5242ede3)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a463d2b97bb2893d89a71ed9f5242ede3}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1af0947d9a2b0e6bdc27e006d6a6d9a6e7)`(`[`SGVector`](#classshogun_1_1SGVector)`< int32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1af0947d9a2b0e6bdc27e006d6a6d9a6e7}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae5df84abcd2784841469f417e74a778d)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae5df84abcd2784841469f417e74a778d}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ace7515285a14ab766e107e71a79d3b73)`(`[`SGVector`](#classshogun_1_1SGVector)`< int64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ace7515285a14ab766e107e71a79d3b73}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a07ab81e0770bf1f7c26742dab652558a)`(`[`SGVector`](#classshogun_1_1SGVector)`< uint64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a07ab81e0770bf1f7c26742dab652558a}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a5abd8a21320384505712beab12346242)`(`[`SGVector](#classshogun_1_1SGVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5abd8a21320384505712beab12346242}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a16bf903fbdb4baeaf543a4e96be78348)`(`[`SGVector](#classshogun_1_1SGVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a16bf903fbdb4baeaf543a4e96be78348}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab547372bfbc64990e3319631c942b8f8)`(`[`SGVector](#classshogun_1_1SGVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab547372bfbc64990e3319631c942b8f8}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a11e09e4005563a89d0335fed4b186ea1)`(`[`SGVector](#classshogun_1_1SGVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a11e09e4005563a89d0335fed4b186ea1}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a21587f844e350cb3bae1f946e2672a20)`(`[`SGVector](#classshogun_1_1SGVector)< [CSGObject`](#classshogun_1_1CSGObject)` *> * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a21587f844e350cb3bae1f946e2672a20}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a1f216e87be28d7458b2b32576e56a37e)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< bool > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1f216e87be28d7458b2b32576e56a37e}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a6201a57a1880c85905cc4379a98d0a4f)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< char > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6201a57a1880c85905cc4379a98d0a4f}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a0abf62a4a7253a6d8d62cf2724db4780)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0abf62a4a7253a6d8d62cf2724db4780}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a8eeada1a844635ca1e359ff1300f749c)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a8eeada1a844635ca1e359ff1300f749c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae833db60d9470be8e8b85bfc525e8feb)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae833db60d9470be8e8b85bfc525e8feb}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a469996a531daee2620e4911fcc280236)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a469996a531daee2620e4911fcc280236}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab068efaaee397fffa73af2543175cec1)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab068efaaee397fffa73af2543175cec1}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a98ba03ab2ff582cafad5c22e994df46c)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a98ba03ab2ff582cafad5c22e994df46c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1af34584bc9472542bcd2489f17f496261)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< int64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1af34584bc9472542bcd2489f17f496261}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a75c427e7c3429416e8dce408d3d33724)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString`](#classshogun_1_1SGString)`< uint64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a75c427e7c3429416e8dce408d3d33724}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a55b5d61c4a95f823950761fa2b830668)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a55b5d61c4a95f823950761fa2b830668}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad5e299d05855104f50d915b5047188ca)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad5e299d05855104f50d915b5047188ca}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a184c1c32cfbdec5954d9eca82a638dcc)`(`[`SGVector](#classshogun_1_1SGVector)< [SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a184c1c32cfbdec5954d9eca82a638dcc}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a25e8904c32345a244d4720008c79f3af)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a25e8904c32345a244d4720008c79f3af}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae1da4f2ea4c34c925af5f4b5226c56f0)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae1da4f2ea4c34c925af5f4b5226c56f0}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae119da3c96988c4e185475d15dc98ac1)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae119da3c96988c4e185475d15dc98ac1}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae846f437abfbfaffffd820d162f22b0f)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae846f437abfbfaffffd820d162f22b0f}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a55395d120b7012277340b9e9a95e9387)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a55395d120b7012277340b9e9a95e9387}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae9dd2baf91a721116a597bddbdfc7ad2)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae9dd2baf91a721116a597bddbdfc7ad2}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad56ac6e16278b6baa01d4c44d70b477c)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad56ac6e16278b6baa01d4c44d70b477c}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a7145bba337451de491ea248096411e5d)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7145bba337451de491ea248096411e5d}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1afd02c33d0a243fe5dd400fc71296cfa1)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1afd02c33d0a243fe5dd400fc71296cfa1}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a0716dbb992bcd3c4d2a6c4d954159346)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0716dbb992bcd3c4d2a6c4d954159346}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a1659cd370a5b28ff093268db31822f34)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1659cd370a5b28ff093268db31822f34}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a27d7dea9c36dacdda0778d2d25bac2cb)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a27d7dea9c36dacdda0778d2d25bac2cb}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a420b576a99229b23ae82f3107a6dfe6e)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a420b576a99229b23ae82f3107a6dfe6e}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a9180255c87d43c7208b9787f8e39fb0b)`(`[`SGVector](#classshogun_1_1SGVector)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a9180255c87d43c7208b9787f8e39fb0b}

add vector param 
#### Parameters
* `param` parameter vector itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a99c6cb84d23a8b9798871944bc3e598c)`(bool ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a99c6cb84d23a8b9798871944bc3e598c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a759e9acafa0e20f39370eb6372bbab11)`(char ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a759e9acafa0e20f39370eb6372bbab11}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a5e01b7d96ed92b7bee2bb71c55be581e)`(int8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5e01b7d96ed92b7bee2bb71c55be581e}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1aa5c11fd4a516e2a752a6e223c908cfc9)`(uint8_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa5c11fd4a516e2a752a6e223c908cfc9}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a9980bc979427240ae8e85efc22a8b213)`(int16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a9980bc979427240ae8e85efc22a8b213}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1ad8aa15bfad196f4fd3867e9098a6cd1f)`(uint16_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad8aa15bfad196f4fd3867e9098a6cd1f}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a5eaf2639b87a94a81144f367e85984d4)`(int32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5eaf2639b87a94a81144f367e85984d4}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1ad11781307f38c35eeaf3fb7f28a78a5a)`(uint32_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad11781307f38c35eeaf3fb7f28a78a5a}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1acdbfb22a12a284802353f3776a4f2185)`(int64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1acdbfb22a12a284802353f3776a4f2185}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a56bff8627127d0929c26b9b8b8a58d63)`(uint64_t ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a56bff8627127d0929c26b9b8b8a58d63}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a6f6e97cbb3c106b470d982e0e5fba159)`(`[`float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6f6e97cbb3c106b470d982e0e5fba159}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1afeca39211a0c8f4902583b087cd270b4)`(`[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1afeca39211a0c8f4902583b087cd270b4}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1abd68485eaf8985213c134a2af39cf97c)`(`[`floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1abd68485eaf8985213c134a2af39cf97c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1aa9bed8e484f4c17042d644b8f6b76f21)`(`[`complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa9bed8e484f4c17042d644b8f6b76f21}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a4c4b4f1f6f5e9e9bf4e0a6fdb159da78)`(`[`CSGObject`](#classshogun_1_1CSGObject)` *** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4c4b4f1f6f5e9e9bf4e0a6fdb159da78}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a89dd70971ff27136ec5782f7db6a2a89)`(`[`SGString`](#classshogun_1_1SGString)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a89dd70971ff27136ec5782f7db6a2a89}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1adc0edb79768c0aad766d20d08653bea5)`(`[`SGString`](#classshogun_1_1SGString)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1adc0edb79768c0aad766d20d08653bea5}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a783d466af4736e127aa69b020bcb11b3)`(`[`SGString`](#classshogun_1_1SGString)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a783d466af4736e127aa69b020bcb11b3}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a1c83cb831303e5a6175356540dfb02dd)`(`[`SGString`](#classshogun_1_1SGString)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1c83cb831303e5a6175356540dfb02dd}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1acfa9178ebc95f1f3ade075e6d00cb3df)`(`[`SGString`](#classshogun_1_1SGString)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1acfa9178ebc95f1f3ade075e6d00cb3df}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a0f677258ae02443888cc814ed14715bb)`(`[`SGString`](#classshogun_1_1SGString)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0f677258ae02443888cc814ed14715bb}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a928f95a69bd9a0815b7c58eadb0776fd)`(`[`SGString`](#classshogun_1_1SGString)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a928f95a69bd9a0815b7c58eadb0776fd}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a5bb886825c3c266697721222a4fde44a)`(`[`SGString`](#classshogun_1_1SGString)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5bb886825c3c266697721222a4fde44a}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1aa43b62c33386e166d91534dc03833706)`(`[`SGString`](#classshogun_1_1SGString)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa43b62c33386e166d91534dc03833706}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a4fd89ea079feea6fd9093b492cfebf18)`(`[`SGString`](#classshogun_1_1SGString)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4fd89ea079feea6fd9093b492cfebf18}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a74c1fef94729d4352ac26123a89ce846)`(`[`SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a74c1fef94729d4352ac26123a89ce846}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a7cf82b927fb631fcb857a5020bd93802)`(`[`SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7cf82b927fb631fcb857a5020bd93802}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a1a6e323eb0786ebc4be5e519b8f5669d)`(`[`SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1a6e323eb0786ebc4be5e519b8f5669d}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a2f353ea085fd5b78e1f0e0d444b76c72)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2f353ea085fd5b78e1f0e0d444b76c72}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a247692a3f9b35e35ff3ff6cdfc7fce8a)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a247692a3f9b35e35ff3ff6cdfc7fce8a}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a0609ffd5a3a29db161270797416c96a0)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0609ffd5a3a29db161270797416c96a0}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1ae0b22f14b3e0d07bcb5c4292744892ad)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae0b22f14b3e0d07bcb5c4292744892ad}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a51455117274de3a5d81cbd8fb9b93370)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a51455117274de3a5d81cbd8fb9b93370}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1ae97e214e9f55dfaa50d1fed49b544042)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae97e214e9f55dfaa50d1fed49b544042}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a2c55bc4cbb476a1e50213d63401c9bed)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2c55bc4cbb476a1e50213d63401c9bed}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a92f4e79eb50adff9800e2d8460c764b3)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a92f4e79eb50adff9800e2d8460c764b3}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1a2389775100e24de128d81c6a37f16886)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2389775100e24de128d81c6a37f16886}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1af1aedbd047eadf956e04ee24fa81d32d)`(`[`SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1af1aedbd047eadf956e04ee24fa81d32d}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1ada59ae2a130415961c78dbc8b6860777)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1ada59ae2a130415961c78dbc8b6860777}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1aee33b3b57cd4a5afa17e359f145ffd3e)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1aee33b3b57cd4a5afa17e359f145ffd3e}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1aead47c41bbe49b6b72930bf80d44d526)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1aead47c41bbe49b6b72930bf80d44d526}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add_matrix`](#classshogun_1_1Parameter_1ad2c42d9240e9b052f9a4521b5df803e7)`(`[`SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > ** param,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_y,`[`index_t`](#common_8h_1a6da8132ec1234c0d616142e3a246f858)` * length_x,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad2c42d9240e9b052f9a4521b5df803e7}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `length_y` y size of matrix 

* `length_x` x size of matrix 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a46f0301db2db9fd7e22e007ed9ec570f)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< bool > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a46f0301db2db9fd7e22e007ed9ec570f}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a7376f3432122f21b31597b7ca2ec40df)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< char > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a7376f3432122f21b31597b7ca2ec40df}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab0826f32098647d7cf4b6b32fd1a1844)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab0826f32098647d7cf4b6b32fd1a1844}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4b156572e6f38de23b85cebc6e3e846d)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4b156572e6f38de23b85cebc6e3e846d}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a69ab639b8df650c891fac73352d1b0cd)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a69ab639b8df650c891fac73352d1b0cd}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a207c0959917ea56052aa7d7bb8a9417a)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a207c0959917ea56052aa7d7bb8a9417a}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a0524d1dfc18cd93d5b9cca960124a8d6)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a0524d1dfc18cd93d5b9cca960124a8d6}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4e781f01c6fa69c73462b80da15969b0)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4e781f01c6fa69c73462b80da15969b0}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a5c611cb2a9502f7d3bb48b36d59fc7e8)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< int64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5c611cb2a9502f7d3bb48b36d59fc7e8}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a95643ad859905498adc65f3f34c6dec8)`(`[`SGMatrix`](#classshogun_1_1SGMatrix)`< uint64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a95643ad859905498adc65f3f34c6dec8}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aced2db64755e06410daa2948a7a7ba13)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aced2db64755e06410daa2948a7a7ba13}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4646a8edaa6780e68df47c11cc10efeb)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4646a8edaa6780e68df47c11cc10efeb}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aefdb466d3ed95f8b9a1e6232aa83acc2)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aefdb466d3ed95f8b9a1e6232aa83acc2}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aa9692e73974f02c1ed776943f348b63c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa9692e73974f02c1ed776943f348b63c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a59dd091d6448fb46f96c359af880a5cf)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [CSGObject`](#classshogun_1_1CSGObject)` *> * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a59dd091d6448fb46f96c359af880a5cf}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ae04ad7e38ec464214105c638827c990c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< bool > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ae04ad7e38ec464214105c638827c990c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aa6785872fdbda058e0a3779114128e6c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< char > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aa6785872fdbda058e0a3779114128e6c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1abfcff6ba7dca8e9810bc5e02ed373f7b)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1abfcff6ba7dca8e9810bc5e02ed373f7b}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab5d7835ccb51c06c19963e02c7b0b1d8)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab5d7835ccb51c06c19963e02c7b0b1d8}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4ae011cb1c7c7641529b15e5c3a86f15)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4ae011cb1c7c7641529b15e5c3a86f15}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1abd0e2dbd734d8a9856b3f47987a89265)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1abd0e2dbd734d8a9856b3f47987a89265}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a3e6bdd05e6bda51eb95c7a7bb2eb9a79)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3e6bdd05e6bda51eb95c7a7bb2eb9a79}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a3be1a15b6e5f5baa11d2ad35a41cbe2e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a3be1a15b6e5f5baa11d2ad35a41cbe2e}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a30882bc5ea58101361a12ab7ed67f225)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< int64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a30882bc5ea58101361a12ab7ed67f225}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad8b55580bbdaa3f3b154acd83a9aabf4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString`](#classshogun_1_1SGString)`< uint64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad8b55580bbdaa3f3b154acd83a9aabf4}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a1ee27de715b7a796747e9f129343fa85)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString](#classshogun_1_1SGString)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1ee27de715b7a796747e9f129343fa85}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aacd132e07ff29667400098c310991821)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString](#classshogun_1_1SGString)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aacd132e07ff29667400098c310991821}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad01dc6aab08a90865cd0ac3eb7444a5e)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGString](#classshogun_1_1SGString)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad01dc6aab08a90865cd0ac3eb7444a5e}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a638fb356f638a0a62c5f2831aafc5a18)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< bool > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a638fb356f638a0a62c5f2831aafc5a18}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a2e4f13bf29962fcec9fde2abf9e6c8b4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< char > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2e4f13bf29962fcec9fde2abf9e6c8b4}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a8ccbcd20869f91db5d380f7d470a2ed4)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a8ccbcd20869f91db5d380f7d470a2ed4}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1acc2e9801c6421c3053696a40ff18f452)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint8_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1acc2e9801c6421c3053696a40ff18f452}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a90ca1bef6cc5807e20d94cb409ac6e3c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a90ca1bef6cc5807e20d94cb409ac6e3c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a6c950defbdd55fcfd66a71d7e492dc06)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint16_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6c950defbdd55fcfd66a71d7e492dc06}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1afd5e308492c45cbfe61ab0c3a2fad7ac)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1afd5e308492c45cbfe61ab0c3a2fad7ac}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a313a6957ceb3706fca6ccda132f7552a)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint32_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a313a6957ceb3706fca6ccda132f7552a}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a6402d74ca0ff2f844f84423325ab359f)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< int64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a6402d74ca0ff2f844f84423325ab359f}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a22b4938f128f6413985e45ee2f26de85)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector`](#classshogun_1_1SGSparseVector)`< uint64_t > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a22b4938f128f6413985e45ee2f26de85}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ac2374ffc0ebd281ab21852fedae3bc17)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ac2374ffc0ebd281ab21852fedae3bc17}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab614f8ad64f2fbc9199e61d422e55f86)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab614f8ad64f2fbc9199e61d422e55f86}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4aa02fe85325ae7d50efc47daedcbf31)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4aa02fe85325ae7d50efc47daedcbf31}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a847a3a386ccc5b390c7d181bff51e62c)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [SGSparseVector](#classshogun_1_1SGSparseVector)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a847a3a386ccc5b390c7d181bff51e62c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a975b17e482a9588de972ddd34e871d12)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< bool > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a975b17e482a9588de972ddd34e871d12}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aea9206df60fa836d1b8ce7bf0d8229aa)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< char > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aea9206df60fa836d1b8ce7bf0d8229aa}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a5852b1a3c79a9757bdfe77726995e62a)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a5852b1a3c79a9757bdfe77726995e62a}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aea28efc49f8847d9c7599f479b8e86ae)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint8_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aea28efc49f8847d9c7599f479b8e86ae}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1aecc935095b109cfe015388a03c75d938)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1aecc935095b109cfe015388a03c75d938}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1affc3bd50a7efa85bf6bbf4d0d860c859)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint16_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1affc3bd50a7efa85bf6bbf4d0d860c859}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a4fcf0077e96eb22e4dcfb0e9de207046)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a4fcf0077e96eb22e4dcfb0e9de207046}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a2276e9afced4dbcf893bbcf78182c622)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint32_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2276e9afced4dbcf893bbcf78182c622}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a1669daabdd5401580a9d8b878a2e50c0)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< int64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a1669daabdd5401580a9d8b878a2e50c0}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ab0b9f37601cd6f8b8f60ee2f3bba1fe0)`(`[`SGSparseMatrix`](#classshogun_1_1SGSparseMatrix)`< uint64_t > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ab0b9f37601cd6f8b8f60ee2f3bba1fe0}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a129d07acca46eac10eb0bb1bd10baf97)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [float32_t`](#common_8h_1a4611b605e45ab401f02cab15c5e38715)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a129d07acca46eac10eb0bb1bd10baf97}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad8ed504425869cf9822b0e98b2686abe)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad8ed504425869cf9822b0e98b2686abe}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1ad5f5fb54beb459ac060f2ad749562462)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [floatmax_t`](#common_8h_1a4ca6ad9dd54ef5b6e900e44b78cc2040)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad5f5fb54beb459ac060f2ad749562462}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a9d412290659a94be75db2a4e773538e0)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [complex128_t`](#common_8h_1a85560c2137997d34dee0a2eab636d7aa)` > * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a9d412290659a94be75db2a4e773538e0}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `public void `[`add`](#classshogun_1_1Parameter_1a2e76a8889309e20d48f3dee8f625eb7c)`(`[`SGSparseMatrix](#classshogun_1_1SGSparseMatrix)< [CSGObject`](#classshogun_1_1CSGObject)` *> * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1a2e76a8889309e20d48f3dee8f625eb7c}

add matrix param 
#### Parameters
* `param` parameter matrix itself 

* `name` name of parameter 

* `description` description of parameter

#### `protected `[`DynArray](#classshogun_1_1DynArray)< [TParameter`](#structshogun_1_1TParameter)` * > `[`m_params`](#classshogun_1_1Parameter_1a74840f2c3a094c65840041da2fcad2d8) {#classshogun_1_1Parameter_1a74840f2c3a094c65840041da2fcad2d8}

array of parameters

#### `protected virtual void `[`add_type`](#classshogun_1_1Parameter_1ad9b0009eed07489043dc344ceb5b3055)`(const `[`TSGDataType`](#structshogun_1_1TSGDataType)` * type,void * param,const char * name,const char * description)` {#classshogun_1_1Parameter_1ad9b0009eed07489043dc344ceb5b3055}

add new type 
#### Parameters
* `type` type to be added 

* `param` pointer to parameter 

* `name` name of parameter 

* `description` description of parameter

