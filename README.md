# Doing MAIHDA with Tidyverse & brms

This repository contains my edited personal note of translation of Evans's MAIHDA code tutorial with `brms` to `tidyverse` syntax. The original code tutorial is supplementary material to the [2024 MAIHDA methodological paper by Evans et al.](https://pmc.ncbi.nlm.nih.gov/articles/PMC11059336/). It is intended to be read alongside the original paper. For reference, [the original tutorial code by Evans et al.](https://osf.io/dtvc3/files/xvtu6) is also available for comparison.

# Contents

- MAIHDA-Code-Tidyverse.qmd: The main Quarto document containing the R code, narrative, and methodological notes.
- MAIHDA-Code-Tidyverse.html: The rendered output. View this file to see the code, tables, and plots without needing to run R.
- TutorialData.dta: The dataset that Evans et al. simulated for the MAIHDA tutorial.
- The cached `brms` models objects: model1A.rds, model1B.rds, model2A.rds, model2B.rds. If these are present in your quarto working directory, the Quarto file will automatically load them instead of re-sampling the models. Feel free to fit your own models on different seed to compare the result, but note that these models are quite heavy, and take some time to fit.

# Running The Code

To run this code locally, you will need R, RStudio, and the cmdstanr backend installed. By default, `brms` use `rstan` as backend, you can run it with `rstan` as backend by deleting this line on every `brms` fit chunk: `backend = "cmdstanr",`. Note that `cmdstanr` requires the CmdStan C++ toolchain. Please follow the official installation guide [here](https://mc-stan.org/cmdstanr/).

You can install all the required R packages by running the following code:

```
install.packages(c("haven", "tidyverse", "bayesplot", "brms", "tidybayes", "labelled", "flextable", "patchwork", "rstan", "cmdstanr"))
```

# Author

Rully Kemal Aziz - MPH Biostatistics | Universitas Indonesia
