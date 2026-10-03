
# Global-Paternity-Fraud-Analysis


Introduction
The Global Paternity Fraud Analysis project was developed as part of the Simulations Capstone Programme at Vephla University. The primary objective was to conduct a comprehensive global analysis of paternity fraud by examining its legal definitions, prevalence, psychological implications, economic consequences, and DNA testing accessibility across different countries and regions. The project utilized data analytics techniques to identify patterns, trends, and disparities in how paternity fraud is recognized and managed worldwide.

Through structured datasets, analytical tools, and interactive dashboards built in Microsoft Power BI, the study generated evidence-based insights to support discussions around legal protections, family welfare, and policy development.

Problem Being Addressed Paternity fraud occurs when a man is wrongly identified as the biological father of a child, either knowingly or unknowingly. This issue carries significant legal, emotional, psychological, and economic consequences for families and societies worldwide. One of the major challenges surrounding paternity fraud is the absence of reliable and globally consistent data. Many countries lack clearly defined legal frameworks specifically addressing paternity fraud, while available statistics are often fragmented, inconsistent, or underreported.

The project addressed several critical questions:

• How do legal systems across countries define and respond to paternity fraud?

. What are the documented psychological and financial impacts on affected families?

• How accessible and regulated are DNA testing services globally?

. Are there observable regional trends or disparities in legal treatment and testing accessibility?

• What evidence-based recommendations can improve legal and social support systems? 1.3





Objectives

● Conduct a comprehensive global analysis of paternity fraud; its definitions, frequency, and legal treatment across countries

● Assess the psychological and economic impact of paternity fraud on affected families using secondary data

● Evaluate the accessibility and regulation of DNA testing practices across different regions

● Produce a complete set of capstone deliverables including an interactive dashboard and technical report

● Generate evidence-based recommendations for legal, policy, and social welfare stakeholders.








<img width="903" height="513" alt="paternity fruad dashboard1" src="https://github.com/user-attachments/assets/91f7cbd7-b327-472d-ad23-56d560945dc8" />






Story of Data
Data Sources
The data used for this project was obtained primarily from secondary sources consisting of international organizations, academic publications, legal databases, demographic research institutions, and publicly available reports. Sources were selected based on their credibility, relevance, and alignment with the project objectives.




<img width="985" height="822" alt="Pat  1" src="https://github.com/user-attachments/assets/460b633d-6ee3-4a6e-94fc-a13929d25608" />





Data Structure
Four primary datasets were compiled from the sources above. After preprocessing and feature engineering, these were merged into a single consolidated Master Dataset. The final dataset contains 1,284 records across 11 variables.



<img width="1027" height="794" alt="Pat  2" src="https://github.com/user-attachments/assets/8f432334-ac9c-4f32-8bb6-65c67f90c041" />

<img width="988" height="225" alt="Pat 3" src="https://github.com/user-attachments/assets/bbc91a96-8e9a-470c-b30b-f0a6417a83bb" />








<img width="903" height="511" alt="paternity dashboard2" src="https://github.com/user-attachments/assets/5f56d08e-9372-40dd-b582-12b13517c179" />







Data Limitations and Biases

Limited Global Data Availability: Reliable and standardized global data specifically relating to paternity fraud remains limited. Many countries lack publicly accessible reporting systems or centralized legal databases dedicated to paternity-related disputes.

Inconsistent Legal Definitions: Definitions and legal interpretations of paternity fraud vary significantly across jurisdictions, making direct cross-country comparisons challenging.

Underreporting of Cases: Due to the sensitive nature of paternity fraud, many cases may have gone unreported, resulting in potential underrepresentation within available datasets.

Data Standardization Challenges: Data collected from multiple sources differed in terminology, reporting structure, and classification systems, requiring extensive preprocessing.

Missing and Incomplete Values: Some countries lacked complete information for variables such as DNA accessibility and psychological impact. 'Unknown' categories were assigned where appropriate.

