##  Basic introduction to Julia and ModelingToolkit.jl

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This tutorial introduces the Julia programming language and the ModelingToolkit.jl (MTK) package in Julia using the solving of systems of nonlinear algebraic equations as an illustrative example. Julia is a free and open-source programming language developed at MIT specifically for high-performance computing in science and engineering and for machine learning applications.  ModelingToolkit is a symbolic-numeric modeling package for use in Julia that provides automated equation manipulations to facilitate numerical processing, among other features.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This tutorial is intended for those who already have some programming experience (e.g., with MATLAB) and who want to learn simultaneously the basics of Julia and ModelingToolkit.jl in an efficient way so that these tools can be applied to modeling problems. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The numerical approach used in this tutorial is to search directly for the value of x where f<sub>i</sub>(x) = 0 (where x is a vector of independent variables), instead of converting the problem into an optimization problem by searching for the value of x where $\sum_{i}$ f<sub>i</sub>(x)^2 is minimized. The latter approach is the approach used by the fsolve() function in MATLAB and is inefficient compared to the approach used here.

###  Functions illustrated:
<span style="font-family:Consolas; font-size:1em;">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; fill(), range(), collect(), sum(), round(), rand(),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; maximum(), max(), minimum(), min(), abs(), println(),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; typeof(), fieldnames(), Symbolics.value(), Symbolics.jacobian(),<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Symbolics.jacobian_sparsity(), Symbolics.substitute()</span><br>

###  Metaprogramming macros illustrated: 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span style="font-family:Consolas; font-size:1em;">@time, @show, @doc, @variables, @parameters, @named</span>
<br>

###  Concepts illustrated:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;vector index notation<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;concatenation of vectors<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;function broadcasting<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;list comprehension<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dictionaries<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;begin/end blocks<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;garbage collection<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Just in Time (JIT) compiling<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;metaprogramming with macros<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;keywords in a function call<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;automatic type promotion<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;symbolic algebra<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;automatic differentiation<br>

###  Numerical algorithms illustrated:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Newton Raphson (from NonlinearSolve.jl)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Newton method with trust region (from NonlinearSolve.jl)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;RobustMultiNewton (from NonlinearSolve.jl)<br>
