# Julia-tutorials-for-ChEs
This repository contains tutorials for the Julia programming language that are especially tailored for chemical and biochemical engineers (ChEs and BioChEs). In addition, the tutorials shown here emphasize the use of the free and open-source software package [ModelingToolkit.jl](https://docs.sciml.ai/ModelingToolkit/stable/) and its ability to combine  symbolic and numeric approaches to solve problems of interest to ChEs and BioChEs. Combining symbolic and numeric approaches in this way enables both more effective solution methods and more efficient compiled numerical code for existing methods. In addition, a pure Julia, single-language approach helps to coordinate the various parts of the overall computational method. ModelingToolkit.jl can also perform either causal or acausal simulations, in contrast to [Modelica](https://modelica.org/), which is strictly acausual, and [Simulink](https://www.mathworks.com/products/simulink.html), which is strictly causal. 

There are several software systems in the Julia ecosystem that are built on top of ModelingToolkit.jl to take advantage of its features. Examples include the following:

| Software | Purpose| License Type|
|  ---  |  ---  |  ---  |
|[Catalyst.jl](https://docs.sciml.ai/Catalyst/stable/)| Simulating chemical reaction networks| Free and open source |
|[MethodOfLines.jl](https://docs.sciml.ai/MethodOfLines/stable/)| Solving PDEs|  Free and open source |
|[ProcessSimulator.jl](https://github.com/SciML/ProcessSimulator.jl)| Simulating chemical processes| Free and open source |
|[Conductor.jl](https://wsphillips.github.io/Conductor.jl/stable/)| Computational neuroscience| Free and open source |
|[Neuroblox](https://www.neuroblox.ai/)| Computational neuroscience and psychiatry| Free for non-commercial use, otherwise monthly fee |
|[PumasAI](https://pumas.ai/)| Pharmacometrics | Free for non-commercial use, otherwise monthly fee |
|[Dyad](https://juliahub.com/products/dyad)| AI-assisted industrial simulations| Free for non-commercial use, otherwise monthly fee |

Catalyst.jl and MethodOfLines.jl from the above table will be included in this tutorial. Since all of the above software systems have ModelingToolkit.jl as their foundation, familiarity with ModelingToolkit.jl greatly facilitates their use.  

Although many tutorials exist for the Julia programming language, none have the focus of this tutorial, and many are somewhat short on using effective pedagogical methods to make learning easy (or at least easier!) for the neophyte. The tutorials here seek to address these needs.
