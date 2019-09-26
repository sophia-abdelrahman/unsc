# unsc
For a final econometrics project, my groupmates and I used Stata to investigate whether being a non-permanent rotational member on the United Nations Security Council has any effect on its inflow of Foreign Direct Investment (Balance of Payment, US dollars).

Multiple regression models with fixed effects were used for this analysis. Log-linear transformations were used on the FDI Y-variable in order to be able to interpret coefficients as percentage point changes rather than dollar value changes.

### some summary statistics
| Variable                          | Observations | Mean     | Std. Err | Min      | Max      |
|-----------------------------------|--------------|----------|----------|----------|----------|
| FDI net inflow (BoP, Current US$) |              |          |          |          |          |
| ln(FDIBoP)                        | 4361         | 19.77946 | 2.824037 | 2.302585 | 27.32179 |
| Country Name                      | 193          | -        | -        | -        | -        |
| Year                              | 4825         | 2005     | 7.21185  | 1993     | 2017     |
