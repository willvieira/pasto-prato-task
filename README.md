# Do Pasto ao Prato Exercise

Task for the Researcher/Data Scientist position at UCLouvain.

## Installation

First download this project to your local machine. Linux and macOS users can simply clone this project by running the following code on terminal:

```bash
git clone https://github.com/willvieira/pasto-prato-task.git
```

Windows users need a Git installation or can manually download this project as a zip file (Green `Code` button on the top right page).

Once this project is downloaded, open `R` in this project environment and run the following code to restore all necessary R packages to reproduce the analysis:

```R
# install `renv` package if necessary
if (!require(renv)) install.packages('renv')
# restore R package dependencies
renv::restore()
```

[Quarto](https://quarto.org/) must also be installed in order to reproduce the report.

## Usage

To compile the report, run the following on terminal:

```bash
quarto render Report.qmd
```

If you only need to reproduce the figure or don't want to install Quarto, you can extract the R code from the Quarto report by using the `purl` R function:

```R
# extract R code in generate a R script
knitr::purl('Report.qmd')
```

This will produce a `Report.R` Rscript script that can be run manually.
