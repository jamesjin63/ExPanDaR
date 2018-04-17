ExPanDaR: Exploring Panel Data with R
================
Joachim Gassen
2018-04-17

[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](http://www.repostatus.org/badges/latest/wip.svg)](http://www.repostatus.org/#wip) [![Travis-CI Build Status](https://travis-ci.org/joachim-gassen/ExPanDaR.svg?branch=master)](https://travis-ci.org/joachim-gassen/ExPanDaR)

You are visiting the github repository of the ExPanDaR (Explore Panel Data with R) package. I develop ExPanDaR to provide the code base for the ExPanD web app. ExPanD is a shiny based app supporting interactive exploratory data analysis.

I designed ExPanD for two purposes:

-   Enable users to assess the robustness of empirical evidence without providing them with access to the underlying data.
-   Provide a toolbox for researchers to explore panel data on the fly.

While I hope that ExPanD might be particularly helpful in the review, publication and replication process I also think that it is convenient for typical exploratory data analysis workflows. In addition, it has already proven to be helpful in the classroom.

This is what ExPanD looks like:

<img src="vignettes/figures/ExPanD_simple_03.png" width="90%" style="display: block; margin: auto;" />

If you are interested to see what ExPanD has to offer without diving into R, click [here](https://jgassen.shinyapps.io/expand_wb/) to explore an instance of ExPanD that hosts World Bank data or click [here](https://jgassen.shinyapps.io/expand_r3/) for a financial accounting and stock returns dataset of U.S. firms.

If you want to analyze your own panel data instead, you can also access a variant of ExPanD app [here](https://jgassen.shinyapps.io/expand/) that allows user-side data uploads. No worries: Your data won't be stored on the server and will get erased from memory as soon as you close the web connection.

Finally, if you are in for the full treat and want to test ExPanD from within R, run the following in your R session to start exploring World Bank data.

``` r
if (!require("devtools")) {
  install.packages("devtools")
}
devtools::install_github("joachim-gassen/ExPanDaR")
library(ExPanDaR)

ExPanD(df = worldbank,  
       df_def = worldbank_data_def, 
       var_def = worldbank_var_def,
       df_name = "World Bank Data",
       config_list = ExPanD_config_worldbank)
```

For further information, please refer to the articles and function call references of the package documentation, available [here](https://joachim-gassen.github.io/ExPanDaR).

Enjoy!
