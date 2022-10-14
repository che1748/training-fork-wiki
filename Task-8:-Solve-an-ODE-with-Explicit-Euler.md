You should now be able to access the ORC, understand basic Unix, write bash scripts, submit jobs using Slurm, write code in Python and C++, and use Git! To tie this all together, I want you to do a short C++ project, run it on a cluster, and produce a plot with Matplotlib. This will help you put everything you have learned together, and see if there is anything you still don’t understand.  
\
You are going to write a code to solve a linear, first-order differential equation,  
<div align="center">
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{dx}{dt}=-3x" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{dx}{dt}=-3x," title="\frac{dx}{dt}=-3x," /></a> </div> <div align="right"> (1)</div>
<div align = "center">
<a href="https://www.codecogs.com/eqnedit.php?latex=x(0)&space;=&space;1" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x(0)&space;=&space;1" title="x(0) = 1" /></a>
</div>
 
which has the analytical solution,
<div align="center">
<a href="https://www.codecogs.com/eqnedit.php?latex=x(t)=e^{-3t}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x(t)=e^{-3t}" title="x(t)=e^{-3t}" /></a> </div> <div align="right">(2)</div>

The numerical method you will use is called the Explicit Euler method. It is very straightforward. Assume that the derivative on the left-hand side of Eq. 1 is discrete,

<div align="center">
<a href="https://www.codecogs.com/eqnedit.php?latex=\frac{x_{i&plus;1}-x_{i}}{t_{i&plus;1}-t_{i}}=-3x_i" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{x_{i&plus;1}-x_{i}}{t_{i&plus;1}-t_{i}}=-3x_i" title="\frac{x_{i+1}-x_{i}}{t_{i+1}-t_{i}}=-3x_i" /></a> </div> <div align="right">(3)</div>
If this is so, then if we know <i>x<sub>0</sub></i> (which we do), then we can solve for <i>x<sub>1</sub></i> (and all of the others), assuming we pick a discrete time step <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;\large&space;\Delta&space;t=t_{i&plus;1}-t_i" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;\large&space;\Delta&space;t=t_{i&plus;1}-t_i" title="\large \Delta t=t_{i+1}-t_i" /></a> ,      
  
<div align="center">
<a href="https://www.codecogs.com/eqnedit.php?latex=x_{i&plus;1}=(1-3\Delta&space;t)x_i" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_{i&plus;1}=(1-3\Delta&space;t)x_i" title="x_{i+1}=(1-3\Delta t)x_i" /></a> </div> <div align="right">(4)</div>

With that background in place, do the following project.
1.	Create a directory called “training\” in your ORC home directory.
2.	Write a C++ code to solve the differential equation above. Put the code in a new directory: “training\src\”.
    1.	The code should read in a text file (params.dat) where the parameters of the time integration (time step, number of steps) are read from file.
    2.	The code should write an output file (output.dat) with  and  in separate columns.
3.	Create a Git repository to track your changes as you write the C++ code. Make regular commits and push them to GitHub as you work.
4.	After you are sure the code works, compile the code and place the executable in a directory called “training\bin\”
5.	Write a Slurm script to run the executable as a batch job. Solve the equation for <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;t&space;\in&space;[0,9]" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;t&space;\in&space;[0,9]" title="t \in [0,9]" /></a> for several different values of the time step parameter, <a href="https://www.codecogs.com/eqnedit.php?latex=\inline&space;\Delta&space;t=10^{-z},&space;z\in&space;\{-6,&space;-5,...,0\}." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\inline&space;\Delta&space;t=10^{-z},&space;z\in&space;\{-6,&space;-5,...,0\}" title="\Delta t=10^{-z}, z\in \{-6, -5,...,0\}" /></a> . Store the resulting input and output files in “training\data\”.
6.	Write a Python script to plot the seven data sets. Calculate the error between the numerical solution you have generated and the analytical solution. Save the script and the plot in “training\plt\”.
