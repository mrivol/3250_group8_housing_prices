# What Impacts Our House Prices?

## Project Description

It's a goal for many people across to world to eventually atain home ownership. People may think of the size of their kitchen and living room or how recently their home was built to value their home. In reality, there are many factors that don't come intuitively to mind that can play a role in determining the sale value of a house. For example, would you have considered the flatness of the grounds, or the direction of the nearest railway? 

This project seeks to analyze a dataset of 80 variables over 1000+ homes to understand how best to predict the value of other homes. This is a small sample, with a relatively small number of features but serves as a an effective example of how to predict the value of homes in any given area of the world where structured data is available on home sales. 

**Project Goal:** Using a given dataset of home sale prices and 80 descriptive features of each home, predict the value of other homes given similar characteristics.

## Group Members
 - Matthias Rivollier
 - Sora Jang
 - Krishna Nuthi
 - Pragya Vaid
 - Roya Sani

## Data

A dataset originating from Kaggle is used in this excercise. It can be found [here](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data). The data is already split into train and test populations. More information on the features found within the dataset is available here:

    MSSubClass: Identifies the type of dwelling involved in the sale.	
    MSZoning: Identifies the general zoning classification of the sale.
    LotFrontage: Linear feet of street connected to property
    LotArea: Lot size in square feet
    Street: Type of road access to property
    Alley: Type of alley access to property
    LotShape: General shape of property
    LandContour: Flatness of the property
    Utilities: Type of utilities available
    LotConfig: Lot configuration
    LandSlope: Slope of property
    Neighborhood: Physical locations within Ames city limits
    Condition1: Proximity to various conditions
    Condition2: Proximity to various conditions (if more than one is present)
    BldgType: Type of dwelling
    HouseStyle: Style of dwelling
    OverallQual: Rates the overall material and finish of the house
    OverallCond: Rates the overall condition of the house
    YearBuilt: Original construction date
    YearRemodAdd: Remodel date (same as construction date if no remodeling or additions)
    RoofStyle: Type of roof
    RoofMatl: Roof material
    Exterior1st: Exterior covering on house
    Exterior2nd: Exterior covering on house (if more than one material)
    MasVnrType: Masonry veneer type
    MasVnrArea: Masonry veneer area in square feet
    ExterQual: Evaluates the quality of the material on the exterior 
    ExterCond: Evaluates the present condition of the material on the exterior
    Foundation: Type of foundation
    BsmtQual: Evaluates the height of the basement
    BsmtCond: Evaluates the general condition of the basement
    BsmtExposure: Refers to walkout or garden level walls
    BsmtFinType1: Rating of basement finished area
    BsmtFinSF1: Type 1 finished square feet
    BsmtFinType2: Rating of basement finished area (if multiple types)
    BsmtFinSF2: Type 2 finished square feet
    BsmtUnfSF: Unfinished square feet of basement area
    TotalBsmtSF: Total square feet of basement area
    Heating: Type of heating
    HeatingQC: Heating quality and condition
    CentralAir: Central air conditioning
    Electrical: Electrical system
    1stFlrSF: First Floor square feet
    2ndFlrSF: Second floor square feet
    LowQualFinSF: Low quality finished square feet (all floors)
    GrLivArea: Above grade (ground) living area square feet
    BsmtFullBath: Basement full bathrooms
    BsmtHalfBath: Basement half bathrooms
    FullBath: Full bathrooms above grade
    HalfBath: Half baths above grade
    Bedroom: Bedrooms above grade (does NOT include basement bedrooms)
    Kitchen: Kitchens above grade
    KitchenQual: Kitchen quality
    TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)
    Functional: Home functionality (Assume typical unless deductions are warranted)
    Fireplaces: Number of fireplaces
    FireplaceQu: Fireplace quality
    GarageType: Garage location
    GarageYrBlt: Year garage was built
    GarageFinish: Interior finish of the garage
    GarageCars: Size of garage in car capacity
    GarageArea: Size of garage in square feet
    GarageQual: Garage quality
    GarageCond: Garage condition
    PavedDrive: Paved driveway
    WoodDeckSF: Wood deck area in square feet
    OpenPorchSF: Open porch area in square feet
    EnclosedPorch: Enclosed porch area in square feet
    3SsnPorch: Three season porch area in square feet
    ScreenPorch: Screen porch area in square feet
    PoolArea: Pool area in square feet
    PoolQC: Pool quality
    Fence: Fence quality
    MiscFeature: Miscellaneous feature not covered in other categories
    MiscVal: $Value of miscellaneous feature
    MoSold: Month Sold (MM)
    YrSold: Year Sold (YYYY)
    SaleType: Type of sale
    SaleCondition: Condition of sale

