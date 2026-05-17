---
output: html_document
---
# R-Workshop Intro To R Syntax

## Source Code

Using the Rproj file and RStudio, open the Rmd file for each module in the series.
Once open, compile it with the button: "Run Document".
This will create a shiny app that is fully contained and interactive.
The code chunks in the tutorial are fully interactive R sessions that keep the state from previous runs using the package `learnr`.
This provides a workshop with zero time spent on setup and leaves the time and attention to focus on R syntax exclusively.

## History

These workshops have been taught twice a year in a two-day format at the Taylor Family Digital Library of the University of Calgary.
The library hosts a series of workshops during the first week, before each academic semester, usually in January and September.
The Introduction to R Syntax Workshops started in January 2021 as a two-module format and a single session.
Over time the material was further expanded and refined into 7 modules and two 1.5h sessions on separate days.

## Workshop Intent

The online modules can be used as self-guided material and for in-class support, even as a replacement for slides.
Each section builds upon the previous ones. 
The first begins with basic operators, variables, and built-in functions.
Then data types and data structures are introduced: unidimensional homogeneous vectors and heterogeneous lists, two-dimensional homogeneous matrices, multidimensional homogeneous arrays and ultimately the multidimensional heterogeneous data frame.
Next comes a module on user functions, the basics of flow control, and iteration for R programming.
Lastly, a module on graphics in base R.

## Philosophy

Throughout the modules, there is an emphasis on the features that make R useful for data analysis and visualization.
Base R's syntax is natively vectorized, meaning there is no need to import libraries to write vectorized expressions.
The basic operators use a technique called recycling to process vectors and matrices of incomplete size.
Another set of base R patterns is presented for subsetting and manipulating basic data structures.
The reusability of the patterns is emphasized to minimize cognitive load and to develop familiarity. 

## Source Code Maintenance

This source code repo is better maintained as CalgaryR by cloning the URL in HTTPS format. 
Then use tokens as passwords for git authentication.
The tokens are generated from the CagaryR account on GitHub.

## Deployment

You can download/clone this repo and run each part from source directly on your computer as described in the first paragraph above. 
Alternatively you can visit the live tutorials deployed to ShinyApps.io until migrated to the new Posit cloud.

  * https://padames-shiny.shinyapps.io/P1_OperatorsVarsBuiltIns/
  * https://padames-shiny.shinyapps.io/P2_Vectors_in_R/
  * https://padames-shiny.shinyapps.io/P3_Matrices_Arrays/
  * https://padames-shiny.shinyapps.io/P4_Lists/
  * https://padames-shiny.shinyapps.io/P5_DataFrames/
  * https://padames-shiny.shinyapps.io/P6_User_Functions_and_Programming/
  * https://padames-shiny.shinyapps.io/P7_BaseR_Graphics/
  

