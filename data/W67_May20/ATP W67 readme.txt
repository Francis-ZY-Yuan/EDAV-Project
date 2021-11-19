PEW RESEARCH CENTER
Wave 67 American Trends Panel 
Dates: April 29 - May 5, 2020
Mode: Web 
Sample: Subsample
Language: English and Spanish
N=10,957

***************************************************************************************************************************

INTERNAL NOTE


**This is where we would put info about how the dataset was changed since Ipsos sent it. This may be in word docs in the data folder for some waves***


***************************************************************************************************************************
WEIGHTS 

There are three weights in the W67 dataset:

WEIGHT_W67 is the weight for the sample. Data for most Pew Research Center reports are analyzed using this weight.
WEIGHT_W66_W67 is the longitudinal weight to use for analysis of respondents to both Wave 66 and Wave 67.[THIS WEIGHT IS USED FOR LONGITUDINAL ANALYSIS WITH VARIABLE COVIDFOL_W66 INCLUDED IN THIS DATASET]
WEIGHT_W67_ASIAN is a custom weight to separate Asians from the Other race category to allow for reporting on Asian Americans. [THIS WEIGHT IS USED IN THE REPORT LISTED BELOW DATED SEPTEMBER 17, 2020]


***************************************************************************************************************************
Releases from this survey:

**All Pew Research Center research on coronavirus can be found at https://www.pewresearch.org/topics/coronavirus-disease-2019-covid-19/***


May 15, 2020 "Majority of Americans who lost a job or wages due to COVID-19 concerned states will reopen too quickly"
https://www.pewresearch.org/fact-tank/2020/05/15/majority-of-americans-who-lost-a-job-or-wages-due-to-covid-19-concerned-states-will-reopen-too-quickly/

May 20, 2020 "Americans favor medical care but not economic aid for undocumented immigrants affected by COVID-19"
https://www.pewresearch.org/fact-tank/2020/05/20/americans-favor-medical-care-but-not-economic-aid-for-undocumented-immigrants-affected-by-covid-19/

May 21, 2020 "Trust in Medical Scientists Has Grown in U.S., but Mainly Among Democrats" 
https://www.pewresearch.org/science/2020/05/21/trust-in-medical-scientists-has-grown-in-u-s-but-mainly-among-democrats/ 

May 21, 2020 "Most Americans expect a COVID-19 vaccine within a year, 72% say they would get vaccinated"
https://www.pewresearch.org/fact-tank/2020/05/21/most-americans-expect-a-covid-19-vaccine-within-a-year-72-say-they-would-get-vaccinated/ 

May 26, 2020 "Few U.S. adults say they’ve been diagnosed with coronavirus, but more than a quarter know someone who has"
https://www.pewresearch.org/fact-tank/2020/05/26/few-u-s-adults-say-theyve-been-diagnosed-with-coronavirus-but-more-than-a-quarter-know-someone-who-has/

June 4, 2020 "Black Americans face higher COVID-19 risks, are more hesitant to trust medical scientists, get vaccinated"
https://www.pewresearch.org/fact-tank/2020/06/04/black-americans-face-higher-covid-19-risks-are-more-hesitant-to-trust-medical-scientists-get-vaccinated/

June 8, 2020 "Most Americans say despite ongoing research, ways to limit spread of COVID-19 are well understood"
https://www.pewresearch.org/fact-tank/2020/06/29/most-americans-say-climate-change-impacts-their-community-but-effects-vary-by-region-2/ 

June 10, 2020 "A majority of Americans say immigrants mostly fill jobs U.S. citizens do not want"
https://www.pewresearch.org/fact-tank/2020/06/10/a-majority-of-americans-say-immigrants-mostly-fill-jobs-u-s-citizens-do-not-want/

June 16, 2020 "Experiences with the COVID-19 outbreak can vary for Americans of different ages"
https://www.pewresearch.org/fact-tank/2020/06/16/experiences-with-the-covid-19-outbreak-can-vary-for-americans-of-different-ages/

June 23, 2020 "Two-Thirds of Americans Think Government Should Do More on Climate" 
https://www.pewresearch.org/science/2020/06/23/two-thirds-of-americans-think-government-should-do-more-on-climate/ 

June 24, 2020 "Millennial and Gen Z Republicans stand out from their elders on climate and energy issues"
https://www.pewresearch.org/fact-tank/2020/06/24/millennial-and-gen-z-republicans-stand-out-from-their-elders-on-climate-and-energy-issues/ 

June 25, 2020 "Younger, more educated U.S. adults are more likely to take part in citizen science research"
https://www.pewresearch.org/fact-tank/2020/06/25/younger-more-educated-u-s-adults-are-more-likely-to-take-part-in-citizen-science-research/ 

June 29, 2020 "Most Americans say climate change affects their local community, including 70% living near a coast"
https://www.pewresearch.org/fact-tank/2020/06/29/most-americans-say-climate-change-impacts-their-community-but-effects-vary-by-region-2/ 

September 17, 2020 "U.S. Public Now Divided Over Whether To Get COVID-19 Vaccine" [USES WEIGHT_W67_ASIAN]
https://www.pewresearch.org/science/2020/09/17/u-s-public-now-divided-over-whether-to-get-covid-19-vaccine/

***************************************************************************************************************************
SYNTAX

*Create F_PARTYSUMIDEO.
compute F_PARTYSUMIDEO = $sysmis.
if F_IDEO eq 1 and F_PARTYSUM_FINAL eq 1 F_PARTYSUMIDEO eq 1.
if F_IDEO eq 2 and F_PARTYSUM_FINAL eq 1 F_PARTYSUMIDEO eq 1.
if F_IDEO eq 3 and F_PARTYSUM_FINAL eq 1 F_PARTYSUMIDEO eq 2.
if F_IDEO eq 4 and F_PARTYSUM_FINAL eq 1 F_PARTYSUMIDEO eq 2.
if F_IDEO eq 5 and F_PARTYSUM_FINAL eq 1 F_PARTYSUMIDEO eq 2.
if F_IDEO eq 1 and F_PARTYSUM_FINAL eq 2 F_PARTYSUMIDEO eq 3.
if F_IDEO eq 2 and F_PARTYSUM_FINAL eq 2 F_PARTYSUMIDEO eq 3.
if F_IDEO eq 3 and F_PARTYSUM_FINAL eq 2 F_PARTYSUMIDEO eq 3.
if F_IDEO eq 4 and F_PARTYSUM_FINAL eq 2 F_PARTYSUMIDEO eq 4.
if F_IDEO eq 5 and F_PARTYSUM_FINAL eq 2 F_PARTYSUMIDEO eq 4.
if F_IDEO eq 99 or F_PARTYSUM_FINAL eq 9 F_PARTYSUMIDEO eq 9.
variable labels F_PARTYSUMIDEO 'Combination variable of F_IDEO and F_PARTYSUM_FINAL'. 
value labels F_PARTYSUMIDEO 1 'Conservative Rep/Lean' 2 'Moderate/Liberal Rep/Lean' 3 'Moderate/Conservative Dem/Lean' 4 'Liberal Dem/Lean' 9 'Refused either F_IDEO or F_PARTYSUM_FINAL'.


