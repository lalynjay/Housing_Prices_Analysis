# Predicting Housing Prices using Linear Regression

### Lynn Anderson

# Overview

The objective of this project was to create a multiple linear regression model to demonstrate how certain characteristics impact the value of a house in King County, WA. Simple linear regression finds the best fitting linear equation using only one explanatory variable, whereas multiple linear regression aims to find a more complex linear combination of independent variables that most closely fits the data. Multiple linear regression was used quantify the relative importance of each independent variable in predicting the value of a target variable. For this project, the target variable was sale price of the house. 

# Business Understanding

A rental company in King County, WA has acquired some houses in the area. They are looking to renovate some of the homes before renting them out, and would like to know which ones would be best to start with, and how they can increase the value of those homes. I am going to identify two features that have the most influence the value of homes in the area, and make recommendations on what the company should prioritize when remodeling their houses. I chose to investigate variables that would be more practical to alter in a home renovation- while factors such as being adjacent to a waterfront or greenbelt are likely to increase home value, it is not feasable to alter those characteristics for a house in a given location without major urban planning.

![map](https://github.com/lalynjay/Housing_Prices_Analysis/blob/alt/images/king_co.png)


# Data


Data was sourced from the King County Housing Sales Dataset, which consisted of 30,155 total records for home sales in King County, WA. The data inlcudes the prices of houses sold in 2021 and 2022 and relevant features which may impact the value of a home. After null values, duplicate entries, and outliers with regards to sale price were removed, 28,120 records were used in the modeling process. The mean sale price was $940k and the median was $830k.  

![hist](https://github.com/lalynjay/Housing_Prices_Analysis/blob/alt/images/price_hist.png)


# Modeling

A baseline simple linear regression model with living room size as the sole independent variable was looked at first. Other iterations investigated making log transformations to the data, yet that resulted in poorer performing models. Grade, condition, patio size, number of bathrooms and floors were added to subsequent models, with regression coefficients and error metrics then analyzed to determine how well the model performed.

# Results and Conclusions

Considering the results of all models analyzed in this project, I consider the model that includes living room size, grade, and condition as the independent variables to be the best model. The r-squared value of 0.395, MAE of $244,000, and RMSE of $338,000 was hardly improved upon when more independent variables were added. Even the model including many independent variables, some that were moderately to highly correlated with each other, reduced error metrics by less than 0.5%. Thus, the model icluding living room size, grade, and condition most succinctly explained the variation in sale price. I will base my reccomendations off of that model. 

In my selected model, a home with a grade of 8, or 'good' was associated with a $151,000 increase in price as compared with an average grade (grade 7) house. Sale price for homes in good condition was $76,660 above that of an average house, and those in very good condition sold for $150,000 more. Finally, for each increase of squarefoot living room, there was an associated $190 increase in price.
![lvg_room](https://github.com/lalynjay/Housing_Prices_Analysis/blob/alt/images/lvg.png)
![grade](https://github.com/lalynjay/Housing_Prices_Analysis/blob/alt/images/grade.png)



# Reccomendations

Based on the results of the analysis, my recommendations for a rental company looking to renovate homes are to:

Enlarge the living room. Living room size had the highest correlation with sale price, more so than even the size of the house. A spacious living room will likely enhance the value of the home and appeal to prospective renters by providing a sense of comfort and community.

Use high quality materials and pay attention to design qualty. For example, tile flooring in the bathrooms, good quality hardwood or bamboo in the interior, exterior, and flooring, and ceramic countertops can greatly add to the quality. In addition, a solid concrete foundation will ensure the house is sturdy- however, the use of concrete in building materials should be limited. The use of plastics should also be avoided.

Ensure any underlying issues or problems with the house structure or design are addressed. As demonstrated by the model, a house in good or great condition was valued significantly higher. Take care to ensure any rennovations address any wear and tear and improve the overall condition of the house.


# Limitations and Next steps

More research should be done to determine the specific styles, designs, and materials associated with an increase in home value. In addition, it would also be worth investigating if there are different factors in different locations- ie does a specific feature for a home in Seattle affect home value more so than in outlying areas?

Because outliers were removed, extremely high priced mansion grade homes were left out. Thus, these models may not accurately reflect how best to increase the value of a mansion. However, since mansions are already valued way above average homes, it is unlikely to be worth the cost to renovate them. 

# For More Information

See the full analysis in the [Jupyter Notebook](https://github.com/lalynjay/Housing_Prices_Analysis/blob/alt/Housing_Prices_Analysis.ipynb) or review [this presentation](https://github.com/lalynjay/Housing_Prices_Analysis/blob/alt/Housing_Prices_presentation.pdf)

For additional info, contact Lynn Anderson at lalynjay@gmail.com

Repository Structure

├── data

├── images

├── README.md

├── Presentation.pdf

└── Housing_Prices_analysis.ipynb
