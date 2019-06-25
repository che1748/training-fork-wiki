You should now be able to access the FSL, understand basic Unix, write bash scripts, submit jobs using Slurm, write code in Python and C++, and use Git! To tie this all together, I want you to do a short C++ project, run it on a cluster, and produce a plot with Matplotlib. This will help you put everything you have learned together, and see if there is anything you still don’t understand.  
You are going to write a code to solve a linear, first-order differential equation,  
$$\frac{dx}{dt} = -3x$$ (1)
 
which has the analytical solution,
	 .	(2)

The numerical method you will use is called the Explicit Euler method. It is very straightforward. Assume that the derivative on the left-hand side of Eq. 1 is discrete,
	 . 	(3)
If this is so, then if we know  (which we do), then we can solve for  (and all of the others), assuming we pick a discrete time step  ,
	 . 	(4)

With that background in place, do the following project.
1.	Create a directory called “training\” in your FSL home directory.
2.	Write a C++ code to solve the differential equation above. Put the code in a new directory: “training\src\”.
a)	The code should read in a text file (params.dat) where the parameters of the time integration (time step, number of steps) are read from file.
b)	The code should write an output file (output.dat) with  and  in separate columns.
3.	Create a Git repository to track your changes as you write the C++ code. Make regular commits and push them to Bitbucket as you work.
4.	After you are sure the code works, compile the code and place the executable in a directory called “training\bin\”
5.	Write a Slurm script to run the executable as a batch job. Solve the equation for  for several different values of the time step parameter,  . Store the resulting input and output files in “training\data\”.
6.	Write a Python script to plot the seven data sets. Calculate the error between the numerical solution you have generated and the analytical solution. Save the script and the plot in “training\plt\”.
