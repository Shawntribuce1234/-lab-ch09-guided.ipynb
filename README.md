# A/B Testing — Designing the Data-Generating Process

## Objective
In this lab, I explored how randomized experiments, statistical testing, and sample size affect our ability to measure causal effects and make decisions using data.

## Methodology
- Loaded the LaLonde NSW job training dataset with 445 participants, including 185 trainees and 260 control participants.
- Calculated the Average Treatment Effect (ATE) by comparing earnings between the treatment and control groups.
- Simulated an observational comparison group to understand how selection bias can lead to misleading conclusions.
- Ran a permutation test using 9,999 shuffles to determine whether the observed difference was statistically significant.
- Used bootstrap resampling with a 95% BCa confidence interval to measure uncertainty around the estimated effect.
- Performed power analysis to understand how sample size and effect size influence statistical power.
- Analyzed the Cookie Cats A/B test with 90,189 players to compare Day-1 retention between gates at levels 30 and 40.
- Created an `n_needed()` function to calculate the sample size required for 80% statistical power.
- Simulated 100 e-commerce A/B tests to compare estimated effects with the true effect.

## Key Findings

### LaLonde Job Training Experiment
The experimental results showed that participants in the job training program earned an average of **$1,794.34 more** than the control group.

The 95% confidence interval ranged from **$575.18 to $3,262.37**, suggesting a positive effect on earnings.

However, the simulated observational comparison produced a negative treatment effect of approximately **-$14,785**, showing how selection bias can completely change the conclusion of a study.

### Cookie Cats A/B Test
The Cookie Cats experiment showed that players assigned to gate 30 had a **0.59 percentage-point higher Day-1 retention rate** than players assigned to gate 40.

However, the 95% confidence interval ranged from **-0.07 to 1.23 percentage points**, meaning the difference was not statistically significant at the 5% level.

Based on these findings, I would recommend keeping the gate at level 30 until additional testing provides stronger evidence.

### Power Analysis and Simulations
I found that larger sample sizes improve our ability to detect smaller effects.

In my e-commerce simulation, the true conversion improvement was 2 percentage points, while the average estimated effect across 100 experiments was **1.99 percentage points**.

Additionally, **77% of experiments rejected the null hypothesis**, which was close to the planned 80% statistical power.

When I reduced the true effect to 1 percentage point, the required sample size increased substantially.

## Conclusion
This lab helped me understand that finding a difference between two groups does not automatically mean one caused the other. Random assignment helps reduce selection bias, while permutation tests, confidence intervals, and power analysis help determine whether the results are meaningful.

My biggest takeaway is that even small differences can matter, but we need enough data and the right experimental design before making decisions.
