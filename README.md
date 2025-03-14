# RADOR-KY data sharing

### [Data Sharing Presentation: Methods and Data Overview](https://docs.google.com/presentation/d/1RYaRZhjkd9He2rbrLLZYkieGva-xxx8D4fwn722n_jc/edit?usp=sharing)

## Twitter 2019 and 2020
* [`kentucky_df_2019.csv`](https://github.com/CompPsychology/rador-ky-data/blob/main/kentucky_df_2019.csv): mental health scores measured from 2019 Twitter data
* [`kentucky_df_2020.csv`](https://github.com/CompPsychology/rador-ky-data/blob/main/kentucky_df_2020.csv): mental health scores measured from 2020 Twitter data 
* [`kentucky_df_2020_diff.csv`](https://github.com/CompPsychology/rador-ky-data/blob/main/kentucky_df_2020_diff.csv): mental health scores measured from 2020 Twitter data *controlling for 2019 scores*

**Measures**:
  *  `anx_score`: Anxiety predictions
  * `dep_score`: Depression predictions
 


## Twitter: 2021 and 2022
* [`kentucky_df_2021.csv`](https://github.com/CompPsychology/rador-ky-data/blob/main/kentucky_df_2021.csv): mental health & opioid prediction scores measured from 2021 Twitter data
* [`kentucky_df_2022.csv`](https://github.com/CompPsychology/rador-ky-data/blob/main/kentucky_df_2022.csv): mental health & opioid prediction scores measured from 2022 Twitter data
  
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
 
* <ins>Opioid Poisoning Mortality</ins>: County-mapped Tweets from 2021 and 2022 are used to estimate opioid poisoning mortality rates from a pretrained model predicting opioid poisoning mortality ([Giorgi, S., Yaden, D.B., Eichstaedt, J.C. et al., 2023](https://www.nature.com/articles/s41598-023-34468-2))
  * `opioid_cr_clipped`: Crude rate opiate-related deaths per 100,000 people, with negative rates set (clipped) to 0
  * `opioid_cr_raw`: Crude rate opiate-related deaths per 100,000 people
  * `opioid_aar`: Age-adjusted opiate-related deaths per 100,000 people


## Open Questions
- Linear rescaling of opioid mortality rates (adjust means of estimates to match true means)?
- Should `denominator` for estimated opioid death rates be 1 or 100,000, as the measurement is "deaths per 100,000 individuals"?
- Fill county-weeks that have no prediction due to thresholding with Null?