# Feature Engineering & Selection

We have created a video below, explaining our procedure for the project as a whole:

[![](http://img.youtube.com/vi/UDd6lqeEHgM/0.jpg)](http://www.youtube.com/watch?v=UDd6lqeEHgM "Housing Project Presentation")

For the feature selection, some of the statistical signficance figures can be found below:

Statistical Significance of comparison of means: 
1. average sales price of C (all) and FV

        **Results**
        Difference	139486.000
        Standard error	17136.897
        95% CI	105332.2140 to 173639.7860
        t-statistic 	8.140
        DF 	73
        Significance level	P < 0.0001

2. average sales price of C (all) and RH

        **Results**
        Difference	57030.000
        Standard error	14111.070
        95% CI	27906.1827 to 86153.8173
        t-statistic 	4.042
        DF 	24
        Significance level	P = 0.0005

3. average sales price of C (all) and RL

        **Results**
        Difference	116476.000
        Standard error	25568.867
        95% CI	66309.5519 to 166642.4481
        t-statistic 	4.555
        DF 	1159
        Significance level	P < 0.0001

4. average sales price of C (all) and RM

        **Results**
        Difference	51788.000
        Standard error	15529.919
        95% CI	21186.0426 to 82389.9574
        t-statistic 	3.335
        DF 	226
        Significance level	P = 0.0010

5. average sales price of FV and RM

        **Results**
        Difference	-87698.000
        Standard error	6984.642
        95% CI	-101446.8628 to -73949.1372
        t-statistic 	-12.556
        DF 	281
        Significance level	P < 0.0001

6. average sales price of FV and RH

        **Results**
        Difference	-82456.000
        Standard error	13852.973
        95% CI	-110029.6528 to -54882.3472
        t-statistic 	-5.952
        DF 	79
        Significance level	P < 0.0001

7. average sales price of FV and RL

        **Results**
        Difference	-23010.000
        Standard error	10138.246
        95% CI	-42900.4274 to -3119.5726
        t-statistic 	-2.270
        DF 	1214
        Significance level	P = 0.0234

8. average sales price of RH and RL

        **Results**
        Difference	59446.000
        Standard error	20225.787
        95% CI	19762.9592 to 99129.0408
        t-statistic 	2.939
        DF 	1165
        Significance level	P = 0.0034

9. average sales price of RH and RM

        **Results**
        Difference	-5242.000
        Standard error	12379.949
        95% CI	-29633.4941 to 19149.4941
        t-statistic 	-0.423
        DF 	232
        Significance level	P = 0.6724

10. average sales price of RL and RM

        **Results**
        Difference	-64688.000
        Standard error	5655.038
        95% CI	-75781.4937 to -53594.5063
        t-statistic 	-11.439
        DF 	1367
        Significance level	P < 0.0001

**Conclusion**:As p-values are less than 0.05 in the calculations except the comparison of average sales price between RH and RM, 
I concluded that this categorical feature can be statistically significant factor to predict sales price. 
 
*comparison of means calculator*: https://www.medcalc.org/calc/comparison_of_means.php
*Average sales price of MSZoning values*: https://colab.research.google.com/drive/1G28UbWB1QyA2M1XwNFADpMvdEwaNgPt6

### Footnotes
Clean Test Data: https://colab.research.google.com/drive/1yr7FQrEJKrui0ATbmsbvDsHJVr__RwyA

Group8_Finalized Data_SJ.ipynb: https://colab.research.google.com/drive/1G28UbWB1QyA2M1XwNFADpMvdEwaNgPt6

Final 16 Input Variables including 4 dummy variables for 'MSZoning' categorical variable: 
*   GrLivArea, GarageCars, TotalBsmtSF, FullBath, YearBuilt, YearRemodAdd, MasVnrArea, Fireplaces, BsmtFinSF1, LotFrontage, WoodDeckSF, OpenPorchSF, MSZoning_C (all), MSZoning_FV, MSZoning_RH, MSZoning_RL

Variable Cleaning: https://colab.research.google.com/drive/1bMWYf3pe3dx6Kcj4pY-Q8GOfO9b8_Kbm 
