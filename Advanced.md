# 15.053_2019SP

This page includes some _advanced_ alternative install and use instructions for the [Julia](https://julialang.org) and [JuMP](https://github.com/JuliaOpt/JuMP.jl) materials for 15.053. You can safely ingnore this page and we recommend you only read it if you have experience with 
command line tools. 

#### Download the materials (Advanced version)

If you know how to use `git` from the command prompt or terminal, you can also download a copy of these materials by running the following command from a terminal (after `cd`'ing to a folder of your choice):
```
git clone https://github.com/juan-pablo-vielma/15.053_2019SP.git
```

### Open Julia (Advanced version)

You can also open Julia by running `julia` at a terminal, but you may need to add the Julia executable to your `Path` environment. 

### Install Jupyter (Advanced version)

The default install instructions installs self-contained versions of `python` and `jupyter` to be used by `IJulia`. If you would like to use your own already installed versions please see the instructions in the [IJulia page](https://github.com/JuliaLang/IJulia.jl).

### Open a Jupyter notebook (Advanced version)

To avoid having to navigate to the `15.053_2019SP` folder after opening Jypyter you can instead run the following code (where `"/path/to/15.053_2019SP"` is the complete path to the location in which you uncompressed the `15.053_2019SP` folder)
```julia
using IJulia
IJulia.notebook(dir="/path/to/15.053_2019SP")
```

### Using the Default Course Packages (Advanced version)

You can also activate the course packages from the Julia REPL or a notebook that is not inside  the `15.053_2019SP` folder by running the following code (where `"/path/to/15.053_2019SP"` is the complete path to the location in which you uncompressed the `15.053_2019SP` folder):
```julia
import Pkg
Pkg.activate("/path/to/15.053_2019SP")
Pkg.instantiate()
```

### Updating Course Files and Packages (Advanced version)
If you know how to use `git` from the command prompt or terminal, you can also get the latest files by running the following command from a terminal within the `15.053_2019SP` folder (i.e. after `cd`'ing to the `15.053_2019SP` folder)
```
git pull
```
