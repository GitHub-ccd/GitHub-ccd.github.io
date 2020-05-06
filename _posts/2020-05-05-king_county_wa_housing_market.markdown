---
layout: post
title:      "King County WA housing market"
date:       2020-05-05 21:46:40 -0400
permalink:  king_county_wa_housing_market
---

1. ***What features are given in the dataset***
Before start modeling it's important to research about the features given in the dataset and what they mean. I've found a list of features and explaination given for the king county dataset. Those are given below. 


*     **id** - ID for each house sold
*     **date** - date house sold
*     **price** - price of home. is prediction target
*     **bedrooms** - of Bedrooms/House
*     **bathrooms** - of bathrooms/bedrooms, where 0.5 account for room with a toilet but no shower
*     **sqft_living** - footage of the living area
*     **sqft_lot** - footage of the land space
*     **floors** - floors (levels) in house
*     **waterfront** - dummy variable House which has a view to a waterfront
*     **view** - index of 0-4 of how good the view of the property
*     **condition** - index of 1-5 how good the condition is ( Overall )
*     **grade** - index of 1-13 King County grading system.

               1-3 falls short of construction and design, 
               4-10 or 7 is average,
               11-13 is high quality. 

*     **sqft_above** - total footage above ground
*     **sqft_basement** - square footage of the basement
*     **yr_built** - Built Year
*     **yr_renovated** - Year last renovated
*     **zipcode** - zipcode
*     **lat** - Latitude coordinate
*     **long** - Longitude coordinate
*     **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
*     **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors



2. ***Cleaning data***
There data were relatively clean. yr_renovated column had to be dropped because 78% of the data was missing. Missing data of couple of other columns were replaced by median or zero. One column had a tag '?', probably to indicate that the data is missing. This was readily identified when trying to plot the data. For numerical features this maybe a good method to check for data inconsitancies. 

Initially, distribution of the 'Price', which is the target feature were checked. It appeared less than 1% of the houses were more than $2,000,000. Thus, it was decided to remove those data that has extremely high price houses to reduce the complexcity of the dataset.  

Then all the features were checked individually for outliers. Outliers were found on bedrooms column. Histograms and seborn joint plots are excellent to check distributions of all reafures rather quickly. Following is the code for jointplots. 
```
tmp_df=df.drop(['id', 'date'], axis=1)
headers=tmp_df.columns

#once again just iterating through our list of columns so that we get each separate plot
for column in headers:
    sns.jointplot(x=column, y="price", 
                  data=tmp_df, #
                  kind='reg', 
                  label=column, 
                  joint_kws={'line_kws':{'color':'blue'}}) #stylistic choices

    plt.legend() #including a legend for our plots
    
    plt.show()
```



3.  ***Exploring features and modeling***

4.  ***Feature selection and model validation***
5.  ***Model analysis and drawing conclusions***
