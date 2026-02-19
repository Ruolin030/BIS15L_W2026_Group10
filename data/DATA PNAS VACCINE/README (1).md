# Title of Dataset: Visual policy narrative messaging and COVID-19 vaccine uptake
---
Our research team conducted a three-wave online panel survey through QualtricsXM of individuals in 50 U.S. states and Washington D.C. in 2021. We contracted with QualtricsXM to administer the survey using their proprietary panels of online survey respondents. These panel participants are recruited from a variety of sources, including website intercept recruitment, targeted email lists, gaming sites, customer loyalty web portals, and social media. Here, we present data from T1 (n = 3,900; launched between January 11 and February 3, 2021) and T2 (n = 2,268; launched between March 22 and April 9, 2021). In these survey waves, we conducted an experiment wherein respondents were randomly assigned to one of four experimental conditions in T1, comprised of three visual policy narrative treatment conditions (“protect yourself,” n = 986, 25%; “protect your circle,” n = 974, 25%; “protect your community,” n = 955, 25%) and a control condition (“get the vaccine”, n = 969, 25%). 

We conduct two main analyses. Analysis 1 assessed the overall effect of narrative risk messages (Xi) on vaccination (Y1), moderated by political ideology (W), controlling for covariates risk perception, COVID-19 experience, flu vaccine behavior, and demographics. Analysis 2, we test (i) the mediation effects of message conditions (Xi) through affective response (M1) and motivation to vaccinate (M2) on vaccine behavior at T2 (Y1), both as individual mediators and as serial mediators, and (ii) the moderation effects of political beliefs (W) for these mediation effects, as well as for the direct effect of message conditions on affective response (M1), motivation to vaccinate (M2), and on vaccine behavior (Y1), all controlling for covariates risk perception, COVID-19 experience, flu vaccine behavior, and demographics.

For the analysis, we use Hayes’ PROCESS models, a regression-based moderated mediation model, the regression coefficients of which are estimated using OLS regression (when M1 or M2 are the outcome variables) and logit regression analysis (when Y1 is the dichotomous outcome variable). For all models, we use 95% confidence intervals, and 5000 bootstrap samples to generate bias-corrected confidence intervals. Given that the Xi variable is a multicategorical variable, both Analysis 1 used two kinds of coding to represent the experimental conditions. The first is indicator coding, which compares each treatment condition to the control.

X1 = "protect yourself" compared to control

X2 = "protect the circle" compared to control

X3 = "protect the community" compared to control

The second is Helmert contrast coding, which is a successive comparison of conditions.

X4 = the average of all three narrative message conditions compared to control

X5 = “protect the circle” plus “protect the community” vs. “protect yourself”

X6 = “protect the community” compared to “protect the circle”

Thus, in the full statistical model, each path from Xi to other variables includes three different paths, each representing the path from Xi to other variables. Similarly, each moderating effect of W includes interaction terms with Xi.
Brief summary of dataset contents, contextualized in experimental procedures and results.


## Description of the Data and file structure

Data are in a csv file. 
Rows represent a unique respondent responses to survey questions. 
Columns represent variable names and responses. 
Cells that read "null" are missing responses. 
T1 = first wave of the survey
T2 = second wave of the survey
Y = dependent or outcome variable
X = independent variable
M = mediator variable
W = moderating variable


**Variable Summary**
Column A = ResponseId = respondent identificaiton number. Because we have multiple waves in this survey (i.e., T1 and T2), it is important to track respondent responses across waves.
Column B = Y_vaccgot2 = Vaccine behavior (Y1; T2)	
* received one or more COVID-19 vaccine doses	
* 0 = no; 1 = yes	
* Mean = .44
* n = 2268
Column C = X_condR = experimental treatment
* received one or more COVID-19 vaccine doses	
* 1 = control; 2 = protect yourself; 3 = protect your circle; 4 = protect your community	
* n = 3884
Column D = M1_valancR1 = Affective response (M1; T1)

