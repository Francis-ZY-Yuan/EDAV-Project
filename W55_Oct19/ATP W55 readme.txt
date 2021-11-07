PEW RESEARCH CENTER
Wave 55 American Trends Panel 
Dates: October 1 - October 13, 2019
Mode: Web
Sample: Subsample
Language: English and Spanish
N= 3,627

***************************************************************************************************************************
NOTES

The Politics team released a report on October 17, 2019 that used a special cross-wave weight for the combined samples of W53 and W55, which both contained questions about presidential impeachment. A total of 3,487 panelists responded to both W53 and W55.
The variable name for the longitudinal analysis weight is WEIGHT_W53_W55. Variable IMPEACHT_W53 is included for longitudinal analysis.

Variable EN6F1count_W55 is a count variable of the how many environmental actions respondents said they did as part of their everyday lives (from 0 to 5). Syntax to create this variable is included below. 


***************************************************************************************************************************
WEIGHTS 

The Wave 55 dataset includes two weights:

WEIGHT_W55 is the weight for the sample. Data for all Pew Research Center reports (except the 10/17/19 report mentioned above) are analyzed using this weight.
WEIGHT_W53_W55 is the weight used for longitudinal analysis for the 3,487 panelists that responded to both W53 and W55.

***************************************************************************************************************************
Releases from this survey:

October 17, 2019 "Modest Changes in Views of Impeachment Proceedings Since Early September"
https://www.people-press.org/2019/10/17/modest-changes-in-views-of-impeachment-proceedings-since-early-september/

November 25, 2019 "U.S. Public Views on Climate and Energy"
https://www.pewresearch.org/science/2019/11/25/u-s-public-views-on-climate-and-energy/

December 2, 2019 "Most Americans say climate change impacts their community, but effects vary by region"
https://www.pewresearch.org/fact-tank/2019/12/02/most-americans-say-climate-change-impacts-their-community-but-effects-vary-by-region/

December 17, 2019 "Most U.S. homeowners say they are considering home solar panels"
https://www.pewresearch.org/fact-tank/2019/12/17/more-u-s-homeowners-say-they-are-considering-home-solar-panels/

January 7, 2020 "More Americans now see ‘very high’ preventive heath benefits from measles vaccine"
https://www.pewresearch.org/fact-tank/2019/12/17/more-u-s-homeowners-say-they-are-considering-home-solar-panels/

March 18, 2020 "About half of U.S. adults are wary of health effects of genetically modified foods, but many also see advantages"
https://www.pewresearch.org/fact-tank/2020/03/18/about-half-of-u-s-adults-are-wary-of-health-effects-of-genetically-modified-foods-but-many-also-see-advantages/


***************************************************************************************************************************
SYNTAX

SPSS syntax to create EN6F1count_W55:

COUNT EN6F1count_W55=EN6F1_a_W55 to EN6F1_e_W55 (1).
If (EN6F1_a_W55=98 OR EN6F1_a_W55=99) OR 
(EN6F1_b_W55=98 OR EN6F1_b_W55=99) OR 
(EN6F1_c_W55=98 OR EN6F1_c_W55=99) OR 
(EN6F1_d_W55=98 OR EN6F1_d_W55=99) OR 
(EN6F1_e_W55=98 OR EN6F1_e_W55=99) 
EN6F1count_W55=99.
Execute.

Var label EN6F1count_W55 “COUNT: Do you do each of the following in your everyday life in order to help protect the environment, or don’t you?”.

value labels EN6F1count_W55 
0 'I do none of these' 
1 '1 of these' 
2 '2 of these' 
3 '3 of these' 
4 '4 of these' 
5 'I do all 5 of these'
99 'DK/Refused to any a - e'.




