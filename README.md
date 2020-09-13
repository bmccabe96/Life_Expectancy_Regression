# Life_Expectancy_Regression 

This project presents an analysis of life expectancy using a dataset containing heatlh data collected from World Health Organization (WHO) and economic data collected from the Unite Nations (UN). This data was compiled by Kumar Rajarshi and posted to [Kaggle](https://www.kaggle.com/kumarajarshi/life-expectancy-who). We (Brian McCabe and Italo Calderon) attempt to conduct a regression analysis to give insight to country leaders on how to increase the life expectancy of their populace.

In this repository there are three notebooks:
  * **life_expectancy_cleaning**: This notebook details the data cleaning process.
  * **life_expectancy_eda**: This notebook contains our initial data exploration and hypothesis tests that informed our creation of our regression. 
  * **regression_model**: This notebook walks through our regression analysis, including the training process for 7 models.

#  EDA and Visualization 

These can be found in the life_expectancy_eda notebook. 

# Models

In the creation of our models, we decided to leave out country name, year, and country status ('developing' vs 'developed') since we wanted to focus on features that can *actually by changed* by a government to affect the life expectancy of their populace. We ran seven models: two without feature engineering and five with engineering polynomial and interaction features. Our best model returned an R-squared value of 0.90 and inlcuded ploynomial and interaction features selected using VIF score. This came at the expense of interpretability. We decided to use a simpler model with more targeted feature engineering that allowed for better interpretability. Our final model returned an R-squared of 0.84. Further details can be found in the regression_model notebook.

# Key Features

We identified three key features with an effect on our model:

  * **Schooling**: We found that each additional year of schooling adds 0.78 years to one's life expectancy.
  * **Income Composition of Resources (ICR)**: Also referred to as Human Development Index, it incorporates three main ideas: (1) income per capita, (2) education, and (3) life expectancy. While our schooling feature accounts for the second point, our tests showed that they are both significant enough to include in our final model. Increasing ICR by one point adds 6.7 years to one's life expectancy. We can begin to see that increasing access to schooling can affect ICR and, in turn, affect life expectancy.
  * **Incidence of HIV/AIDs**: Incidence of HIV/AIDS in a country had the strongest negative affect on life expectancy. With each incidence of HIV/AIDS, life expectancy decreases by 4.2 years. 
  
# Conclusion








