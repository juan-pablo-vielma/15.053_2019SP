# 15.053_2019SP

### Install Julia

To get started, you first need to install Julia.

 - Download and install Julia v1.0.3 from [https://julialang.org/downloads/](https://julialang.org/downloads/).

**Windows 7 Users**: as instructed on the downloads page, you will need to
install at least version 3.0 of the [Windows Management Framework](https://docs.microsoft.com/en-us/powershell/wmf/overview).

### Download the materials

Next, you need to download a copy of these materials.

 - If you have `git`
installed, (after `cd`'ing to an appropriate directory) run
```
git clone https://github.com/juan-pablo-vielma/15.053_2019SP.git
```
 - If you don't have `git` installed (i.e., the above command fails), [download this zip file](https://github.com/lanl-ansi/tutorial-grid-science-2019/archive/master.zip). Once downloaded, unzip it to an appropriate location.

### Open Julia

Now open Julia, either by typing `julia` at a terminal, or from where ever you installed it. Once open, you should be faced with the Julia *REPL* that looks like this:

![Julia REPL](figures/repl.png)

### Install Jupyter

Now we need to install [Jupyter](http://jupyter.org/).
In the Julia REPL, run the following commands (this may take a little bit of time):
```julia
import Pkg
ENV["JUPYTER"]=""
Pkg.add("IJulia")
```

### Open a Jupyter notebook

Okay, last step, let's launch a Jupyter notebook! Open a Julia REPL and then run:
```julia
using IJulia
IJulia.notebook(dir="/path/to/15.053_2019SP")
```

Note: we've had some reports that `dir="~"` fails on some NIX machines. Use an
absolute path instead.

If all goes well, a browser window will open that looks like this:

![jupyer_notebook](figures/jupyter.png)

To get started on the content portion of the tutorials, click on the first notebook entitled `Introduction to Julia-JuMP.ipynb`.
