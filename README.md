# Text classification data for publication bias

This repository contains the text evidence for classification of labor union data in Section 4.2 of my paper "Publication Bias under Aggregation Frictions." 

## Repository content
- 01_data
  - classification.csv = summary results of classifications
  - original.csv = extracted data from Doucouliagos et al. 2018
- 02_text
  - 01-09,...,70-73 = scanned PDF of papers with highlights as contained in Doucouliagos and Laroche 2003 paper
  - additional = scanned PDF of papers with highlights as added in Doucouliagos et al. 2018 paper
  
## Objectives for classification
The objective of paper classification is to focus on the meta-analysis data for which the communication model makes empirical predictions: the papers that highlight the dichotomous, yes-or-no conclusion for readers who aggregate multiple papers without consulting the regression coefficients and their standard errors. Yet the meta-analysis data also contain papers that have their estimates in the main text without highlighting in easy-to-read sections of the paper. 

## Process of classification
We read the abstract, and whenever available, also the introduction and the conclusions of the papers to examine whether each paper highlights the binary conclusions. This manual classification method is practical compared to automated method since each combination of words for each paper will look different from each other. However, it also raises the concerns whether multiple analyzers will reach the same classification. Here, there are three values we hoped to pursue in this analysis:
1.	Consistency: minimize the human error in classification
2.	Verifiability: other analyzers can verify the reasons of classification
3.	Conservativeness: exclude as least papers as possible from the data (we hope to avoid making arbitrary selection of data.)

Given the resource available, we designed the classification process and record herein to pursue the above values.
1. Consistency: Whenever possible, Chishio Furukawa and 1 Research Assistant for each meta-analysis independently classified the papers into categories. When there were disagreement, we discussed whether this was due to (i) human error (unintentionally missing some parts of the text), or (ii) genuine disagreement due to ambiguity of language.
   - there was an unanticipated update of the data in October 2018, as I met with Chris Doucouliagos at the MAER-Net Colloquium. We originally only had data from Doucouliagos and Laroche (2003), but updated to incorporate data from Doucouliagos, Freeman, Laroche, and Stanley (2017.) However, the contract with Research Assistants had been expired by this time. Thus, classification of additional 34 papers were conducted by Chishio alone.

2. Verifiability: To ensure that the readers of the paper can verify the classification, we have made the following documentation:
   i.	PDF that highlights the main parts of text or lack thereof
   ii.	Discussion on classification where there were disagreements due to (ii) ambiguity of language
   iii.	Summary of all classifications and the text evidence behind them (for (i), we have corrected to reach the correct classification).
3.  Conservativeness: if there were ambiguity due to the text evidence, we chose the classification that will lead to the least amount of omission from the data.

## Content of classification
"classification.csv" contains the results from the manual classification. 
-	1 if it indicated that unions increased firm productivity
-	0 if unions had no statistically significant impact on productivity
-	-1 if unions had a negative effect on productivity
-	100 if the article did not mention the impact of unions on productivity
-	101 if the findings were inconclusive.
- 102 if the article belonged to a book
- 103 if the article could not be found

This assessment was based on reviewing article abstracts, introductions, and conclusions until an outcome was mentioned. There were 7 books that were all included in the analyses since they do not follow the format of abstract, introduction, and conclusions. There were 3 articles that could not be found even after extensive search.

## Reasons for multiple assessments
If there were multiple assessments possible due to (i) ambiguity of language as main reason above, we listed 2 classifications for each article. There were following 3 kinds of ambiguities:

1. Heterogeneous effects on different groups: while the articles mentioned that unions had heterogeneous effects on productivity depending on the group that was examined, Classification 1 assigned a single number regardless of specific group results while Classification 2 assigned numbers that varied by group.
   - An example of Milkman (1997) demonstrates this. The article writes “The union/nonunion productivity differential for average minority students is positive. However, the productivity differential is negative for minority students attending schools where the majority of students are nonminority, but the productivity differential is positive for minority students attending schools where the majority of students are minorities.” There are several classifications within the article’s overarching examination of productivity and minority students.
   
2.	No direct statement regarding unions and productivity: Some articles made no clear statement that specifically concerned the impact of unions on firm productivity. They focused on the impact of other factors, like labor management practices or technologies, on productivity instead.
   - An example of Black and Lynch (2001) shows this. The article writes “Unionized establishments that have adopted human resource practices that promote joint decision making coupled with incentive-based compensation have higher productivity than other similar nonunion plants, whereas unionized businesses that maintain more traditional labor management relations have lower productivity.” This statement expresses whether labor management relations affect productivity, which may or may not indicate unionization.
   
3.	Variation in text evidence: the evidence selected to support each classification’s claim varied, with each piece supporting a different conclusion.
   - An example of Guthrie (2001) demonstrates this. In Classification 1, one reviewer has put “Study results indicate a positive association between use of high-involvement work practices and employee retention and firm productivity.” In Classification 2, another reviewer has put “high involvement work practices may have implications for the effect of turnover on firm productivity; turnover is adversely associated with productivity when the use of these practices is high and, conversely, turnover is positively associated with productivity when use of the practices is low.” Classification 1’s evidence focuses on the impact of high-involvement work practices, not unionization, on productivity, resulting in a classification of 100. Classification 2’s evidence resulted in a classification of -1, since high-involvement was taken to mean more worker voice and participation, along the lines of unionization, having a negative effect on productivity.

## References
- Doucouliagos, Christos, and Patrice Laroche. 2003. “What Do Unions Do to Productivity? A Meta-Analysis.” Industrial Relations: A Journal of Economy and Society
- Doucouliagos, Christos, Richard Freeman, Patrice Laroche, and Tom Stanley. 2018. “How Credible is Trade Union Research? Forty Years of Evidence on the Monopoly-Voice Tradeoff.” Industrial Relations: A Journal of Economy and Society

## Acknowledgment
I thank my Research Assistants, Shreya Parajan and Beryce Garcia, for helping me through the classification process in 2018.
