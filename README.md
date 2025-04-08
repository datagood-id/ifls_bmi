# IFLS BMI MAIHDA


Intersectionality is the study of how multiple sociodemographic
identities intersect and interact to create unique experiences of
discrimination and privilege that result in inequalities in individual
outcomes. Intersectionality makes visible the experiences of hidden
marginalized populations.

From quantitative data analysis perspective, a natural approach to study
intersectional sociodemographic inequalities in individual outcomes is
to estimate linear regressions of the individual outcome of interest on
their sociodemographic characteristics and their interactions. As we
introduce further sociodemographic characteristics, it proves
statistically and interpretationally challenging to also introduce more
and more interactions, many imprecisely estimated parameters and risk of
type I errors. As a result, interactions effects and therefore
intersectionality in individual outcomes is typically under explored,
running the risk of misunderstanding or even missing important
marginalized populations.

Intersectional multilevel analysis of individual heterogeneity and
discriminatory accuracy (MAIHDA) aims to address these challenges, a
systematic approach to explore many and complex interaction effects.
Intersectional MAIHDA involves an innovative application of two-level
linear regression of individual outcomes where individuals are modeled
as clustered in 10s or even 100s of strata defined by the combinations
of their sociodemographics characteristics, interest lies in studying
how mean outcomes vary across strata. The approach was proposed by Evans
et al. (2018) and has been further developed by Evans, Merlo, Leckie,
and others.

## Data

Data were drawn from wave 5 of Indonesia family life survey (IFLS).
Sample consists of 29934 respondents after being cleaned. The outcome is
toothache experience. The sociodemographic characteristics are: age,
sex, marital, urban, education, job.

|           |                | Mean  | Std. Dev. |
|-----------|----------------|-------|-----------|
| BMI       |                | 23.3  | 4.5       |
|           |                | N     | Pct.      |
| Age       | \<40           | 19441 | 64.9      |
|           | (more than) 40 | 10493 | 35.1      |
| Sex       | Female         | 15723 | 52.5      |
|           | Male           | 14211 | 47.5      |
| Marital   | Married        | 21824 | 72.9      |
|           | Not Married    | 8110  | 27.1      |
| Urban     | Rural          | 11987 | 40.0      |
|           | Urban          | 17947 | 60.0      |
| Education | Elementary     | 9256  | 30.9      |
|           | High_school    | 16381 | 54.7      |
|           | University     | 4297  | 14.4      |
| Job       | Employed       | 2669  | 8.9       |
|           | Unemployed     | 27265 | 91.1      |

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-7-1.png)

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-8-1.png)

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-9-1.png)

## Strata

The strata is defined by combination of age, sex, marital, urban,
education and job, resulting in 94 theoretical strata. The individual
BMI experience are now viewed as clustered in strata, the variables
defining the strata are elevated from individual to stratum level
characteristics. Intersectional strata identities and even the
characteristics defining them are no longer modeled as personal
characteristics (risking “blaming the victim”), but are now modeled as
social contexts viewed as encompassing the broader shared social
experiences of individuals in each strata.

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-11-1.png)

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-12-1.png)

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-13-1.png)

## Model fit

Model null measures the extent to which individual outcome heterogeneity
is explained by sociodemographic intersections vs other factors.
Optimally predicts the mean outcome for each stratum.

Model full decomposes sociodemographic mean outcomes into additive and
non-additive effects and measures relative importance of interactions.
Optimally predicts the strata interaction effects with built in control
for type I errors of inference.

Model is fitted by maximum likelihood estimation (MLE).

<table style="border-collapse:collapse; border:none;">
<tr>
<th style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm;  text-align:left; ">&nbsp;</th>
<th colspan="2" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">Mental health</th>
<th colspan="2" style="border-top: double; text-align:center; font-style:normal; font-weight:bold; padding:0.2cm; ">Mental health</th>
</tr>
<tr>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  text-align:left; ">Predictors</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">Estimates</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">CI (95%)</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">Estimates</td>
<td style=" text-align:center; border-bottom:1px solid; font-style:italic; font-weight:normal;  ">CI (95%)</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Intercept</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">23.13</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">22.77&nbsp;&ndash;&nbsp;23.52</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">20.14</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">19.63&nbsp;&ndash;&nbsp;20.67</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Age: >40</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.32</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.94&nbsp;&ndash;&nbsp;1.71</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Female</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.81</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.45&nbsp;&ndash;&nbsp;2.18</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Married</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.61</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.23&nbsp;&ndash;&nbsp;1.99</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Urban</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.65</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.28&nbsp;&ndash;&nbsp;1.03</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Education: High school</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.23</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.21&nbsp;&ndash;&nbsp;0.67</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Education: University</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">1.14</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">0.65&nbsp;&ndash;&nbsp;1.61</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; ">Job: Employed</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  "></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.37</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:center;  ">&#45;0.75&nbsp;&ndash;&nbsp;0.03</td>
</tr>
<tr>
<td colspan="5" style="font-weight:bold; text-align:left; padding-top:.8em;">Random Effects</td>
</tr>
&#10;<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">&sigma;<sup>2</sup></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">17.42</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">17.52</td>
</tr>
&#10;<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">&tau;<sub>00</sub></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">2.78 <sub>strata</sub></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">0.55 <sub>strata</sub></td>
&#10;<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">ICC</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">0.14</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">0.03</td>
&#10;<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">N</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">94 <sub>strata</sub></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">94 <sub>strata</sub></td>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm; border-top:1px solid;">Observations</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="2">29853</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left; border-top:1px solid;" colspan="2">29853</td>
</tr>
<tr>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; text-align:left; padding-top:0.1cm; padding-bottom:0.1cm;">Marginal R<sup>2</sup> / Conditional R<sup>2</sup></td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">0.000 / 0.141</td>
<td style=" padding:0.2cm; text-align:left; vertical-align:top; padding-top:0.1cm; padding-bottom:0.1cm; text-align:left;" colspan="2">0.104 / 0.141</td>
</tr>
&#10;</table>

<div id="riksdzzoys" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">

| Measure | Value  |
|---------|--------|
| VPC     | 13.62% |
| VPC adj | 3.04%  |
| PCV     | 80.15% |

</div>

Variance partition coefficient (VPC) measures the proportion of
individual heterogeneity which lies between strata. The variance in
individual BMI is 13.62% between strata means, and the rest 86.38% is
attributable to unmodeled factors that vary across individuals. There is
less variation between strata means, than within strata. Therefore, the
strata has very low discriminatory accuracy. The strata tells us very
little about individual toothache.

The VPC adjusted is just 3.04% which is too little for interaction
effects to explain the variation.

Percentage change in variance (PCV) measures the degree to which we
explain the overall sociodemographic variation by just the main effects.
The variation of sociodemographic main effects is 80.15%, and thus only
19.85% of the variation explained by sociodemographic interaction
effects.

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-19-1.png)

![](ifls_bmi_files/figure-commonmark/unnamed-chunk-21-1.png)

The caterpillar plot gives a sense of not just the variablity in
predicted strata means, but their individual imprecision, and their lack
of statistical separation.