Potential Regional Bias: A larger proportion of available literature originated from regions with stronger research infrastructure, which may have introduced geographical representation bias. Nigeria alone accounts for 58.4% of all records, which should be considered during interpretation.

Scope of Low DNA Access: No records were classified as 'Low' DNA access, which likely reflects a data gap rather than the absence of low-access regions globally.




Data Splitting and Preprocessing

Data Cleaning

The datasets were cleaned and standardized in Microsoft Excel using Power Query Editor. Since data was collected from multiple academic articles, legal reports, journals, and institutional databases, preprocessing was necessary to eliminate inconsistencies and prepare the datasets for integration and visualization. 

The following cleaning activities were performed:

Missing values in the year column were replaced using average-based estimation

Missing country-related values were estimated using observable regional and trend-based patterns across similar records

Over 1,000 duplicates were removed from the merged master dataset Blank rows that did not contribute to the analysis were removed

Country names were standardized to ensure consistency, e.g., 'USA' was changed to 'United States' and 'UK' to 'United Kingdom' to enable successful table joins



Columns Removed During Preprocessing

Non-analytical columns were removed from each dataset to reduce noise and improve focus. The following columns were dropped:



<img width="988" height="448" alt="columns-rem" src="https://github.com/user-attachments/assets/e56961a6-223d-415b-9a66-19eab30c0e2e" />



Feature Engineering

Feature engineering was carried out to create new, more meaningful variables from the raw data collected across the four datasets. Rather than working with raw text entries and inconsistent values directly, the team developed structured categories and scores that made the data easier to analyze and visualize. For example, a legal strength score was calculated for each country by evaluating whether key legal protections were in place, such as the existence of a legal definition for paternity fraud, the ability to challenge paternity claims, and whether child support reversal was permitted.


This score was then used to classify countries into Low, Medium, or High legal protection levels. Similarly, the time allowed for legal challenges was grouped into Flexible, Moderate, or Strict categories based on the nature of the time limits described in the source data.


The same approach was applied across the other datasets. Psychological impact descriptions were grouped into categories such as Trauma, Trust Issues, Identity Issues, and Mixed, while economic consequences were classified into categories including Child Support Loss, Long-term Financial Burden, and Legal Costs. DNA testing availability was assessed and classified based on how accessible and regulated testing services were within each country.


Finally, the method through which paternity fraud was discovered in each case was grouped into three categories: DNA Test, Legal Dispute, or Confession, and the severity of the financial impact was assessed and labelled as High, Medium, or Low based on the nature and scale of the consequences described. These engineered variables formed the foundation for the dashboard visualizations and KPI calculations that followed.




Table Merging and Integration

After preprocessing and feature engineering, the four datasets were merged into a consolidated master dataset using Left Outer Joins in Power Query Editor:

. The Case/Event dataset (primary table) was joined with the Legal Framework dataset on the country column

. The resulting table was joined with the DNA Testing dataset on country

. The merged table was then joined with the Impact dataset on country

Left Outer Joins were used to preserve all records from the primary Case/Event dataset, add matching information from supporting datasets, and retain records even where no corresponding match existed (shown as NULL rather than deleted). The final master dataset was exported as an Excel file and transferred into Microsoft Power BI for visualization and dashboard development.



Data Splitting
Variables were organized into independent and dependent analytical categories to support trend identification and comparative analysis:


<img width="984" height="304" alt="Cat" src="https://github.com/user-attachments/assets/71eea70b-a4c4-40b2-a0e8-4b988bf09657" />



Pre-Analysis

The pre-analysis phase focused on exploring the cleaned and transformed datasets to identify early patterns, inconsistencies, distributions, and relationships before conducting detailed dashboard visualization and KPI analysis in Microsoft Power BI.


Initial exploration of the merged datasets revealed considerable variation in legal framework strength, DNA testing accessibility, financial severity, and psychological impact across countries and regions. Early profiling showed that legal protection indicators were unevenly distributed, with some countries recording consistently higher legal strength scores due to formal paternity challenge procedures, DNA testing regulations, and child support reversal policies.


