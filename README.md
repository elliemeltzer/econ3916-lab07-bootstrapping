# Estimation & Bootstrapping — Quantifying Uncertainty Without a Formula

## Objective

I compared formula-based and simulation-based methods for measuring uncertainty in estimates from the UCI Adult Census Income data.

## Methodology

- I loaded data for 32,561 respondents.
- I distinguished the standard deviation of individual observations from the standard error of an estimated mean.
- I checked how standard error changes with the square root of sample size.
- I constructed a parametric confidence interval for mean age.
- I compared the Central Limit Theorem’s convergence for age and positive capital gains.
- I manually bootstrapped medians and means.
- I compared percentile and BCa bootstrap intervals.
- I estimated the difference in mean weekly hours between men and women.
- I ran a coverage simulation on lognormal data.
- I created and verified a reusable bootstrap-interval function.

## Key Findings

The standard deviation of age was 13.640 years, while the standard error for samples of 100 was approximately 1.36 years. Increasing the sample size by a factor of four approximately halved the standard error.

The bootstrap median age was 37 in every resample, producing a bootstrap standard error of 0.0000. This happened because 858 observations were tied at age 37, pinning the sample median rather than indicating absolute certainty about the population.

Among 2,712 respondents with positive capital gains, the mean was $12,939 and the median was $7,298. The manual bootstrap produced a standard error of $424 for the mean.

For mean lognormal outcomes at a sample size of 50, the parametric interval covered 92.5% of experiments and the percentile bootstrap covered 91.5%. Their one-point difference was within the simulation’s sampling error. For the median, the mean-centered parametric interval covered only 66.8%, while the bootstrap interval covered 93.2%.

Men reported an average of 6.02 more weekly hours than women in this 1994 sample. The 95% BCa interval ranged from 5.73 to 6.28 hours, but this observational comparison does not establish causation.
