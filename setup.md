# RAdelaide25 Setup Instructions

For this session we'll need both `R` and `RStudio` installed and the 
instructions for this are provided below.
People on managed devices may need to work with their IT Department, whilst for 
those on self-managed devices, the process should hopefully be easy to wrangle.

There's no strict requirement to use the latest version of `R` although the 
absolute minimum required version will be `R` 4.2.1.
The latest release is `R` 4.5.1 and this is the version the course has been 
tested on.
Earlier versions are still expected to work, as long as they are above the 
minimum version (i.e. R 4.2.1, R 4.3.x or R 4.4.x).

If you're having trouble with installation, we will be available from 8:30 on Tuesday 8th to help you.

## Self-Managed Devices

- To install `R` please head to https://cran.r-project.org and install the version suitable for your operating system.
This will be the latest release (v4.5.1)
- After installing `R`, please head to https://posit.co/downloads/ and install the free version of RStudio Desktop
- Open `R` (not RStudio) and paste the following lines followed by \<Enter\>:

``` r
install.packages(
  c(
    "tidyverse", "ggrepel", "ggpmisc", "corrplot", "pheatmap", "reactable", 
    "htmltools", "palmerpenguins", "lme4", "lmerTest", "rmarkdown"
  )
)
```

That should be all you need to do to get started

## Managed Devices

If you have a laptop managed by your institution's IT department, please check 
the software centre they manage for the packages `R` and `RStudio`.
If these are not available, please contact your IT department to have them 
installed.
We have contingency plans for those who have difficulties with installation so 
please let us know if you have problems and we'll get you setup using a Posit 
cloud account.

Once you have `R` installed, please paste the same code as above, followed by 
the \<Enter\> key.
Again, do contact us if there are any problems with this code being executed.

``` r
install.packages(
  c(
    "tidyverse", "ggrepel", "ggpmisc", "corrplot", "pheatmap", "reactable", 
    "htmltools", "palmerpenguins", "lme4", "lmerTest", "rmarkdown"
  )
)
```
