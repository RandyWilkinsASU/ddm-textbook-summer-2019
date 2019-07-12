


*** { @unit = "", @title = "Playing Moneyball (Team 4)", @reading, @foldout }

## Prediction  (Team 4)

* Eagle, N., & Greene, K. (2014). Reality mining: Using big data to engineer a better world. MIT Press. **CH6 optimizing resource allocation**
* Eagle, N., & Greene, K. (2014). Reality mining: Using big data to engineer a better world. MIT Press. **CH10 engineering a safer and healthier world**

<br>
<br>




*** { @unit = "", @title = "Bias in Prediction (Team 5)", @reading, @foldout }

## Bias in Prediction (Team 5)

* O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH1 bomb parts**
* O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH5 justice in an era of big data**
* O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH8 landing credit**

<br>
<br>


*** { @unit = "Due July 23rd", @title = "LAB 3 - Feature Selection", @assignment, @foldout }


## Preview

This lab covers "feature selection", the process of selecting variables you believe to be strong predictors of your outcome. In public policy feature selection can be a grueling process of testing lots of theories until you come up with a consistent story about what works. 

One of the biggest challanges in guessing which data will be useful ahead of time is that the brain is designed to tell stories, not to test the strength of theories (humans are bad at assessing probabilities of events occuring). When we are presented with a new variable our brains immediately start to invent stories of why it could explain the outcome. A well-known human bias is that the easier it is for us to invent a story, the more likely we are to believe it is true (lacking any evidence). 

You don't believe me? Well give it a try. The table below contains the 57 variables that Zillow uses for it's Zestimate model that predicts the market value of a home. Can you guess which three variables will most strongly predict the home value? 