* rate reaction to message	
* 1=extremely negative; 2 = moderately negative; 3 = slightly negative; 4 = neither positive nor negative; 5 = slightly positive; 6 = moderately positive; 7 = extremely positive	
* Mean  = 4.84
* s.d. = 1.614
* n = 3884
Column E = M2_motYOU1R = Motivation to vaccinate (M2; T1)	
* motivate to get COVID-19 vaccine after image exposure	
* 1 = not at all to 7 = a great deal (there were no words for 2, 3, 4, 5, 6, just a scale with labeled end points)
* Mean = 3.79
* s.d. = 2.067
* n = 3493
Column F = W_pol_ideo = Political ideology (W; T1)	
* political ideology scale	 
* 1=extremely conservative; 2 = conservative; 3 = slightly conservative; 4 = moderate, middle of the road; 5 = slightly liberal; 6 = liberal; 7 = extremely liberal
* Mean = 4
* s.d. = 1.598
* n = 3900

Covariates
Column G = RP_sevR1 = Risk perception: likelihood	
* Multi-item variable constructed from 3 variables: likelihood to (i) get COVID-19 (Column U = covrisk_get_wv1), (ii) get seriously ill (Column V = covrisk_ill_wv1), and (iii) die (Column W= covrisk_die_wv1). 
* Each of these 3 variables had responses on a 7-point scale: 1 = no chance; 2 = very low; 3 = low; 4 = medium; 5 = high; 6 = very high; 7 = certain
* Multi-item variable scale built, revealing a scale from 1 = not a chance to 19 = certain
* Cronbach’s alpha = .805	
* Mean = 7.42
* s.d. = 3.721
* n = 3885
Column H = RP_likR1 = Risk perception: severity	
* Multi-item variable constructed from 4 variables: worry about COVID-19 (i) getting it Column X = covid_worry_1_wv1), (ii) others I care about getting it (Column Y = covid_worry_2_wv1), (iii) feel anxious (Column Z =covid_worry_3_wv1), (iv) feel uncomfortable (Column AA = covid_worry_4_wv1). 
* Each of these variables had rsponses on a 5 point scale: 1 = strongly disagree; 2 = disagree; 3 = neither agree nor disagree; 4 = agree; 5 = strongly agree
* Multi-item variable scale built, revealing a scale from 1 = strongly disagree to 17 = strongly agree
* Cronbach’s alpha = .864	▁X = 10.84
* s.d. = 4.347
* n = 3900
Column I = hadcovi1 = COVID-19 experience	
* Have you had COVID-19	
* 0 = no; 1 = yes	
* Mean = .15
* n = 3517
Column J = flushot1 = Flu vaccine frequency	
* How often get flu vaccine inlast 5 years	
* 0 = never; 1 = onece or twice; 2 = most years but not all; 3 = every year	
* Mean = 1.59
* s.d. = 1.24
* n = 3900
Column K = race1R = Race	
* What is your race 	
* 0 = all other races; 1 = White	
* Mean = .24
* n = 3900
Column L = genderR1 = Gender	
* WHat is oyur gender
* 0 = Male; 1 = Female/non-binary	
* Mean = .50 
* n = 3887
Column M = age = Age	
* Age in years	
* 18 to 93	
* Mean = 45.05
* s.d. = 17.594
* n = 3900
Column N = educ = Education	
* Levels of education 	
* 1 = less than high school; 2 = high school; 3 = some college; 4 = 2 year degree; 5 = 4 year degree; 6 = graduate degre
* Mean = 3.94
* s.d. = 1.487
* n = 3900
Column O = income =Income 	
* Household pre-tax income in 2020	
* 1 = $10k or less; 2 = $10,001 - $20k; 3 = $20,001 - $30k; 4 = $30,001 to $40k; 5 = $40,001 - $50k; 6 = $50,001 - $60k; 7 = $60,001 - $80k; 8 = $80,001 - $100k; 9 = $101,001 - $150k; 10 = more than $150k	
* Mean = 5.81
* s.d. = 2.817
* n = 3900
Column P = kidsR = Children	
* Number of children under 18 years live in household
* 0 to 10	
* Mean = 0.67
* s.d. = 1.017
* n = 3889

missing data codes = null



## Sharing/access Information

These data are not linked to other publicly accessible locations of the data

