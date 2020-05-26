Predicting attitudes towards racist college professors
================
Maria Benavides
2020-05-25

## Introduction

Using data from the General Social Survey (GSS) – which provides
information about what Americans think and feel about issues of national
spending priorities, crime and punishment, intergroup relations, and
confidence in institutions – we will analyze the factors that determine
whether or not an individual believes a racist person should be allowed
to teach.

### First approach: considering socio-demographic variables

**Table 1** shows whether age, gender, level of education and political
party identification have incidence in a person’s attitude towards a
racist professor teaching in a college or university.

<table>

<caption>

Table 1: predictors of attitudes towards racist professors

</caption>

<thead>

<tr>

<th style="text-align:left;">

Predictor

</th>

<th style="text-align:right;">

B

</th>

<th style="text-align:right;">

SE

</th>

<th style="text-align:right;">

t

</th>

<th style="text-align:right;">

p

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

(Intercept)

</td>

<td style="text-align:right;">

\-0.128

</td>

<td style="text-align:right;">

0.203

</td>

<td style="text-align:right;">

\-0.629

</td>

<td style="text-align:right;">

0.529

</td>

</tr>

<tr>

<td style="text-align:left;">

age

</td>

<td style="text-align:right;">

\-0.004

</td>

<td style="text-align:right;">

0.003

</td>

<td style="text-align:right;">

\-1.376

</td>

<td style="text-align:right;">

0.169

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeHS

</td>

<td style="text-align:right;">

\-0.053

</td>

<td style="text-align:right;">

0.137

</td>

<td style="text-align:right;">

\-0.387

</td>

<td style="text-align:right;">

0.699

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeJunior Coll

</td>

<td style="text-align:right;">

0.170

</td>

<td style="text-align:right;">

0.204

</td>

<td style="text-align:right;">

0.832

</td>

<td style="text-align:right;">

0.406

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeBachelor deg

</td>

<td style="text-align:right;">

0.551

</td>

<td style="text-align:right;">

0.164

</td>

<td style="text-align:right;">

3.358

</td>

<td style="text-align:right;">

0.001

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeGraduate deg

</td>

<td style="text-align:right;">

0.673

</td>

<td style="text-align:right;">

0.188

</td>

<td style="text-align:right;">

3.573

</td>

<td style="text-align:right;">

0.000

</td>

</tr>

<tr>

<td style="text-align:left;">

partyid\_3Ind

</td>

<td style="text-align:right;">

0.401

</td>

<td style="text-align:right;">

0.107

</td>

<td style="text-align:right;">

3.759

</td>

<td style="text-align:right;">

0.000

</td>

</tr>

<tr>

<td style="text-align:left;">

partyid\_3Rep

</td>

<td style="text-align:right;">

0.325

</td>

<td style="text-align:right;">

0.123

</td>

<td style="text-align:right;">

2.647

</td>

<td style="text-align:right;">

0.008

</td>

</tr>

<tr>

<td style="text-align:left;">

sexFemale

</td>

<td style="text-align:right;">

\-0.235

</td>

<td style="text-align:right;">

0.092

</td>

<td style="text-align:right;">

\-2.549

</td>

<td style="text-align:right;">

0.011

</td>

</tr>

</tbody>

</table>

According to this model:

  - The older a person is, the lower the probability of accepting that a
    racist person should be allowed to teach.
  - People with higher levels of education are more likely to accept
    that a racist person should be allowed to teach, relatively to a
    person with no high school diploma.
  - Republicans and independents are more likely to accept that a racist
    person should be allowed to teach, relatively to a democrat.
  - Women are less likely to accept that a racist person should be
    allowed to teach, relatively to men.

When including a dummy variable indicating **whether the surveyed person
is black or whether is hispanic**, most of the results remain the same;
only the factor regarding a person’s identification with the Republican
party loses statistical significance. In addition, we can state that
African Americans and Hispanic people are less likely to accept that a
racist professor teaches at a university. This is shown in **Table 2**.

<table>

<caption>

Table 2: predictors of attitudes towards racist professors considering
race

</caption>

<thead>

<tr>

<th style="text-align:left;">

Predictor

</th>

<th style="text-align:right;">

B

</th>

<th style="text-align:right;">

SE

</th>

<th style="text-align:right;">

t

</th>

<th style="text-align:right;">

p

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

(Intercept)

</td>

<td style="text-align:right;">

0.194

</td>

<td style="text-align:right;">

0.225

</td>

<td style="text-align:right;">

0.861

</td>

<td style="text-align:right;">

0.389

</td>

</tr>

<tr>

<td style="text-align:left;">

age

</td>

<td style="text-align:right;">

\-0.005

</td>

<td style="text-align:right;">

0.003

</td>

<td style="text-align:right;">

\-1.842

</td>

<td style="text-align:right;">

