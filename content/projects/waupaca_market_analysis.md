---
title: "Waupaca Farmers Market - Maps & Analysis"
date: 2021-06-23T09:14:12-04:00
draft: false
---

In my work for Farm 2 Facts, I created a series of thematic and reference maps to aid research into the community around the Waupaca Farmers Market located in Central Wisconsin. Below are links to a series of research maps with some brief analysis. This work prompted further research by our team to help the market further support their local community.

Creating these maps involved sourcing various data sets, including the Census ACS 5-year, OpenStreetMap, and the USDA Food Access Research Atlas. After loading all of the data into a PostgreSQL database using the PostGIS extension, I efficiently queried just the data near the farmers market making working with the data in QGIS fast.

![Waupaca Income Map](/img/waupaca/waupaca_income.png)

There are two block groups immediately east and north of the market, which have 30-65% of the households earning under $30,000 annually. The market could play a role in making healthy food available to these households experiencing poverty.

![Waupaca SNAP Map](/img/waupaca/waupaca_snap.png)

Several census tracts in and around Waupaca receive SNAP assistance. The census tract directly east of the market (shaded dark purple) has almost 25% of its households receiving SNAP benefits and are experiencing food insecurity. The Waupaca market could use targeted outreach to these households to provide an accessible access venue to fresh foods.

![Waupaca Education Map](/img/waupaca/waupaca_education.png)

Most of the areas around the Waupaca market have less than 40% of the population with bachelor degrees, with one block group just east of the market having 0-15% with bachelor degrees.

![Waupaca Transit Map](/img/waupaca/waupaca_transit.png)

No major buses or trains run through Waupaca. Therefore a car is necessary to get to the market. However, a main road/highway does run close to the town, bringing potential customers. There is also a bike path southwest of the market, which could funnel traffic to the market if the connection north is safe and well-advertised.

Farm 2 Facts is an organization that provides farmers market managers with a toolkit to help them collect data, inform decisions, and communicate with stakeholders, so they achieve their market goals. Organizations include city- or state-wide farmers market organizations or any other organization that oversees multiple farmers markets.