During preliminary exploration, DNA testing appeared repeatedly as the dominant discovery method across documented cases, suggesting that scientific verification systems play a major role in uncovering disputed paternity cases globally.


Exploratory review of the psychological impact variables showed that trauma-related descriptions appeared more frequently than identity-related or trust-related concerns. Similarly, early examination of economic variables indicated that legal costs and long-term financial burdens were among the most commonly recurring financial consequences.


Regional exploration further showed that case records were concentrated more heavily within Africa, North America, and Europe, suggesting differences in legal reporting systems, public data accessibility, research availability, and documentation practices across regions.


The preliminary exploration also identified several data quality issues that required additional preprocessing attention, including inconsistent country naming conventions, duplicate case records, missing values within psychological and financial variables, and inconsistent legal terminology across international sources. These findings guided the selection of KPI measures, dashboard visualizations, DAX calculations, and comparative analyses implemented during the main analytical phase.





In-Analysis

The in-analysis phase focused on detailed exploration, calculation, visualization, and interpretation of the transformed datasets using Microsoft Power BI. The analysis combined dashboard visualizations, DAX calculations, KPI generation, and comparative regional evaluation to uncover key insights relating to legal protection, DNA accessibility, financial severity, and psychological effects associated with paternity fraud.


Key Performance Indicators (KPIs)
The following KPI cards were generated from the master dataset to provide a high-level summary of the project's analytical scope:


<img width="966" height="240" alt="KPI" src="https://github.com/user-attachments/assets/1346416a-7b87-49c6-9a96-8ffd1b4e608c" />


The Average Legal Strength Score of 1.93 out of a maximum of 4 indicates that globally, most countries fall within the Medium legal protection range, with significant room for improvement in legal frameworks specifically addressing paternity fraud.



Regional Case Distribution
The dataset revealed significant regional disparities in documented paternity fraud cases. Africa recorded the highest concentration of cases, driven predominantly by Nigeria which alone accounted for 750 of the 1,284 total records (58.4%).



<img width="1013" height="837" alt="Sce  1" src="https://github.com/user-attachments/assets/713669f4-eb43-4ff3-aeea-5aebc36f3a43" />



Discovery Method Analysis

Analysis of the discovery method distribution revealed that DNA testing is the dominant mechanism through which paternity fraud cases are uncovered globally, reinforcing the critical importance of accessible and regulated DNA testing infrastructure.


<img width="973" height="334" alt="Sce  2" src="https://github.com/user-attachments/assets/cf571e13-6884-45ad-9a46-5e107bd033fe" />



Legal Strength and Protection Level Analysis

The legal protection level distribution demonstrated that the majority of countries in the dataset operate with medium legal protections. Only 4.1% of records were associated with countries that have High legal protection levels, highlighting that comprehensive legal frameworks for paternity fraud remain rare globally.


<img width="982" height="449" alt="legal" src="https://github.com/user-attachments/assets/3177cefe-aed1-477a-9c16-b8796540011d" />



Nigeria recorded the highest cumulative legal strength score across the dataset, followed by the United States and the United Kingdom. The table below presents the country-level breakdown:


<img width="963" height="671" alt="legal-2" src="https://github.com/user-attachments/assets/e8d19b90-1213-4fb0-9447-ad2f1c40ad04" />



Financial Severity Assessment

The financial severity analysis revealed that the economic consequences of paternity fraud are overwhelmingly severe, with high financial impact cases dominating the dataset at 83.8%. This reflects the substantial burden of wrongful child support obligations, legal expenses, and reimbursement disputes associated with paternity fraud cases.


<img width="979" height="448" alt="fin-sev" src="https://github.com/user-attachments/assets/4a5d54c9-bc3b-4c76-8313-e9a0cb768d3a" />



DNA Accessibility Distribution