0.065

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeHS

</td>

<td style="text-align:right;">

\-0.120

</td>

<td style="text-align:right;">

0.141

</td>

<td style="text-align:right;">

\-0.851

</td>

<td style="text-align:right;">

0.395

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeJunior Coll

</td>

<td style="text-align:right;">

0.086

</td>

<td style="text-align:right;">

0.208

</td>

<td style="text-align:right;">

0.413

</td>

<td style="text-align:right;">

0.680

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeBachelor deg

</td>

<td style="text-align:right;">

0.444

</td>

<td style="text-align:right;">

0.169

</td>

<td style="text-align:right;">

2.620

</td>

<td style="text-align:right;">

0.009

</td>

</tr>

<tr>

<td style="text-align:left;">

degreeGraduate deg

</td>

<td style="text-align:right;">

0.561

</td>

<td style="text-align:right;">

0.194

</td>

<td style="text-align:right;">

2.899

</td>

<td style="text-align:right;">

0.004

</td>

</tr>

<tr>

<td style="text-align:left;">

partyid\_3Ind

</td>

<td style="text-align:right;">

0.291

</td>

<td style="text-align:right;">

0.111

</td>

<td style="text-align:right;">

2.627

</td>

<td style="text-align:right;">

0.009

</td>

</tr>

<tr>

<td style="text-align:left;">

partyid\_3Rep

</td>

<td style="text-align:right;">

0.173

</td>

<td style="text-align:right;">

0.129

</td>

<td style="text-align:right;">

1.339

</td>

<td style="text-align:right;">

0.180

</td>

</tr>

<tr>

<td style="text-align:left;">

sexFemale

</td>

<td style="text-align:right;">

\-0.227

</td>

<td style="text-align:right;">

0.093

</td>

<td style="text-align:right;">

\-2.451

</td>

<td style="text-align:right;">

0.014

</td>

</tr>

<tr>

<td style="text-align:left;">

blackYes

</td>

<td style="text-align:right;">

\-0.532

</td>

<td style="text-align:right;">

0.139

</td>

<td style="text-align:right;">

\-3.821

</td>

<td style="text-align:right;">

0.000

</td>

</tr>

<tr>

<td style="text-align:left;">

hispanic\_2Yes

</td>

<td style="text-align:right;">

\-0.222

</td>

<td style="text-align:right;">

0.142

</td>

<td style="text-align:right;">

\-1.567

</td>

<td style="text-align:right;">

0.117

</td>

</tr>

</tbody>

</table>

### Second approach: considering scales

Now, we should consider that other factors influence the attitudes of
people towards racism; we can examine authoritarian, egalitarian and
tolerance tendency, and understand how influential they are in the level
of racism acceptence.

<table>

<caption>

Table 3: scales as predictors of attitudes towards racist professors

</caption>

<thead>

<tr>

<th style="text-align:left;">

Predictor

</th>

<th style="text-align:right;">

B

</th>

<th style="text-align:right;">

SE

</th>

<th style="text-align:right;">

t

</th>

<th style="text-align:right;">

p

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

(Intercept)

</td>

<td style="text-align:right;">

\-5.770

</td>

<td style="text-align:right;">

0.349

</td>

<td style="text-align:right;">

\-16.542

</td>

<td style="text-align:right;">

0.000

</td>

</tr>

<tr>

<td style="text-align:left;">

authoritarianism

</td>

<td style="text-align:right;">

0.143

</td>

<td style="text-align:right;">

0.036

</td>

<td style="text-align:right;">

3.995

</td>

<td style="text-align:right;">

0.000

</td>

</tr>

<tr>

<td style="text-align:left;">

egalit\_scale

</td>

<td style="text-align:right;">

\-0.010

</td>

<td style="text-align:right;">

0.006

</td>

<td style="text-align:right;">

\-1.706

</td>

<td style="text-align:right;">

0.088

</td>

</tr>

<tr>

<td style="text-align:left;">

tolerance

</td>

<td style="text-align:right;">

0.517

</td>

<td style="text-align:right;">

0.026

</td>

<td style="text-align:right;">

19.893

</td>

<td style="text-align:right;">

0.000

</td>

</tr>

</tbody>

</table>

According to **Table 3**, as we could, a prior, assume, people with
higher tendency levels of tolerance, are more acceptance of racist
behaviors; that is, they would be more likely to accept that that a
racist person should be allowed to teach. Also, more authoritarian
people present the same behavior. Mine while, those who are more
egalitarian, are less likely to accept that a racist professor teaches
at a university or
college.

![](racist-professors_files/figure-gfm/plot%20model%201%20&%202%20&%203-1.png)<!-- -->

## Conclusions

