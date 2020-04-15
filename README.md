# What Impacts Our House Prices?

## Project Description

It's a goal for many people across to world to eventually atain home ownership. People may think of the size of their kitchen and living room or how recently their home was built to value their home. In reality, there are many factors that don't come intuitively to mind that can play a role in determining the sale value of a house. For example, would you have considered the flatness of the grounds, or the direction of the nearest railway? 

This project seeks to analyze a dataset of 80 variables over 1000+ homes to understand how best to predict the value of other homes. This is a small sample, with a relatively small number of features but serves as a an effective example of how to predict the value of homes in any given area of the world where structured data is available on home sales. 

**Project Goal:** Using a given dataset of home sale prices and 80 descriptive features of each home, predict the value of other homes given similar characteristics.

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

## Findings
1. 
