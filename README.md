# Life_Expectancy_Regression 

This project presents an analysis of life expectancy using a dataset containing heatlh data collected from World Health Organization (WHO) and economic data collected from the Unite Nations (UN). This data was compiled by Kumar Rajarshi and posted to [Kaggle](https://www.kaggle.com/kumarajarshi/life-expectancy-who). We (Brian McCabe and Italo Calderon) attempt to conduct a regression analysis to give insight to country leaders on how to increase the life expectancy of their populace.

In this repository there are three notebooks:
  * **life_expectancy_cleaning**: This notebook details the data cleaning process.
  * **life_expectancy_eda**: This notebook contains our initial data exploration and hypothesis tests that informed our creation of our regression. 
  * **regression_model**: This notebook walks through our regression analysis, including the training process for 7 models.

#  EDA and Visualization 

![Image](life_expect_by_status.png?raw=true)

# Models

In the creation of our models, we decided to leave out country name, year, and country status ('developing' vs 'developed') since we wanted to focus on features that can *actually by changed* by a government to affect the life expectancy of their populace. We ran seven models: two without feature engineering and five with engineering polynomial and interaction features. Our best model returned an R-squared value of 0.90 and inlcuded ploynomial and interaction features selected using VIF score. This came at the expense of interpretability. We decided to use a simpler model with more targeted feature engineering that allowed for better interpretability. Our final model returned an R-squared of 0.84. Further details can be found in the regression_model notebook.

# Key Features

We identified three key features with an effect on our model:

  * **Schooling**: We found that a one standard deviation increase in years of schooling adds 0.78 years to one's life expectancy.
  * **Income Composition of Resources (ICR)**: Also referred to as Human Development Index, it incorporates three main ideas: (1) income per capita, (2) education, and (3) life expectancy. While our schooling feature accounts for the second point, our tests showed that they are both significant enough to include in our final model. Increasing ICR by one standard deviation adds 6.7 years to one's life expectancy. We can begin to see that increasing access to schooling can affect ICR and, in turn, affect life expectancy.
  * **Incidence of HIV/AIDS**: Incidence of HIV/AIDS in a country had the strongest negative effect on life expectancy. With a one standard deviation increase in incidence of HIV/AIDS, life expectancy decreases by 4.2 years. 
  
# Conclusion

Based on our model, country leaders should focus their efforts on the following:

  * **Increase access to schooling.** Our model shows that access to education is connected to the two strongest predictors of life expectancy. Therefore, increase access to education can positively affect ICR and Incidence of HIV/AIDS. For instance, increasing schooling may lead to higher income for the population which in turn will inflate the ICR score of a country. Further, educating the population on safer sex practices will reduce the incidence of HIV/AIDS and increase life expectancy. 
  * **Increase income per capita.** Our strongest positive predictor of life expectancy was ICR which includes a measure of income per capita and schooling. Not only is it important to increase access to schooling for the reasons stated above, but focus on increasing income per capita. This can be done a number of way, including increasing the minimum wage, creating new jobs, and/or instating universal basic income. 
  * **Decrease Incidence of HIV/AIDS.** This can be done through educating the populace on the risks of unsafe sex (STIs) and HIV/AIDS prevention (condoms, injection drug use, e.g.). As well as, increase access to these. 