Based on the previous analysis, we could argue that many factors
influence people’s attitudes towards racism. In general terms we could
say that:

  - Being part of a minority group decreases the probability of
    accepting racist behaviors.
  - Political affiliations are also correlated with the level of
    acceptance of racism. A republican person is more likely to tolerate
    the fact that a racist professor teaches at a university.
  - Identifying as women is negatively correlated with the likelihood of
    accepting a racist professor.
  - People with higher levels of tolerance, are also more accepting of
    racist professors teaching in universities and
    colleges.

## Session info

``` r
devtools::session_info()
```

    ## ─ Session info ───────────────────────────────────────────────────────────────
    ##  setting  value                               
    ##  version  R version 3.6.3 (2020-02-29)        
    ##  os       Red Hat Enterprise Linux 8.1 (Ootpa)
    ##  system   x86_64, linux-gnu                   
    ##  ui       X11                                 
    ##  language (EN)                                
    ##  collate  en_US.UTF-8                         
    ##  ctype    en_US.UTF-8                         
    ##  tz       America/Chicago                     
    ##  date     2020-05-25                          
    ## 
    ## ─ Packages ───────────────────────────────────────────────────────────────────
    ##  package     * version  date       lib source                        
    ##  assertthat    0.2.1    2019-03-21 [2] CRAN (R 3.6.3)                
    ##  backports     1.1.5    2019-10-02 [2] CRAN (R 3.6.3)                
    ##  broom       * 0.5.6    2020-04-20 [1] CRAN (R 3.6.3)                
    ##  callr         3.4.3    2020-03-28 [2] CRAN (R 3.6.3)                
    ##  cellranger    1.1.0    2016-07-27 [2] CRAN (R 3.6.3)                
    ##  cli           2.0.2    2020-02-28 [2] CRAN (R 3.6.3)                
    ##  colorspace    1.4-1    2019-03-18 [2] CRAN (R 3.6.3)                
    ##  crayon        1.3.4    2017-09-16 [2] CRAN (R 3.6.3)                
    ##  DBI           1.1.0    2019-12-15 [2] CRAN (R 3.6.3)                
    ##  dbplyr        1.4.2    2019-06-17 [2] CRAN (R 3.6.3)                
    ##  desc          1.2.0    2018-05-01 [2] CRAN (R 3.6.3)                
    ##  devtools      2.3.0    2020-04-10 [1] CRAN (R 3.6.3)                
    ##  digest        0.6.25   2020-02-23 [2] CRAN (R 3.6.3)                
    ##  dplyr       * 0.8.5    2020-03-07 [2] CRAN (R 3.6.3)                
    ##  ellipsis      0.3.0    2019-09-20 [2] CRAN (R 3.6.3)                
    ##  evaluate      0.14     2019-05-28 [2] CRAN (R 3.6.3)                
    ##  fansi         0.4.1    2020-01-08 [2] CRAN (R 3.6.3)                
    ##  farver        2.0.3    2020-01-16 [2] CRAN (R 3.6.3)                
    ##  forcats     * 0.5.0    2020-03-01 [2] CRAN (R 3.6.3)                
    ##  fs            1.4.0    2020-03-31 [2] CRAN (R 3.6.3)                
    ##  generics      0.0.2    2018-11-29 [2] CRAN (R 3.6.3)                
    ##  ggplot2     * 3.3.0    2020-03-05 [2] CRAN (R 3.6.3)                
    ##  ggstance      0.3.4    2020-04-02 [1] CRAN (R 3.6.3)                
    ##  glue          1.4.0    2020-04-03 [1] CRAN (R 3.6.3)                
    ##  gtable        0.3.0    2019-03-25 [2] CRAN (R 3.6.3)                
    ##  haven         2.2.0    2019-11-08 [2] CRAN (R 3.6.3)                
    ##  here        * 0.1      2017-05-28 [1] CRAN (R 3.6.3)                
    ##  highr         0.8      2019-03-20 [2] CRAN (R 3.6.3)                
    ##  hms           0.5.3    2020-01-08 [2] CRAN (R 3.6.3)                
    ##  htmltools     0.4.0    2019-10-04 [2] CRAN (R 3.6.3)                
    ##  httr          1.4.1    2019-08-05 [2] CRAN (R 3.6.3)                
    ##  jsonlite      1.6.1    2020-02-02 [2] CRAN (R 3.6.3)                
    ##  jtools      * 2.0.5    2020-04-21 [1] CRAN (R 3.6.3)                
    ##  kableExtra  * 1.1.0    2019-03-16 [1] CRAN (R 3.6.3)                
    ##  knitr         1.28     2020-02-06 [2] CRAN (R 3.6.3)                
    ##  labeling      0.3      2014-08-23 [2] CRAN (R 3.6.3)                
    ##  lattice       0.20-38  2018-11-04 [2] CRAN (R 3.6.3)                
    ##  lifecycle     0.2.0    2020-03-06 [2] CRAN (R 3.6.3)                
    ##  lubridate     1.7.8    2020-04-06 [1] CRAN (R 3.6.3)                
    ##  magrittr      1.5      2014-11-22 [2] CRAN (R 3.6.3)                
    ##  MASS          7.3-51.5 2019-12-20 [2] CRAN (R 3.6.3)                
    ##  memoise       1.1.0    2017-04-21 [2] CRAN (R 3.6.3)                
    ##  modelr        0.1.6    2020-02-22 [2] CRAN (R 3.6.3)                
    ##  munsell       0.5.0    2018-06-12 [2] CRAN (R 3.6.3)                
    ##  nlme          3.1-144  2020-02-06 [2] CRAN (R 3.6.3)                
    ##  pander        0.6.3    2018-11-06 [1] CRAN (R 3.6.3)                
    ##  pillar        1.4.3    2019-12-20 [2] CRAN (R 3.6.3)                
    ##  pkgbuild      1.0.6    2019-10-09 [2] CRAN (R 3.6.3)                
    ##  pkgconfig     2.0.3    2019-09-22 [2] CRAN (R 3.6.3)                
    ##  pkgload       1.0.2    2018-10-29 [2] CRAN (R 3.6.3)                
    ##  plyr          1.8.6    2020-03-03 [2] CRAN (R 3.6.3)                
    ##  prettyunits   1.1.1    2020-01-24 [2] CRAN (R 3.6.3)                
    ##  processx      3.4.2    2020-02-09 [2] CRAN (R 3.6.3)                
    ##  ps            1.3.2    2020-02-13 [2] CRAN (R 3.6.3)                
    ##  purrr       * 0.3.3    2019-10-18 [2] CRAN (R 3.6.3)                
    ##  R6            2.4.1    2019-11-12 [2] CRAN (R 3.6.3)                
    ##  rcfss         0.1.9    2020-04-18 [1] Github (uc-cfss/rcfss@6dd8d8b)
    ##  Rcpp          1.0.4    2020-03-17 [2] CRAN (R 3.6.3)                
    ##  readr       * 1.3.1    2018-12-21 [2] CRAN (R 3.6.3)                
    ##  readxl        1.3.1    2019-03-13 [1] CRAN (R 3.6.3)                
    ##  remotes       2.1.1    2020-02-15 [2] CRAN (R 3.6.3)                
    ##  reprex        0.3.0    2019-05-16 [2] CRAN (R 3.6.3)                
    ##  rlang         0.4.5    2020-03-01 [2] CRAN (R 3.6.3)                
    ##  rmarkdown     2.1      2020-01-20 [2] CRAN (R 3.6.3)                
    ##  rprojroot     1.3-2    2018-01-03 [2] CRAN (R 3.6.3)                
    ##  rstudioapi    0.11     2020-02-07 [2] CRAN (R 3.6.3)                
    ##  rvest         0.3.5    2019-11-08 [2] CRAN (R 3.6.3)                
    ##  scales        1.1.0    2019-11-18 [2] CRAN (R 3.6.3)                
    ##  sessioninfo   1.1.1    2018-11-05 [2] CRAN (R 3.6.3)                
    ##  stringi       1.4.6    2020-02-17 [2] CRAN (R 3.6.3)                
    ##  stringr     * 1.4.0    2019-02-10 [2] CRAN (R 3.6.3)                
    ##  testthat      2.3.2    2020-03-02 [2] CRAN (R 3.6.3)                
    ##  tibble      * 3.0.0    2020-03-30 [2] CRAN (R 3.6.3)                
    ##  tidyr       * 1.0.2    2020-01-24 [2] CRAN (R 3.6.3)                
    ##  tidyselect    1.0.0    2020-01-27 [2] CRAN (R 3.6.3)                
    ##  tidyverse   * 1.3.0    2019-11-21 [1] CRAN (R 3.6.3)                
    ##  usethis       1.6.0    2020-04-09 [1] CRAN (R 3.6.3)                
    ##  vctrs         0.2.4    2020-03-10 [2] CRAN (R 3.6.3)                
    ##  viridisLite   0.3.0    2018-02-01 [2] CRAN (R 3.6.3)                
    ##  webshot       0.5.2    2019-11-22 [1] CRAN (R 3.6.3)                
    ##  withr         2.1.2    2018-03-15 [2] CRAN (R 3.6.3)                
    ##  xfun          0.12     2020-01-13 [2] CRAN (R 3.6.3)                
    ##  xml2          1.3.0    2020-04-01 [2] CRAN (R 3.6.3)                
    ##  yaml          2.2.1    2020-02-01 [2] CRAN (R 3.6.3)                
    ## 
    ## [1] /home/mabenavides/R/x86_64-redhat-linux-gnu-library/3.6
    ## [2] /usr/lib64/R/library
    ## [3] /usr/share/R/library
