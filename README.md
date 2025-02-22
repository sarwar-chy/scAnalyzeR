#                                                              scAnalyzeR
**scAnalyzeR:** a comprehensive software package with graphical user interface for single-cell RNA sequencing analysis

### Overview
We have developed a scAnalyzeR, a scRNA-seq analysis pipeline with an interactive and user-friendly graphical interface for analyzing and visualizing scRNA-seq data. It accepts scRNA-seq data from various technology platforms, e.g., 10X genomics, Fluidigm or SMART-seq, and different model organisms (human and mouse), and allows flexibility in input file format. It provides functionalities for data preprocessing, quality control, basic summary statistics, dimension reduction, unsupervised clustering, differential gene expression, gene set enrichment analysis, correlation analysis, pseudotime cell trajectory inference and various visualization plots. It also provides default parameters for easy usage and allows a wide range of flexibility and optimization by accepting user-defined options.

# How to run the scAnalyzeR?
There are two different ways to setting up the pipeline in your own machine: <br/>
**Way 1:** using from Docker image (**strongly recommended**)
1.	Download and install [Docker](https://www.docker.com/products/docker-desktop)
2.	Pull the docker image from Docker Hub by running the following command:
  ```
 docker pull gscdocker/scanalyzer:latest
  ```
3.	Run the docker image locally on your computer and access the link: <br/>
  To run the docker image, execute the following command:
  ```
  docker run -d --rm -p 3838:3838 gscdocker/scanalyzer:latest
  ```
  After running the docker image successfully, open the following link on a web browser (e.g., Firefox, Google Chrome) to access the pipeline: 
  ```
  http://localhost:3838/
  ```
  If you are new in Docker and interested to learn more, there are enormous tutorials including the followings: <br/>
  *  [Docker for beginners](https://docker-curriculum.com/) 
  *  [More about docker](https://www.youtube.com/watch?v=6aBsjT5HoGY)
  
**Way 2:** using from source  <br/>
Firstly, you need to download and install following softwares (install R then RStudio): <br/>
Download and install R and RStudio on your machine, <br/>
i.	Download and install R (v-3.6.2 or above): https://cran.r-project.org/ <br/>
ii.	Download and install RStudio: RStudio (v-1.1.456 or above): https://rstudio.com/products/rstudio/download/ <br/>
After installing the R and RStudio on your machine successfully, then, you need to clone this (https://github.com/sarwarchy20/scAnalyzeR/archive/master.zip) repository as well as unzip it. <br/>
Now, please run the following script on RStudio to install the **renv** R package: <br/>
```
install.packages("renv")
```
Next, run the following scripts on RStudio to install all the dependent R packages. Please replace ~ with the location of your scAnalyzeR-master unzipped folder: <br/> 
```
renv::consent(provided=TRUE)
setwd("~/scAnalyzeR-master")
renv::restore() 
```
Finally, run the app using RStudio by running the script below: <br/>
```
shiny::runApp('~/scAnalyzeR-master/')
```
After successfully running the scAnalyzeR, the GUI will be displayed automatically.
<br/>
# Interface with user manual <br/>
Click the link below to download/view the full 47 pages usage manual <br/>
[Usage Manual](https://github.com/sarwarchy20/scAnalyzeR/blob/master/user_manual/User_manual_scAnalyzeR_1_0.pdf)

