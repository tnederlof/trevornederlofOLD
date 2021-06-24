---
title: "Oak Creek Farmers Market - Maps & Analysis"
date: 2021-06-23T10:27:12-04:00
draft: false
---

In my work for Farm 2 Facts, I created a series of thematic and reference maps to aid research into the community around the Oak Creek Farmers Market located South of Milwaukee. Below are links to a series of research maps with some brief analysis. This work prompted further research by our team to help the market further support their local community.

Creating these maps involved sourcing various data sets, including the Census ACS 5-year, OpenStreetMap, and the USDA Food Access Research Atlas. After loading all of the data into a PostgreSQL database using the PostGIS extension, I efficiently queried just the data near the farmers market making working with the data in QGIS fast.

![Oak Creek Race Map](/img/oakcreek/oak_creek_race.png)

The neighborhoods surrounding the market are predominantly white. However, there are some block groups where no race is above 50%. These diverse block groups could serve as a more diverse customer base with some targeted outreach.

![Oak Creek Food Sources Map](/img/oakcreek/oak_creek_food_sources.png)

There are several competing farmers markets within a 10-mile radius of the Oak Creek Market, many of which are closer to the city of Milwaukee, lessening the chance of having customers from the city make it as far south as Oak Creek. There are also several supermarkets close by which also serve as competitors in terms of fresh foods.

![Oak Creek Income Map](/img/oakcreek/oak_creek_income.png)

Except for one block group 2.5 miles to the west of the market, all other block groups in the surrounding area of the Oak Creek Market have households making over $30,000 annually. Customers at the market are likely to have higher incomes than those closer to the city of Milwaukee.

![Oak Creek SNAP Map](/img/oakcreek/oak_creek_snap.png)

The areas surrounding the market have low SNAP usage, and it does not increase much until you get to West Milwaukee. A few census tracts received SNAP assistance around the market in a 5-mile radius, which the market could support.

![Oak Creek Transit Map](/img/oakcreek/oak_creek_transit.png)

A major bike path runs just north of the market, and the market square itself has ample bike parking spots. In addition, several bus routes go close to the market. It is worth understanding if the buses stop by the market, who takes the bus, and are they already customers.  
  

About Farm 2 Facts  
Farm 2 Facts is an organization that provides farmers market managers with a toolkit to help them collect data, inform decisions, and communicate with stakeholders, so they achieve their market goals. Organizations include city- or state-wide farmers market organizations or any other organization that oversees multiple farmers markets.

