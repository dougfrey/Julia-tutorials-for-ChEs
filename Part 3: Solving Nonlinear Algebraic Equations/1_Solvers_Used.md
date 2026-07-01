##  Specifications for the main numerical algorithms used in this tutorial part. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;All the algorithms below have changeable linear subprogram solvers, options for Jacobian calculations, and other adjustable features.

###  Newton method with trust region. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Newton method with trust region is available in NonlinearSolve.jl. The following statement assigns the numerical method definition to `alg_TR` and uses entirely default settings:

```julia
julia> alg_TR = TrustRegion()
```

Below again the numerical method definition is assigned to `alg_TR`, but this time two key options are explicitly selected:

```julia
julia> alg_TR = TrustRegion(autodiff=AutoForwardDiff(),
                            linsolve=SimpleLUFactorization())
```

If you want to use finite differencing for the Jacobian, then use `autodiff=AutoFiniteDiff()` above.

###   Robust MultiNewton method

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The RobustMultiNewton algorithm tries various Newton-based algorithms (Trust Region, Line Search etc.) until it finds one that works.  If this algorithm fails then you definitely have a very difficult problem (or you used a very poor initial guess!). The following statement assigns the numerical method definition to <span style="font-family:Consolas; font-size:1em;">alg_RMN</span>:

```julia
julia> alg_RMN = RobustMultiNewton(autodiff=AutoForwardDiff(),
                                   linsolve=SimpleLUFactorization())
```

###  Newton Raphson method

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;As above, the following statement assigns the definition of a pure Newton Raphson solver to <span style="font-family:Consolas; font-size:1em;">alg_NR</span>:

```julia
julia> alg_NR = NewtonRaphson(autodiff=AutoForwardDiff(),
                              linsolve=SimpleLUFactorization())
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;If you want to know more about any of the numerical methods used above, such as what the adjustable options are, then use the `@doc` macro as mentioned earlier.  For example, to find out more about TrustRegion(), use the following:

```julia
julia> @doc TrustRegion()
```

The above command produces the following output:

<span style="font-family:Consolas; font-size:1em;">
<div>
   <blockquote>
TrustRegion(;<br>
    concrete_jac = nothing, linsolve = nothing,<br>
    radius_update_scheme = RadiusUpdateSchemes.Simple, max_trust_radius::Real = 0 // 1,<br>
    initial_trust_radius::Real = 0 // 1, step_threshold::Real = 1 // 10000,<br>
    shrink_threshold::Real = 1 // 4, expand_threshold::Real = 3 // 4,<br>
    shrink_factor::Real = 1 // 4, expand_factor::Real = 2 // 1,<br>
    max_shrink_times::Int = 32,<br>
    vjp_autodiff = nothing, autodiff = nothing, jvp_autodiff = nothing<br>
)<br>
<br>
An advanced TrustRegion implementation with support for efficient handling of sparse matrices via colored<br>
automatic differentiation and preconditioned linear solvers. Designed for large-scale and<br> 
numerically-difficult nonlinear systems.<br>
<br>
Keyword Arguments:<br>
radius_update_scheme: the scheme used to update the trust region radius. Defaults to RadiusUpdateSchemes.Simple.<br>
See RadiusUpdateSchemes for more details. For a review on trust region radius update schemes, see yuan2015recent.<br>
For the remaining arguments, see NonlinearSolveFirstOrder.GenericTrustRegionScheme documentation.<br>
</blockquote>
</div>
</span>
