---
classname: "shogun::RelaxedTreeUtil"
type: "class"
---

# class `shogun::RelaxedTreeUtil` {#classshogun_1_1RelaxedTreeUtil}

Utility class for [CRelaxedTree](#classshogun_1_1CRelaxedTree)

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`estimate_confusion_matrix`](#classshogun_1_1RelaxedTreeUtil_1a5179629e66eb8d02f62c43dee3d2ed26)`(`[`CBaseMulticlassMachine`](#classshogun_1_1CBaseMulticlassMachine)` * machine,`[`CFeatures`](#classshogun_1_1CFeatures)` * X,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * Y,int32_t num_classes)` | estimate confusion matrix with cross validation. 
`public void `[`get_confusion_matrix`](#classshogun_1_1RelaxedTreeUtil_1aa552b319ba602dacab33bf262fef3c65)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & conf_mat,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * gt,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * pred)` | Get confusion matrix. 

## Members

#### `public `[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > `[`estimate_confusion_matrix`](#classshogun_1_1RelaxedTreeUtil_1a5179629e66eb8d02f62c43dee3d2ed26)`(`[`CBaseMulticlassMachine`](#classshogun_1_1CBaseMulticlassMachine)` * machine,`[`CFeatures`](#classshogun_1_1CFeatures)` * X,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * Y,int32_t num_classes)` {#classshogun_1_1RelaxedTreeUtil_1a5179629e66eb8d02f62c43dee3d2ed26}

estimate confusion matrix with cross validation. 
#### Parameters
* `machine` multiclass machine used to compute confusion matrix 

* `X` training data 

* `Y` labels for training data 

* `num_classes` number of classes 

#### Returns
num_classes-by-num_classes confusion matrix.

#### `public void `[`get_confusion_matrix`](#classshogun_1_1RelaxedTreeUtil_1aa552b319ba602dacab33bf262fef3c65)`(`[`SGMatrix](#classshogun_1_1SGMatrix)< [float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` > & conf_mat,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * gt,`[`CMulticlassLabels`](#classshogun_1_1CMulticlassLabels)` * pred)` {#classshogun_1_1RelaxedTreeUtil_1aa552b319ba602dacab33bf262fef3c65}

Get confusion matrix. 
#### Parameters
* `conf_mat` num_class-by-num_class matrix, confusion matrix will be assigned to this 

* `gt` ground-truth labels 

* `pred` predicted labels

