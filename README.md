# GA <img src="man/figures/logo.png" align="right" width="100px " alt=""/>

[![CRAN\_Status\_Badge](http://www.r-pkg.org/badges/version/GA)](https://cran.r-project.org/package=GA)
[![CRAN\_MonthlyDownloads](http://cranlogs.r-pkg.org/badges/GA)](https://cran.r-project.org/package=GA)

An [R](https://www.r-project.org/) package for stochastic optimisation using **Genetic Algorithms**.

The **GA** package provides a flexible general-purpose set of tools for implementing genetic algorithms search in both the continuous and
discrete case, whether constrained or not. Users can easily define their own objective function depending on the problem at hand. Several genetic operators are available and can be combined to explore the best settings for the current task. Furthermore, users can define new genetic operators and easily evaluate their performances. Local search using general-purpose optimisation algorithms can be applied stochastically to exploit interesting regions. GAs can be run sequentially or in parallel, using an explicit master-slave parallelisation or a coarse-grain islands approach.

## Installation

You can install the released version of **GA** from CRAN:

#Preliminary edits;
ga & gaisl amended to allow the fitness function to return a named list length 2, one element named "fitness" and the second element named "realfitness". A summary for each iteration, and each iteration for each island (if using gaisl) will be returned in the ga object once the function has finished. Further amendments will be made to make this more robust but for now I just needed a working solution that would return me my underlying fitness function (i.e RMSE) if I am artificially penalising my fitness function to reduce features in the model. For now, I have changed the function names to ga_mod and gaisl_mod to avoid conflicts with existing ga package. 


```{r}
install.packages("GA")
```

or the development version from GitHub:

```{r}
# install.packages("devtools")
devtools::install_github("luca-scr/GA", build_vignettes = TRUE)
```

## Usage

Usage of the main functions and several examples are included in the
papers shown in the references section below.

For an intro see the vignette **A quick tour of GA**, which is available as

```{r}
vignette("GA")
```

The vignette is also available in the *Get Started* section on the
GitHub web page of the package at http://luca-scr.github.io/GA/.

## References

Scrucca, L. (2013) GA: A Package for Genetic Algorithms in R. **Journal of Statistical Software**, 53(4), 1-37. https://www.jstatsoft.org/article/view/v053i0

Scrucca, L. (2017) On some extensions to GA package: hybrid
optimisation, parallelisation and islands evolution. **The R Journal**, 9(1), 187–206. https://journal.r-project.org/archive/2017/RJ-2017-008