Medium DNA accessibility levels dominated across the dataset at 87.4%. No records were classified as Low DNA accessibility, which likely represents a data gap rather than the absence of low-access regions, as many countries with limited DNA testing infrastructure may simply be underrepresented in the available secondary data.


<img width="986" height="457" alt="DNA" src="https://github.com/user-attachments/assets/463437e3-bc2e-4576-8236-32fa10a4a2b9" />



Psychological Impact Analysis

Trauma emerged as the most frequently documented psychological effect, recorded in 526 cases (41.0%). This finding reinforces that the impact of paternity fraud extends well beyond legal and financial dimensions into serious emotional and family welfare consequences.


<img width="1072" height="717" alt="psycho" src="https://github.com/user-attachments/assets/b07863c2-ff1c-4767-8a07-99a65db10624" />



Challenge Window Distribution

The legal challenge window analysis showed that 96.3% of records (1,236) were associated with Flexible challenge systems, suggesting that most documented legal systems allow relatively open-ended periods for challenging paternity claims. Only 17 records (1.3%) were associated with Strict challenge windows, indicating that rigid legal timeframes for paternity disputes are uncommon across the dataset.



DAX Functions Used for Analysis
Data Analysis Expressions (DAX) functions were implemented extensively within Microsoft Power BI to generate dynamic calculations, KPI indicators, filtering logic, and percentage-based insights for the dashboard. The DAX measures were prepared by Eniola Adelakun and applied across KPI cards, bar charts, column charts, donut charts, geographic maps, and regional comparison visuals.



<img width="1020" height="779" alt="legal prot" src="https://github.com/user-attachments/assets/57991937-e643-4d27-9e7e-a2ae4fd8ec38" />

<img width="987" height="163" alt="legal-prot -2" src="https://github.com/user-attachments/assets/842c7755-3ec6-4d64-b183-9ed134b3710f" />



The TRIM() and UPPER() functions were also applied within FILTER() expressions to standardize text values before comparison, ensuring accurate filtering regardless of text case or whitespace inconsistencies in the dataset. This was particularly important given that the dataset was compiled from multiple sources with varying formatting conventions. 





Post-Analysis and Insights 

The post-analysis phase focused on interpreting the final analytical outcomes generated from the dashboard visualizations, DAX calculations, and comparative regional analysis. The analysis confirmed that paternity fraud represents a multidimensional issue involving legal, psychological, financial, and institutional challenges across different countries and regions. 

One of the most significant findings was the dominance of DNA testing as the primary discovery method, present in 55.5% of all documented cases. This highlights the growing importance of scientific verification systems in legal and family-related disputes globally. 

The analysis also revealed substantial disparities in legal protection systems. While countries like the United Kingdom demonstrated High legal protection levels, the majority of records (60.4%) fell into the Medium protection category, and 35.5% were associated with Low protection frameworks, indicating that comprehensive legal structures specifically addressing paternity fraud remain far from universal. 

Psychological trauma emerged as the most commonly documented emotional consequence at 41.0% of cases, reinforcing that the issue extends beyond legal and financial dimensions into broader family and social welfare concerns. From an economic perspective, 83.8% of cases were classified as High financial severity, demonstrating the substantial and recurring economic burden associated with paternity fraud. 

The geographical mapping of the dataset further demonstrated that paternity fraud-related records and legal disputes are globally distributed across Africa, Europe, North America, Asia, and South America, reinforcing the international relevance of the issue. However, the concentration of records in Nigeria (58.4%) should be interpreted alongside the acknowledged data availability limitations for other regions. 

Overall, the project successfully transformed fragmented legal, demographic, and case-related information into structured analytical insights capable of supporting policy discussions, legal awareness, and future research initiatives. 




Value to the Industry 
The findings provide valuable insights into global legal disparities, DNA testing accessibility, and the social and economic consequences associated with paternity fraud. The analysis may assist stakeholders in: 

. Identifying weaknesses in existing legal frameworks 

. Improving DNA testing accessibility and regulation 

