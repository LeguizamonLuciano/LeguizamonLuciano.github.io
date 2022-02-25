---
title: Pandas + Power BI - Properati
date: 2022-02-18 18:32:00 -0300
categories: [Projects, Pandas+PowerBI]
tags: [transform, data, python, powerbi]
pin: true
---

## <u>About</u>

This dataset comes from Properati Data (https://www.properati.com.ar/data/) is the data division of Properati, a real estate search site in Latin America. 

The idea was to work 100% from PowerBI but I ran into difficulties (power bi is very slow for some tasks) so I decided to first clean the data with Pandas and then use PowerBI for graphics 

> I will be updating this page at least once a week
{: .prompt-warning}

## <u>Topic</u>

It contains information on online property rental or sale ads from around 2020 to 2021, it has various details such as square meters, price, region, etc.

## <u>Features</u>

|Col |Description   |
|----------|-------------|
| type |  Notice type (Property, Development/Project) |
| country |    Country in which the notice is published   |
| id | Notice identifier. It is not unique: if the notice is updated by the real estate agency (new version of the notice), a new record is created with the same id but different dates | 
| start_date |Notice registration date|
| end_date |Notice cancellation date|
| place |Fields referring to the location of the property or development|
| lat |Latitude|
| lon |Length|
| l1,l2,l3,l4 | Country, province, city, neighborhood|
| operation |Type of operation (Sale, Rent)|
| type |Type of property (House, Department, PH)|
| rooms |Number of rooms (useful in Argentina)|
| bedrooms |Number of bedrooms (useful in the rest of the countries)|
| bathrooms |Number of bathrooms|
| surface_total |Total surface in m²|
| surface_covered |Surface covered in m²|
| price |Price|
| currency |Currency of the published price|
| price_period |Price Period (Daily, Weekly, Monthly)|
| title |Title of the ad|
| description |Description of the ad|
| development |Fields related to real estate development (empty if the ad is for a property)|
| status |Development status (Completed, Under construction, ...)|
| name |Development name|
| short_description |Short description of the ad|
| description |Description of the ad|

## <u>To be continued...</u>
