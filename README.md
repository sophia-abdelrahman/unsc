# unsc
## intro
Investigating effect of non-permanent rotational membership on the United Nations Security Council ion inflow of Foreign Direct Investment (Balance of Payment, US dollars) for a final econometrics group project.

Multiple regression models with fixed effects were used for this analysis. Log-linear transformations were used on the FDI Y-variable in order to be able to interpret coefficients as percentage point changes rather than dollar value changes.

| Variable                          | Observations | Mean     | Std. Err | Min      | Max      |
|-----------------------------------|--------------|----------|----------|----------|----------|
| FDI net inflow (BoP, Current US$) | 4498         | 5.370463 | 18.99977 | -82.8921 | 773.928  |
| ln(FDIBoP)                        | 4361         | 19.77946 | 2.824037 | 2.302585 | 27.32179 |
| Country Name                      | 193          | -        | -        | -        | -        |
| Year                              | 4825         | 2005     | 7.21185  | 1993     | 2017     |
*Table 1: Some summary statistics: panel data was compiled from World Bank and UNSC sources and cleaned*

## empirical models and results
One important assumption made was that any variables affecting FDI that are also correlated with UNSC membership are “controlled” for by country and year fixed effects incorporated into models, thereby handling omitted variable bias.

Below are some multiple regression models designed for the analysis, and their results:

  1. **Immediate effects model**
  * This model consists of 6 dummy variables:
      * `onUNSC` indicates whether a country was on the UNSC relative to the year
      * `postUNSC1` indicates if the country is in the first year following membership
      * `postUNSC2` indicating the same as postUNSC1 but for the second year following membership
      * ... and so on until `postUNSC5`
      
  ### Yit = 𝛽0 + 𝛽1onUNSC + 𝛽2postUNSC1 + 𝛽3postUNSC2 + 𝛽4postUNSC3 + 𝛽5postUNSC4 + 𝛽6postUNSC5 + 𝛄i + αt + ɛit 
