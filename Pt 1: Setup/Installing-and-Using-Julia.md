##  Getting Started with Julia

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To get started with Julia, first download the 64-bit version of the Julia programming language for your particular computer and operating system from the following link:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[https://julialang.org/downloads/](https://julialang.org/downloads/)

Then start Julia so you are at the Julia REPL (read-eval-print loop), which looks like this:


`                _                                                    `<br>
`   _       _ _(_)_     |  Documentation: https://docs.julialang.org`<br>
`   (_)     | (_) (_)    |                                           `<br>
`   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.`<br>
`   | | | | | | |/ _  |  |                                            `<br>
`   | | |_| | | | (_| |  |  Version 1.11.6 (2025-07-09)            `<br>
` _/ |\__ _|_|_|\__ _|  |  Official https://julialang.org/ release`<br>
`|__/                   |                                            `<br>

```julia
julia>
```
Note that `julia>` is the prompt for the top-level Julia REPL. You can access three additional sub-REPLs from the top-level REPL by entering either ], ?, or ; at the Julia REPL.  The structure looks like this: 


`               -----> Enter ] ----->  (@v1.11) Pkg> `<br>
`              /                                     `<br>
`          julia>  -----> Enter ? ----->  help?>     `<br>
`              \                                     `<br>
`               -----> Enter ; -----> shell>         `<br>


Although sub-REPLs are no doubt helpful to the power user, to keep things simple and uniform only the top-level REPL will be used here. If you find yourself in a sub-REPL, you can exit back to the top-level REPL using the backspace key.

Next, the ModelingToolkit, NonlinearSolve, and IJulia packages need to be installed. This can be accomplished as follows: 

```julia
julia>  using Pkg                   # load the Pkg package (and note that this package 
                                    #      does not need installation)
julia>  Pkg.add("ModelingToolkit")  # install ModelingToolkit package
julia>  Pkg.add("NonlinearSolve")   # install NonlinearSolve package
julia>  Pkg.add("IJulia")           # install IJulia package
```
The # symbol denotes a comment and text after the # symbol is not executed. The package version numbers and upgrade status of installed packages are obtained by the following statement:

```julia
julia>  Pkg.status() 
```
<br>
Typical information producted by the statement above is as follows:

<span style="font-family:Consolas; font-size:1em;">
<div>
   <blockquote>
  Status `C:\Users\dfrey1\.julia\environments\v1.11\Project.toml`<br>
  ⌃ [7073ff75] IJulia v1.29.2<br>
  ⌃ [961ee093] ModelingToolkit v10.14.0<br>
&nbsp;&nbsp;[8913a72c] NonlinearSolve v4.10.0<br>
  Info: Packages marked with ⌃ and ⌅ have new versions available. Those with ⌃ may be<br>
  upgradable, but those with ⌅ are restricted by compatibility constraints from upgrading.<br>
  To see why use `status --outdated`<br>
</blockquote>
</div>
</span>
<br>

Additional potentially useful examples of Pkg package statements are as follows (note again the Pkg package must be previously loaded to employ these statements):

```julia
julia> Pkg.rm("NonlinearSolve")  # remove the NonlinearSolve package
julia> Pkg.update("ModelingToolkit")  # update ModelingToolkit package to newest version
julia> Pkg.update()  # update all packages to newest versions
julia> Pkg.build("IJulia")  # rebuild all connections for IJulia package
```
Help for (almost) any item can be obtain with the @doc macro.  For example, to obtain help with the min() function you can use: 

```julia
julia> @doc min()
```

Output from the above looks like this:

<span style="font-family:Consolas; font-size:1em;">
<div>
   <blockquote>
  min(x, y, ...)<br>
<br>
  Return the minimum of the arguments, with respect to the isless function. If any of the arguments is missing, return missing.<br>
  See also the minimum function to take the minimum element from a collection.<br>
<br>
  Examples<br>
  ≡≡≡≡≡≡≡≡<br>
<br>
  julia> min(2, 5, 1)<br>
  1<br>
<br>
  julia> min(4, missing, 6)<br>
  missing<br>
</blockquote>
</div>
</span>

You can exit from the Julia REPL as follows:

```julia
julia>  exit()  
```

More information about the Package Manager is located here:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[https://docs.julialang.org/en/v1/stdlib/Pkg/](https://docs.julialang.org/en/v1/stdlib/Pkg/)

More information about key packages is located here:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[https://mtk.sciml.ai/stable/](https://mtk.sciml.ai/stable/)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[https://nonlinearsolve.sciml.ai/stable/](https://nonlinearsolve.sciml.ai/stable/)<br>