. Enhancing family welfare and psychological support systems 

. Supporting evidence-based policymaking

. Increasing public awareness of the legal and psychological impacts of paternity fraud 
Guiding future academic and institutional research in this under-studied area 





Observations and Recommendations 

The following observations were derived from the dashboard analysis, KPI findings, and comparative regional evaluation. Each observation is paired with a targeted recommendation for legal, policy, and social welfare stakeholders.


<img width="968" height="286" alt="obs -rec" src="https://github.com/user-attachments/assets/ee6f32a3-329b-4261-a337-2765e4cc9a56" />

<img width="996" height="836" alt="obs -rec -2" src="https://github.com/user-attachments/assets/9a523628-a33e-48f7-8aba-6c60edf7407c" />

<img width="983" height="468" alt="obs -rec -3" src="https://github.com/user-attachments/assets/4cce0d72-0300-476b-982b-2fb057b3cdc2" />

<img width="995" height="790" alt="obs -rec -4" src="https://github.com/user-attachments/assets/dd46d418-011c-4cd3-a967-0a0643063088" />

<img width="1006" height="534" alt="obs -rec -5" src="https://github.com/user-attachments/assets/11859e98-4854-464b-bbb5-76d0e16e3d42" />

<img width="974" height="276" alt="obs -rec -6" src="https://github.com/user-attachments/assets/885988c1-2758-4348-b743-c224911ccd25" />






Conclusion 

The Global Paternity Fraud Analysis project provided significant insights into the legal, psychological, financial, and institutional dimensions of paternity fraud across different countries and regions. Through the integration of multiple secondary datasets and the application of data analytics techniques in Microsoft Excel and Microsoft Power BI, the project successfully transformed fragmented global information into structured and interpretable analytical findings. 

The most significant finding was that DNA testing remains the dominant method for discovering paternity fraud, present in 55.5% of all documented cases. Substantial disparities in legal protection systems were identified, with only 4.1% of records associated with countries having High legal protection levels. Psychological trauma was the most frequently documented emotional consequence, and 83.8% of cases involved High financial severity, underscoring the broad and serious impact of paternity fraud on affected individuals and families. 

The project further demonstrated the value of data analytics and interactive dashboard visualization in simplifying complex legal and social datasets into actionable insights capable of supporting policy discussions, academic research, and stakeholder decision-making. 



Future Research 

Expansion of Global Data Collection: Future studies may benefit from broader international collaboration and the development of centralized global reporting systems dedicated to paternity fraud statistics and legal outcomes.

Inclusion of Primary Data: Conducting surveys, interviews, or case-based qualitative studies may provide deeper insight into the emotional, social, and family-related consequences of paternity fraud. 

Advanced Predictive Analytics: Future research could incorporate predictive analytics or machine learning models to identify patterns and risk factors associated with paternity fraud cases. 

Comparative Legal Policy Studies: Further analysis comparing the effectiveness of legal systems and DNA regulations across countries may support stronger international legal standards. 

Child Welfare and Long-Term Social Impact Studies: Additional research may explore the long-term effects of paternity fraud on children, family relationships, and identity development. 

Improved Data Standardization: Future projects may benefit from more standardized global terminology, reporting structures, and legal classifications to improve consistency in cross-country analysis. 






References 

Institutional and Public Data Sources 

AABB Annual Paternity Testing Reports

World Health Organization (WHO) datasets 

UNICEF birth registration and legal parenthood datasets 

Pew Research Center demographic and family structure reports 

GDELT Project global event datasets 

National court records and legal databases 


Academic and Research Sources 

Google Scholar publications 

JSTOR academic journals 

HeinOnline legal research database \

Family law textbooks and legal publications 

Peer-reviewed journal articles relating to paternity fraud, DNA testing, and family law 


Software and Analytical Tools

Microsoft Excel (Power Query Editor) 

Microsoft Power BI 

Data Analysis Expressions (DAX) Vephla University


