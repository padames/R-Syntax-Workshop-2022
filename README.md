# R-Workshop Intro To R Syntax

Material for intro to R Syntax workshop

Using the Rproj file and Rstudio, open the Rmd file for each module in the series.
Once open, compile it with the button: "Run Document".
This will create a shiny app that is fully contained and interactive.
The code chunks in the tutorial are fully interactive R sessions that keep the state from previous runs using the package `learnr`.
This provides a workshop with zero time spent on setup and leaves the time and attention to focus on R syntax exclusively.

These workshop has been taught twice a year in a two-day format.
Each section builds upon the previous ones. 
The first begins with basic operators, variables, and built-in functions.
Then data types and data structures are introduced: unidimensional homogeneous vectors and heterogeneous lists, two-dimensional homogeneous matrices, multidimensional homogeneous arrays and ultimately the multidimensional heterogeneous data frame.
Next come a modulefor user functions and the basics of flow control and iteration for R programming.
Lastly a module on graphics in base R.

Throughout the modules, there is an emphasis on the features that make R useful for data analysis and visualization.
Base R's syntax is natively vectorized, meaning there is no need to import libraries to write vectorized expressions.
The basic operators use a technique called recycling to process vectors and matrices of incomplete size.
Another set of base R patterns are presented for subsetting and manipulating basic data structures.
The reusability of the patterns is emphasized to minimize cognitive load and to develop familiarity. 

This source code repo is better maintained as CalgaryR by cloning the url in HTPPS format. 
Then use tokens as passwords for git authentication.
The tokens are generated from the CagaryR account on GitHub.