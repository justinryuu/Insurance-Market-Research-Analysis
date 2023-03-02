# New York Workers’ Compensation Market Analysis
## Justin Lyu for Insurtech Advisors LLC

## Abstract
The analysis of Disability Benefits in New York state revealed a significant “Benefit Gap” caused by themaximum weekly benefit limit of $170 when the weekly benefit calculated according to the NY Workers’ Compensation Board suggested a level of compensation significantly higher for both genders.

The formula used to calculate Lost Wage Benefits involves a “% of disability based on medical evidence”term that is very difficult to objectively valuate. Rather than simulating the disability classification process,this report calculated different payouts depending on the level of disability of a hypothetical claimant.

Similar to Disability Benefits, Lost Wage Benefits have weekly maximums but are instead adjusted yearly. Average Lost Wage Benefits in New York did not demonstrate a “Benefit Gap” as in the case of Disability Benefits due to these maximums, however the difference between the average lost wage benefit in the case of Total disability (intended to illustrate the upper extreme of payouts) and the government-imposed maximum has been growing over recent years. This means that insurance providers might have to provide significantly higher payouts in rare cases before the weekly maximum prevents them from paying any more. This suggests that less common but highly expensive claims now carry relatively more risk.

Demographic analyses were conducted on the number of claims filed by Age Group, Gender, and District. Workers in age ranges 35-49 and 50-65 filed the most claims, Male workers filed comparatively more claims than Female workers, and the most claims were filed in the NYC district. It is important to consider the composition of the labor force in interpreting these results; there is a possibility that these age ranges, Male workers, and workers located in NYC comprise the largest proportion of the labor force. It is possible that there are simply more claims filed under these characteristics as a result.

A multiple linear regression analysis was used in order to formally measure the extent to which different claim characteristics had an effect on the average payout. Payout was defined as the average weekly earnings of a claimant divided by 2, which is the Workers’ Compensation Board’s calculation for weekly disability benefits. Through an examination of the Beta coefficients of each characteristic several observations were made:

1. Female claimants had an average payout that was $111 lower than Male claimants.
2. Age had a slight positive effect on increasing the average payout.
3. On average, claims filed in Binghamton and Rochester resulted in payouts $33 and $36 lower than the
average payout.
4. On average, claims filed in NYC and Hauppauge resulted in payouts $96 and $138 higher than the
average payout. This is likely due to the relatively higher household incomes enjoyed in these districts
compared to others.

## Context
This report is a summary analysis on the state of New York’s Workers’ Compensation claims from January 2017 to March 2022. The objective of this report is to identify potentially useful trends in Disability Benefit and Lost Wage Benefit claims in order to aid Insurtech Advisors LLC’s examination of New York’s Workers’ Compensation insurance market.

## Introduction of Data
The dataset used in this analysis was retrieved from New York’s open source database Open NY, and is titled [Assembled Workers’ Compensation Claims: Beginning 2000](https://data.ny.gov/Government-Finance/Assembled-Workers-Compensation-Claims-Beginning-20/jshw-gkgu/data). This dataset contains information on 4,364,233 claims from the year 2000 to present, and 54 variables that describe the different characteristics of each claim (such as date of filing, weekly wage of claimant, etc.)
For the sake of recency, this report will only consider claims from the last five years (January 1, 2017 and
beyond), which amounts to 1,326,412 unique claims. The analysis will be conducted on a random sample of
10,000 of these claims. Any incorrect or broken observations were removed.

## Disability Benefits and the Benefit Gap
[According to the NY Workers’ Compensation Board](https://www.wcb.ny.gov/content/main/DisabilityBenefits/what-are-disability-benefits.jsp), the Disability Benefit “provides weekly cash benefits to replace, in part, wages lost due to injuries or illnesses that do not arise out of or in the course of employment”. Disability Benefits are calculated to be 50 percent of the claimant’s average weekly wage for the last eight weeks worked, with a maximum benefit of $170 per week.
The wage used to calculate total disability benefit rates for most claimants is defined as 1/52 of the Injured Worker’s average annual earnings, based on the prior year’s payroll data. Disability Benefits are typically paid out by a private insurer, either from individual or company insurance.
Below are the histograms of the calculated disability benefits for male and female claimants according to the formula used by the NY Workers’ Compensation board, which is calculated as half the weekly wage of the claimant.

<img src="images/Figure_1.png" width="80%" height="80%">