| Feature         | Description    |
|:----------------|:----------------------------|
| **airconditioningtypeid**        |  Type of cooling system present in the home (if any)                                                                   |
| **architecturalstyletypeid**     |  Architectural style of the home (i.e. ranch, colonial, split-level, etc…)                                             |
| **basementsqft**                 |  Finished living area below or partially below ground level                                                            |
| **bathroomcnt**                  |  Number of bathrooms in home including fractional bathrooms                                                            |
| **bedroomcnt**                   |  Number of bedrooms in home                                                                                            |
| **buildingqualitytypeid**        |  Overall assessment of condition of the building from best (lowest) to worst (highest)                                 |
| **buildingclasstypeid**          | The building framing type (steel frame, wood frame, concrete/brick)                                                    |
| **calculatedbathnbr**            |  Number of bathrooms in home including fractional bathroom                                                             |
| **decktypeid**                   | Type of deck (if any) present on parcel                                                                                |
| **threequarterbathnbr**          |  Number of 3/4 bathrooms in house (shower + sink + toilet)                                                             |
| **finishedfloor1squarefeet**     |  Size of the finished living area on the first (entry) floor of the home                                               |
| **calculatedfinishedsquarefeet** |  Calculated total finished living area of the home                                                                     |
| **finishedsquarefeet6**          | Base unfinished and finished area                                                                                      |
| **finishedsquarefeet12**         | Finished living area                                                                                                   |
| **finishedsquarefeet13**         | Perimeter  living area                                                                                                 |
| **finishedsquarefeet15**         | Total area                                                                                                             |
| **finishedsquarefeet50**         |  Size of the finished living area on the first (entry) floor of the home                                               |
| **fips**                         |  Federal Information Processing Standard code -  see https://en.wikipedia.org/wiki/FIPS_county_code for more details   |
| **fireplacecnt**                 |  Number of fireplaces in a home (if any)                                                                               |
| **fireplaceflag**                |  Is a fireplace present in this home                                                                                   |
| **fullbathcnt**                  |  Number of full bathrooms (sink, shower + bathtub, and toilet) present in home                                         |
| **garagecarcnt**                 |  Total number of garages on the lot including an attached garage                                                       |
| **garagetotalsqft**              |  Total number of square feet of all garages on lot including an attached garage                                        |
| **hashottuborspa**               |  Does the home have a hot tub or spa                                                                                   |
| **heatingorsystemtypeid**        |  Type of home heating system                                                                                           |
| **latitude**                     |  Latitude of the middle of the parcel multiplied by 10e6                                                               |
| **longitude**                    |  Longitude of the middle of the parcel multiplied by 10e6                                                              |
| **lotsizesquarefeet**            |  Area of the lot in square feet                                                                                        |
| **numberofstories**              |  Number of stories or levels the home has                                                                              |
| **parcelid**                     |  Unique identifier for parcels (lots)                                                                                  |
| **poolcnt**                      |  Number of pools on the lot (if any)                                                                                   |
| **poolsizesum**                  |  Total square footage of all pools on property                                                                         |
| **pooltypeid10**                 |  Spa or Hot Tub                                                                                                        |
| **pooltypeid2**                  |  Pool with Spa/Hot Tub                                                                                                 |
| **pooltypeid7**                  |  Pool without hot tub                                                                                                  |
| **propertycountylandusecode**    |  County land use code i.e. it's zoning at the county level                                                             |
| **propertylandusetypeid**        |  Type of land use the property is zoned for                                                                            |
| **propertyzoningdesc**           |  Description of the allowed land uses (zoning) for that property                                                       |
| **rawcensustractandblock**       |  Census tract and block ID combined - also contains blockgroup assignment by extension                                 |
| **censustractandblock**          |  Census tract and block ID combined - also contains blockgroup assignment by extension                                 |
| **regionidcounty**               | County in which the property is located                                                                                |
| **regionidcity**                 |  City in which the property is located (if any)                                                                        |
| **regionidzip**                  |  Zip code in which the property is located                                                                             |
| **regionidneighborhood**         | Neighborhood in which the property is located                                                                          |
| **roomcnt**                      |  Total number of rooms in the principal residence                                                                      |
| **storytypeid**                  |  Type of floors in a multi-story house (i.e. basement and main level, split-level, attic, etc.).  See tab for details. |
| **typeconstructiontypeid**       |  What type of construction material was used to construct the home                                                     |
| **unitcnt**                      |  Number of units the structure is built into (i.e. 2 = duplex, 3 = triplex, etc...)                                    |
| **yardbuildingsqft17**           | Patio in  yard                                                                                                         |
| **yardbuildingsqft26**           | Storage shed/building in yard                                                                                          |
| **yearbuilt**                    |  The Year the principal residence was built                                                                            |
| **taxvaluedollarcnt**            | The total tax assessed value of the parcel                                                                             |
| **structuretaxvaluedollarcnt**   | The assessed value of the built structure on the parcel                                                                |
| **landtaxvaluedollarcnt**        | The assessed value of the land area of the parcel                                                                      |
| **taxamount**                    | The total property tax assessed for that assessment year                                                               |
| **assessmentyear**               | The year of the property tax assessment                                                                                |
| **taxdelinquencyflag**           | Property taxes for this parcel are past due as of 2015                                                                 |
| **taxdelinquencyyear**           | Year for which the unpaid propert taxes were due    |




** Week 4 - Challenges of Big Data

*** { @unit = "Due July 28th", @title = "Data Quality (Team 1)", @reading, @foldout }

1.	Meier, P. (2015). Digital humanitarians: how big data is changing the face of humanitarian response. Routledge. **CH2 the rise of big crisis data pp 31-47**
2.	Meier, P. (2015). Digital humanitarians: how big data is changing the face of humanitarian response. Routledge. **CH7 verifying big crisis data via crowd computing**
3.	Meier, P. (2015). Digital humanitarians: how big data is changing the face of humanitarian response. Routledge. **CH8 verifying big crisis data via artificial intelligence** 



*** { @unit = "", @title = "Manipulation (Team 2)", @reading, @foldout }

1.	O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH4 propaganda machine**
2.	O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH10 targeting citizens**




*** { @unit = "", @title = "Ethics of Algorithms (Team 3)", @reading, @foldout }

1.	O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH9 getting insurance**
2.	O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **conclusion**


*** { @unit = "", @title = "Best Practices for Privacy (Team 4)", @reading, @foldout }

