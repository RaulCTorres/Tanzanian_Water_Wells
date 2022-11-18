# Tanzanian Water Wells Analysis

**Authors**: Juan Acosta, Drew Holcombe, Raul Torres

## Overview

Tanzania is one of many countries facing water shortages in the face of climate change. In our dataset, provided by Taarifa and the Tanzanian Ministry of Water via DrivenData's competition "Pump it Up: Data Mining the Water Table," nearly half of the wells we studied are non-functional or in need of repair, which leaves countless people and families without reliable water access. We achieved an 85% accurate model which predicts which wells are functional, non-functional, and in need of repair. The most important features included Water Quantity, Extraction Type, and Payment Type: by accessing waterpoints with ample available water, well-documented and established extraction types, and requiring payment from users, we believe the Tanzania Water Fund can construct new wells with the best chance of lasting success.

## Business Problem

As with any nonprofit, the Tanzania Water Fund has finite resources to fulfill their objective of bring clean water to the people of Tanzania; when attempting to provide reliable water access, it is imperitive that new wells stay functional. As identifying the functionality of currently existing wells is rather apparent, we aimed to look to the future and optimize future construction: what factors would result in high-functioning wells? This would allow the organization's resources to be efficiently allocated and establish the most reliable water access possible.

Our model utilized nine contributing variables from a dataset of 59,400 rows, each representing a single well. These features are:

## Methods

We iterated through a series of decision trees and random forest models in order to correct the overfitting we initially ran into. Our final model is a random forest, with hyperparameters optimized through a series of gridsearches, which achieved an accuracy rating of 85%.

## Results

Our final model has an accuracy of roughly 85%; we chose to focus on accuracy becuase we were equally concerned in identfying all three classes of wells (functional, non-functional, and needing repairs). Our final model greatly outperformed the baseline model (54% compared to 85%), giving great insight into what features are shared by successful wells throughout Tanzania. We are very confident this will help the Tanzania Water Fund to focus on strategies that will make their work as successful as possible.

## Feature Importance 

![Feature Importance](https://github.com/RaulCTorres/Tanzanian_Water_Wells/blob/main/Images/FEATURE_IMPORTANCE-not-transparent.png)
## Extraction Types

![Extraction Types](https://github.com/RaulCTorres/Tanzanian_Water_Wells/blob/main/Images/extraction_type.png)
## Payment Types

![Payment Types](https://github.com/RaulCTorres/Tanzanian_Water_Wells/blob/main/Images/payment.png)

## Conclusions

Based on our findings, we reccommend that Tanzania focus on continued use of well-established extraction types (gravity, nira/tanira, submersible, and SWN 80), choose waterpoints with an ample water supply when possible, and initiate payment plans for users of future wells. By doing so, we hope these well will remain functional for as long as possible.

Our model does not cover some metrics where data was too incomplete or poorly-defined that might also be contributing factors, such as elevation, installers/funders, and management. As these are likely to contribute to the performance of these wells, we would like to perform further analysis on these factors in the future we were not able to address in the time we had. We'd also like to interact with the creators of the dataset in order to define terminology used that we were not able to investigate, such as public_meeting and num_private.

In the future, we would also like to investigate the role of seasons and weather in the operation of wells (perhaps based on date of evaluation) and precise location through the provided latitude/longitude coordinates. Provided more time and resources, we would love to dig deeper into this issue and mine more useful information from the source of the data.

Please review our full analysis in our [Jupyter Notebook](https://github.com/RaulCTorres/Tanzanian_Water_Wells/blob/main/Tanzanian%20Water%20Wells%20Analysis.ipynb) or our [presentation](https://github.com/RaulCTorres/Tanzanian_Water_Wells/blob/main/water_well_presentation.pdf).

## For More Information

For any additional questions, please contact Juan Acosta at jmaa3108@gmail.com, Drew Holcombe at drew.holcombe7@gmail.com, or Raul Torres at cassielponce@icloud.com.

# Repository Structure

```
├── README.md                                    <- The top-level README for reviewers of this project
├── Tanzanian Water Wells Analysis.ipynb         <- Narrative documentation of analysis in Jupyter notebook
├── water_well_presentation.pdf                  <- PDF version of project presentation
├── data                                         <- Dataframes used in modelling process 
├── Images                                       <- Visuals generated from code
└── Scratch_code                                 <- Working jupyter notebooks containing scratch work                     
```
