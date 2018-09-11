---
classname: "shogun::lbfgs_parameter_t"
type: "struct"
---

# struct `shogun::lbfgs_parameter_t` {#structshogun_1_1lbfgs__parameter__t}

L-BFGS optimization parameters. Call [lbfgs_parameter_init()](#group__liblbfgs__api_1ga67d513e0b18261defa4c3aec5a8c95fa) function to initialize parameters to the default values.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
`public int `[`m`](#structshogun_1_1lbfgs__parameter__t_1a742204794ea328ba293fe59cec79b990) | The number of corrections to approximate the inverse hessian matrix. The L-BFGS routine stores the computation results of previous [m](#structshogun_1_1lbfgs__parameter__t_1a742204794ea328ba293fe59cec79b990) iterations to approximate the inverse hessian matrix of the current iteration. This parameter controls the size of the limited memories (corrections). The default value is `6`. Values less than `3` are not recommended. Large values will result in excessive computing time.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`epsilon`](#structshogun_1_1lbfgs__parameter__t_1a0bde8d297e19e73b20b99110ba38f7bd) | Epsilon for convergence test. This parameter determines the accuracy with which the solution is to be found. A minimization terminates when \|\|g\|\| < [epsilon](#structshogun_1_1lbfgs__parameter__t_1a0bde8d297e19e73b20b99110ba38f7bd) * max(1, \|\|x\|\|), where \|\|.\|\| denotes the Euclidean (L2) norm. The default value is `1e-5`.
`public int `[`past`](#structshogun_1_1lbfgs__parameter__t_1acc958e04c64d7f8589872c70820fef8d) | Distance for delta-based convergence test. This parameter determines the distance, in iterations, to compute the rate of decrease of the objective function. If the value of this parameter is zero, the library does not perform the delta-based convergence test. The default value is `0`.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`delta`](#structshogun_1_1lbfgs__parameter__t_1a1444325087d751e0a2fd6157b540b9fb) | Delta for convergence test. This parameter determines the minimum rate of decrease of the objective function. The library stops iterations when the following condition is met: (f' - f) / f < [delta](#structshogun_1_1lbfgs__parameter__t_1a1444325087d751e0a2fd6157b540b9fb), where f' is the objective value of [past](#structshogun_1_1lbfgs__parameter__t_1acc958e04c64d7f8589872c70820fef8d) iterations ago, and f is the objective value of the current iteration. The default value is `0`.
`public int `[`max_iterations`](#structshogun_1_1lbfgs__parameter__t_1a82eead8e5a402b5c5da8b449073bad45) | The maximum number of iterations. The [lbfgs()](#namespaceshogun_1a10b3d59fc1354b2551a4bf7fc0ac0f00) function terminates an optimization process with LBFGSERR_MAXIMUMITERATION status code when the iteration count exceedes this parameter. Setting this parameter to zero continues an optimization process until a convergence or error. The default value is `0`.
`public int `[`linesearch`](#structshogun_1_1lbfgs__parameter__t_1ae97f89415ae32583797aae0b6017754b) | The line search algorithm. This parameter specifies a line search algorithm to be used by the L-BFGS routine.
`public int `[`max_linesearch`](#structshogun_1_1lbfgs__parameter__t_1a2e0d53974a0ed121040194ee75bf3a37) | The maximum number of trials for the line search. This parameter controls the number of function and gradients evaluations per iteration for the line search routine. The default value is `20`.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`min_step`](#structshogun_1_1lbfgs__parameter__t_1a4a63ca9be8be892a9d7c46b330a99c93) | The minimum step of the line search routine. The default value is `1e-20`. This value need not be modified unless the exponents are too large for the machine being used, or unless the problem is extremely badly scaled (in which case the exponents should be increased).
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`max_step`](#structshogun_1_1lbfgs__parameter__t_1ad23a0b15d2f083c41ee0bc117411f548) | The maximum step of the line search. The default value is `1e+20`. This value need not be modified unless the exponents are too large for the machine being used, or unless the problem is extremely badly scaled (in which case the exponents should be increased).
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`ftol`](#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae) | A parameter to control the accuracy of the line search routine. The default value is `1e-4`. This parameter should be greater than zero and smaller than `0.5`.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`wolfe`](#structshogun_1_1lbfgs__parameter__t_1a75ecfb6697ae4e9bab5f526c0b84243f) | A coefficient for the Wolfe condition. This parameter is valid only when the backtracking line-search algorithm is used with the Wolfe condition, LBFGS_LINESEARCH_BACKTRACKING_STRONG_WOLFE or LBFGS_LINESEARCH_BACKTRACKING_WOLFE . The default value is `0.9`. This parameter should be greater the [ftol](#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae) parameter and smaller than `1.0`.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gtol`](#structshogun_1_1lbfgs__parameter__t_1a1ac7df48f3ab2e621c3acfedc33c6209) | A parameter to control the accuracy of the line search routine. The default value is `0.9`. If the function and gradient evaluations are inexpensive with respect to the cost of the iteration (which is sometimes the case when solving very large problems) it may be advantageous to set this parameter to a small value. A typical small value is `0.1`. This parameter shuold be greater than the [ftol](#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae) parameter (`1e-4`) and smaller than `1.0`.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`xtol`](#structshogun_1_1lbfgs__parameter__t_1a7e3b76d3d379235b397badb4ba611e58) | The machine precision for floating-point values. This parameter must be a positive value set by a client program to estimate the machine precision. The line search routine will terminate with the status code (LBFGSERR_ROUNDING_ERROR) if the relative width of the interval of uncertainty is less than this parameter.
`public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`orthantwise_c`](#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286) | Coeefficient for the L1 norm of variables. This parameter should be set to zero for standard minimization problems. Setting this parameter to a positive value activates Orthant-Wise Limited-memory Quasi-Newton (OWL-QN) method, which minimizes the objective function F(x) combined with the L1 norm \|x\| of the variables, {F(x) + C \|x\|}. This parameter is the coeefficient for the \|x\|, i.e., C. As the L1 norm \|x\| is not differentiable at zero, the library modifies function and gradient evaluations from a client program suitably; a client program thus have only to return the function value F(x) and gradients G(x) as usual. The default value is zero.
`public int `[`orthantwise_start`](#structshogun_1_1lbfgs__parameter__t_1a434d09e62b683b07b9d03f80e581f394) | Start index for computing L1 norm of the variables. This parameter is valid only for OWL-QN method (i.e., [orthantwise_c](#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286) != 0). This parameter b (0 <= b < N) specifies the index number from which the library computes the L1 norm of the variables x, \|x\| := \|x_{b}\| + \|x_{b+1}\| + ... + \|x_{N}\| . In other words, variables x_1, ..., x_{b-1} are not used for computing the L1 norm. Setting b (0 < b < N), one can protect variables, x_1, ..., x_{b-1} (e.g., a bias term of logistic regression) from being regularized. The default value is zero.
`public int `[`orthantwise_end`](#structshogun_1_1lbfgs__parameter__t_1acd13e81daee6bc88cbca9817b57e6dc5) | End index for computing L1 norm of the variables. This parameter is valid only for OWL-QN method (i.e., [orthantwise_c](#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286) != 0). This parameter e (0 < e <= N) specifies the index number at which the library stops computing the L1 norm of the variables x,

## Members

#### `public int `[`m`](#structshogun_1_1lbfgs__parameter__t_1a742204794ea328ba293fe59cec79b990) {#structshogun_1_1lbfgs__parameter__t_1a742204794ea328ba293fe59cec79b990}

The number of corrections to approximate the inverse hessian matrix. The L-BFGS routine stores the computation results of previous [m](#structshogun_1_1lbfgs__parameter__t_1a742204794ea328ba293fe59cec79b990) iterations to approximate the inverse hessian matrix of the current iteration. This parameter controls the size of the limited memories (corrections). The default value is `6`. Values less than `3` are not recommended. Large values will result in excessive computing time.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`epsilon`](#structshogun_1_1lbfgs__parameter__t_1a0bde8d297e19e73b20b99110ba38f7bd) {#structshogun_1_1lbfgs__parameter__t_1a0bde8d297e19e73b20b99110ba38f7bd}

Epsilon for convergence test. This parameter determines the accuracy with which the solution is to be found. A minimization terminates when ||g|| < [epsilon](#structshogun_1_1lbfgs__parameter__t_1a0bde8d297e19e73b20b99110ba38f7bd) * max(1, ||x||), where ||.|| denotes the Euclidean (L2) norm. The default value is `1e-5`.

#### `public int `[`past`](#structshogun_1_1lbfgs__parameter__t_1acc958e04c64d7f8589872c70820fef8d) {#structshogun_1_1lbfgs__parameter__t_1acc958e04c64d7f8589872c70820fef8d}

Distance for delta-based convergence test. This parameter determines the distance, in iterations, to compute the rate of decrease of the objective function. If the value of this parameter is zero, the library does not perform the delta-based convergence test. The default value is `0`.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`delta`](#structshogun_1_1lbfgs__parameter__t_1a1444325087d751e0a2fd6157b540b9fb) {#structshogun_1_1lbfgs__parameter__t_1a1444325087d751e0a2fd6157b540b9fb}

Delta for convergence test. This parameter determines the minimum rate of decrease of the objective function. The library stops iterations when the following condition is met: (f' - f) / f < [delta](#structshogun_1_1lbfgs__parameter__t_1a1444325087d751e0a2fd6157b540b9fb), where f' is the objective value of [past](#structshogun_1_1lbfgs__parameter__t_1acc958e04c64d7f8589872c70820fef8d) iterations ago, and f is the objective value of the current iteration. The default value is `0`.

#### `public int `[`max_iterations`](#structshogun_1_1lbfgs__parameter__t_1a82eead8e5a402b5c5da8b449073bad45) {#structshogun_1_1lbfgs__parameter__t_1a82eead8e5a402b5c5da8b449073bad45}

The maximum number of iterations. The [lbfgs()](#namespaceshogun_1a10b3d59fc1354b2551a4bf7fc0ac0f00) function terminates an optimization process with LBFGSERR_MAXIMUMITERATION status code when the iteration count exceedes this parameter. Setting this parameter to zero continues an optimization process until a convergence or error. The default value is `0`.

#### `public int `[`linesearch`](#structshogun_1_1lbfgs__parameter__t_1ae97f89415ae32583797aae0b6017754b) {#structshogun_1_1lbfgs__parameter__t_1ae97f89415ae32583797aae0b6017754b}

The line search algorithm. This parameter specifies a line search algorithm to be used by the L-BFGS routine.

#### `public int `[`max_linesearch`](#structshogun_1_1lbfgs__parameter__t_1a2e0d53974a0ed121040194ee75bf3a37) {#structshogun_1_1lbfgs__parameter__t_1a2e0d53974a0ed121040194ee75bf3a37}

The maximum number of trials for the line search. This parameter controls the number of function and gradients evaluations per iteration for the line search routine. The default value is `20`.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`min_step`](#structshogun_1_1lbfgs__parameter__t_1a4a63ca9be8be892a9d7c46b330a99c93) {#structshogun_1_1lbfgs__parameter__t_1a4a63ca9be8be892a9d7c46b330a99c93}

The minimum step of the line search routine. The default value is `1e-20`. This value need not be modified unless the exponents are too large for the machine being used, or unless the problem is extremely badly scaled (in which case the exponents should be increased).

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`max_step`](#structshogun_1_1lbfgs__parameter__t_1ad23a0b15d2f083c41ee0bc117411f548) {#structshogun_1_1lbfgs__parameter__t_1ad23a0b15d2f083c41ee0bc117411f548}

The maximum step of the line search. The default value is `1e+20`. This value need not be modified unless the exponents are too large for the machine being used, or unless the problem is extremely badly scaled (in which case the exponents should be increased).

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`ftol`](#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae) {#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae}

A parameter to control the accuracy of the line search routine. The default value is `1e-4`. This parameter should be greater than zero and smaller than `0.5`.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`wolfe`](#structshogun_1_1lbfgs__parameter__t_1a75ecfb6697ae4e9bab5f526c0b84243f) {#structshogun_1_1lbfgs__parameter__t_1a75ecfb6697ae4e9bab5f526c0b84243f}

A coefficient for the Wolfe condition. This parameter is valid only when the backtracking line-search algorithm is used with the Wolfe condition, LBFGS_LINESEARCH_BACKTRACKING_STRONG_WOLFE or LBFGS_LINESEARCH_BACKTRACKING_WOLFE . The default value is `0.9`. This parameter should be greater the [ftol](#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae) parameter and smaller than `1.0`.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`gtol`](#structshogun_1_1lbfgs__parameter__t_1a1ac7df48f3ab2e621c3acfedc33c6209) {#structshogun_1_1lbfgs__parameter__t_1a1ac7df48f3ab2e621c3acfedc33c6209}

A parameter to control the accuracy of the line search routine. The default value is `0.9`. If the function and gradient evaluations are inexpensive with respect to the cost of the iteration (which is sometimes the case when solving very large problems) it may be advantageous to set this parameter to a small value. A typical small value is `0.1`. This parameter shuold be greater than the [ftol](#structshogun_1_1lbfgs__parameter__t_1ac949822695850a81d1cf51232dc8caae) parameter (`1e-4`) and smaller than `1.0`.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`xtol`](#structshogun_1_1lbfgs__parameter__t_1a7e3b76d3d379235b397badb4ba611e58) {#structshogun_1_1lbfgs__parameter__t_1a7e3b76d3d379235b397badb4ba611e58}

The machine precision for floating-point values. This parameter must be a positive value set by a client program to estimate the machine precision. The line search routine will terminate with the status code (LBFGSERR_ROUNDING_ERROR) if the relative width of the interval of uncertainty is less than this parameter.

#### `public `[`float64_t`](#common_8h_1ac55f3ae81b5bc9053760baacf57e47f4)` `[`orthantwise_c`](#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286) {#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286}

Coeefficient for the L1 norm of variables. This parameter should be set to zero for standard minimization problems. Setting this parameter to a positive value activates Orthant-Wise Limited-memory Quasi-Newton (OWL-QN) method, which minimizes the objective function F(x) combined with the L1 norm |x| of the variables, {F(x) + C |x|}. This parameter is the coeefficient for the |x|, i.e., C. As the L1 norm |x| is not differentiable at zero, the library modifies function and gradient evaluations from a client program suitably; a client program thus have only to return the function value F(x) and gradients G(x) as usual. The default value is zero.

#### `public int `[`orthantwise_start`](#structshogun_1_1lbfgs__parameter__t_1a434d09e62b683b07b9d03f80e581f394) {#structshogun_1_1lbfgs__parameter__t_1a434d09e62b683b07b9d03f80e581f394}

Start index for computing L1 norm of the variables. This parameter is valid only for OWL-QN method (i.e., [orthantwise_c](#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286) != 0). This parameter b (0 <= b < N) specifies the index number from which the library computes the L1 norm of the variables x, |x| := |x_{b}| + |x_{b+1}| + ... + |x_{N}| . In other words, variables x_1, ..., x_{b-1} are not used for computing the L1 norm. Setting b (0 < b < N), one can protect variables, x_1, ..., x_{b-1} (e.g., a bias term of logistic regression) from being regularized. The default value is zero.

#### `public int `[`orthantwise_end`](#structshogun_1_1lbfgs__parameter__t_1acd13e81daee6bc88cbca9817b57e6dc5) {#structshogun_1_1lbfgs__parameter__t_1acd13e81daee6bc88cbca9817b57e6dc5}

End index for computing L1 norm of the variables. This parameter is valid only for OWL-QN method (i.e., [orthantwise_c](#structshogun_1_1lbfgs__parameter__t_1a139627b84155169b0fdd68e4c106b286) != 0). This parameter e (0 < e <= N) specifies the index number at which the library stops computing the L1 norm of the variables x,

