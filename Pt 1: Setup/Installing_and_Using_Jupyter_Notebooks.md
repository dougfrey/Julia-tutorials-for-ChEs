## Installing and Using the Jupyter Notebook System

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Jupyter notebooks are the primary means to implement this tutorial and are widely used as a platform in general to share computational methods and results. For example, Google Colab and SaturnCloud are a cloud-based Jupyter notebook enviroments available for free. For this tutorial we will install the Jupyter notebook system on your local computer instead of using a cloud-based environment. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To begin, first start the Julia REPL and then make the IJulia package availabe for use as follows: 

```julia
julia> using IJulia  
```
Next, start Jupyter Notebooks as follows:

```julia
julia> notebook()  
```
The first time you run the above statement, you will be prompted to install "Miniconda", which you should do.  Then, you should be viewing the Jupyter notebook system homepage. Look at the upper right of the screen on this homepage and find a dropdown button labelled "New". Using that button open a new notebook, which is one of several options. As the notebook opens, you will be prompted to open a "kernel", which is the computer language system you want to use.  Python will be one choice since it is installed by default.  Don't select Python but instead look for and select the Julia kernel.  If there is no Julia kernel to select, then you will need to exit from the Jupyter notebook and also shut down your Julia REPL session where you executed the notebook() function since it is no longer usable.  Then open a new Julia REPL and then rebuild all the connections for IJulia using the following:

```julia
julia> using Pkg
julia> Pkg.build("IJulia")  
```
Then start over from the beginning of this section and see if you can create a new Jupyter notebook with Julia as the selected computer language.  If you can, then download this tutorial (that you are now using) from the following link and put it somewhere on your computer that you can find:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Julia-ModelingToolkit Tutorial](https://www.youtube.com/watch?v=HW29067qVWk&t)

Next, "upload" the Jupyter notebook you just put on your computer by going to the Jupyter notebook homepage and select the "Upload" button in the upper right of your screen.  "Upload" here means to upload from your computer into the Jupyter notebook system. If this all works then you can switch to the Jupyter notebook version of this tutorial.

A helpful YouTube tutorial explaining the purpose of Jupyter notebooks and how to use them is here:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[https://www.youtube.com/watch?v=HW29067qVWk&t](https://www.youtube.com/watch?v=HW29067qVWk&t)