1.	Pentland, A. (2015). Social Physics: How social networks can make us smarter. Penguin. **CH10 data-driven societies, Appendix 2 openPDS**
2.	Eagle, N., & Greene, K. (2014). Reality mining: Using big data to engineer a better world. MIT Press. **CH2 using personal data in a privacy-sensitive way**
3.	Everything you need to know about the EU’s new privacy law GDPR: https://www.theverge.com/2018/3/28/17172548/gdpr-compliance-requirements-privacy-notice




*** { @unit = "Due July 30rd", @title = "LAB 4 - Feature Engineering", @assignment }







** Week 5 - Managing with Data 


*** { @unit = "Due Aug 4th", @title = "Managerial Experiments (Team 5)", @reading, @foldout }

1.	Duhigg, C. (2016). Smarter faster better: The secrets of being productive. Random House. **CH8 Charlotte Fludd pp 247-252, the data room 252-256**
2.	BBC World Service: “How Iceland Saved Its Teenagers” November 11, 2017. [ link ]
3.	Eagle, N., & Greene, K. (2014). Reality mining: Using big data to engineer a better world. MIT Press. **CH4 engineering public policy**

*** { @unit = "", @title = "Information Blindness (Team 1)", @reading, @foldout }

1.	Duhigg, C. (2016). Smarter faster better: The secrets of being productive. Random House. **CH8 Charlotte Fludd pp 247-252, the data room 252-256**
2.	Meier, P. (2015). Digital humanitarians: how big data is changing the face of humanitarian response. Routledge. **CH2 the rise of big crisis data pp 25-31**
3.	Pentland, A. (2015). Social Physics: How social networks can make us smarter. Penguin. **CH7 organizational change**



*** { @unit = "", @title = "Start Final Memo", @assignment }






** Week 6 - Data-Driven Human Resources  

*** { @unit = "Due Aug 11th", @title = "Building Effective Teams (Team 2)", @reading, @foldout }


1.	Duhigg, C. (2016). “[What we learned from Google’s Efforts to Build a Perfect Team](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html).” The New York Times Magazine, Feb. 25, 2016.
1.	Pentland, A. (2015). Social Physics: How social networks can make us smarter. Penguin. **CH4 engagement**


*** { @unit = "", @title = "Incentivizing Teams (Team 3)", @reading, @foldout }

1.	Pentland, A. (2015). Social Physics: How social networks can make us smarter. Penguin. **CH3 idea flow**
1.	Pentland, A. (2015). Social Physics: How social networks can make us smarter. Penguin. **CH5 collective intelligence**
1.	Pentland, A. (2015). Social Physics: How social networks can make us smarter. Penguin. **CH6 shaping organizations**



*** { @unit = "", @title = "A Tale of Two Data-Driven Management Systems: Amazon and Zappos (Team 4)", @reading, @foldout }

Make an argument that Amazon's use of human resources data will be more effective than Zappos's approach.

1.	O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH7 sweating bullets**
1.	Kantor, J. & Streitfeld, D. “Inside Amazon: Wrestling Big Ideas in a Bruising Workplace.” The New York Times, August 15, 2015.
1.	Richard Feloni (Feb 19, 2016). “A former Zappos manager explains how her job changed after the company got rid of bosses.” Business Insider.
1.	Yuki Noguchi (July 21, 2015). "Zappos: A Workplace Where No One And Everyone Is The Boss." NPR.


*** { @unit = "", @title = "A Tale of Two Data-Driven Management Systems: Amazon and Zappos (Team 5)", @reading, @foldout }

Make an argument that Zappos's use of human resources data will be more effective than Amazon's approach.

1.	O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books. **CH7 sweating bullets**
1.	Kantor, J. & Streitfeld, D. “Inside Amazon: Wrestling Big Ideas in a Bruising Workplace.” The New York Times, August 15, 2015.
1.	Richard Feloni (Feb 19, 2016). “A former Zappos manager explains how her job changed after the company got rid of bosses.” Business Insider.
1.	Yuki Noguchi (July 21, 2015). "Zappos: A Workplace Where No One And Everyone Is The Boss." NPR.


*** { @unit = "Due August 13", @title = "Final Memo", @assignment }


