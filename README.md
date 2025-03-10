# RADOR-KY data sharing

## Twitter 2019 and 2020
* [`kentucky_df_2019.csv`](): mental health scores measured from 2019 Twitter data
* [`kentucky_df_2020.csv`](): mental health scores measured from 2020 Twitter data 
* [`kentucky_df_2020_diff.csv`](): mental health scores measured from 2020 Twitter data *controlling for 2019 scores*

**Measures**:
  *  `anx_score`: Anxiety predictions
  * `dep_score`: Depression predictions
 


## Twitter: 2021 and 2022
* [`kentucky_df_2021.csv`](): mental health & opioid prediction scores measured from 2021 Twitter data
* [`kentucky_df_2022.csv`](): mental health & opioid prediction scores measured from 2022 Twitter data
  
**Measures**:
- `anx_score`: Anxiety predictions 
- `dep_score`: Depression predictions 
- `opioid_cr_clipped`: Crude rate opioid mortality clipped to 0 
- `opioid_cr_raww`: Crude rate opioid mortality raw
- `opioid_aar`: Age-adjusted opioid mortality


## Measure Descriptions: 

* <ins>Language-Based Mental Health Assessments</ins>: "County-mapped messages are filtered to self-written posts, from which language features are extracted and passed through pretrained language-based mental health assessments to generate user scores. These scores are then reweighted to better represent county demographics and are then aggregated to communities in time." ([Mangalik, S., Eichstaedt, J.C., Giorgi, S. et al., 2024](https://www.nature.com/articles/s41746-024-01100-0))
  * `anx_score`: Anxiety predictions aggregated to the county-week level
  * `dep_score`: Depression predictions aggregated to the county-week level
 
* <ins>Opioid Poisoning Mortality</ins>: County-mapped Twitter messages from 2021 and 2022 are used to estimate opioid poisoning mortality rates from a pretrained model predicting opioid poisoning mortality ([Giorgi, S., Yaden, D.B., Eichstaedt, J.C. et al., 2023](https://www.nature.com/articles/s41598-023-34468-2))
  * `opioid_cr_clipped`: Crude rate opiate-related deaths per 100,000 people, with negative rates set (clipped) to 0
  * `opioid_cr_raw`: Crude rate opiate-related deaths per 100,000 people
  * `opioid_aar`: Age-adjusted opiate-related deaths per 100,000 people



## Sources

* *[Robust language-based mental health assessments in time and space through social media
](https://www.nature.com/articles/s41746-024-01100-0)*
* *[Predicting U.S. county opioid poisoning mortality from multi-modal social media and psychological self-report data
](https://www.nature.com/articles/s41598-023-34468-2)*
