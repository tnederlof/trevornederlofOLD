---
title: "Brownsville Farmers Market - Maps & Analysis"
date: 2021-06-23T09:27:12-04:00
draft: false
---

In my work for Farm 2 Facts, I created a series of thematic and reference maps to aid research into the community around the Brownsville Farmers Market located in Southern Texas. Below are links to a series of research maps with some brief analysis. This work prompted further research by our team to help the market further support their local community.

Creating these maps involved sourcing various data sets, including the Census ACS 5-year, OpenStreetMap, and the USDA Food Access Research Atlas. After loading all of the data into a PostgreSQL database using the PostGIS extension, I efficiently queried just the data near the farmers market making working with the data in QGIS fast.

![Brownsville Education Map](/img/brownsville/brownsville_education.png)

A few block groups just northwest of the market have 65-100% of the population with bachelor degrees. Outside of those groups, many block groups are 0-10% with bachelor degrees showing a lot of discrepancy from neighborhood to neighborhood.

![Brownsville Income Map](/img/brownsville/brownsville_income.png)

Many block groups around the market have households almost entirely making less than $30,000 annually. These households in neighborhoods surrounding the market are likely experiencing food insecurity due to their low income.

![Brownsville SNAP Map](/img/brownsville/brownsville_snap.png)

Many census tracts around the market receive SNAP assistance with some as high as 80% of households. It should be a focus of the market to make it easy to use SNAP benefits and even match purchase dollars.

![Brownsville Transit Map](/img/brownsville/brownsville_transit.png)

There are no trains or light rail, but there is an extensive bus network, some of which pass close to the market. There are also some green spaces and a nearby river that could be attractive for people who want to linger after their visit to the market.



About Farm 2 Facts
Farm 2 Facts is an organization that provides farmers market managers with a toolkit to help them collect data, inform decisions, and communicate with stakeholders, so they achieve their market goals. Organizations include city- or state-wide farmers market organizations or any other organization that oversees multiple farmers markets.

