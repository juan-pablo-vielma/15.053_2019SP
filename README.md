# 15.053_2019SP

This page includes the install and use instructions for the [Julia](https://julialang.org) and [JuMP](https://github.com/JuliaOpt/JuMP.jl) materials for 15.053. Some sections include an alternative _Advanced Version_ that you can safely ignore. 

### Install Julia

To get started, you first need to install Julia.

 - Download and install Julia v1.0.3 from [https://julialang.org/downloads/](https://julialang.org/downloads/).

**Windows 7 Users**: as instructed on the downloads page, you will need to
install at least version 3.0 of the [Windows Management Framework](https://docs.microsoft.com/en-us/powershell/wmf/overview).

### Download the materials

To get the course materials [download this zip file](https://github.com/juan-pablo-vielma/15.053_2019SP/archive/master.zip) and uncompress it to a folder of your choice. This will create a sub-folder `15.053_2019SP` with all the materials. 

### Open Julia

Now open Julia by clicking on the Julia icon you installed. Once open, you should be faced with the Julia *REPL* (Julia's interactive command prompt) that looks like this:

![Julia REPL](figures/repl.png)

### Install Jupyter

Now we need to install [Jupyter](http://jupyter.org/).
In the Julia REPL, run the following commands (this may take a little bit of time):
```julia
import Pkg
ENV["JUPYTER"]=""
Pkg.add("Conda")
Pkg.add("IJulia")
import Conda
Conda.add("jupyter")
```

### Open a Jupyter notebook

Okay, last step, let's launch a Jupyter notebook! Open a Julia REPL and then run:
```julia
using IJulia
IJulia.notebook()
```

If all goes well, a browser window will open that looks like this:

![jupyer_notebook](figures/jupyter_root.png)

You can then navigate to the location of where you uncompressed the `15.053_2019SP` folder and you should see something like this: 
![jupyer_notebook](figures/jupyter.png)

To get started on the tutorials, click on the first notebook entitled `Introduction to Julia-JuMP.ipynb`.

### Using the Default Course Packages

The files `Project.toml` and `Manifest.toml` contain the information about versions of the default course packages that we know work well. These packages can be _activated_ by running the following code in any Jupyter notebook in the `15.053_2019SP` folder:
```julia
import Pkg
Pkg.activate(@__DIR__)
Pkg.instantiate()
```
You will see this as the first code cell in all example notebooks and you should add it to all the notebooks you create.


### Updating Course Files and Packages
To get the latest version of this repsitory (files and safe versions of packages) simply [re-download this zip file](https://github.com/juan-pablo-vielma/15.053_2019SP/archive/master.zip), which always contains the latest versions. 


