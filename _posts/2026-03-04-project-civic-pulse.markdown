---
layout: post
title:  Project Civic-Pulse
date:   2026-03-04 15:01:35 +0300
image: city_chicago.png
tags:   Personal Project
---

Spotlighting an analytics project completed while pursing a Masters degree in Computational Analytics and Public Policy. This project is titled Project Civic pulse as it aimed to analyze a connection between civic sentiment, annual budget and demographics surrounding the areas with the largest volume of 311 complaints. For this project data was acquired from three public datasets: City of Chicago Budget, Chicago 311 calls and Chicago Census. 

***

### Methodology:

Data was sourced via API calls and CSV bulk imports from three public datasets: the Chicago City Budget, 311 Calls for the City of Chicago, and Chicago Annual Census Data.

City Budget data was cleaned and aggregated by department, then joined to 311 call volume using City Department as the shared key — with 311 calls aggregated annually and by department to support this join. Chicago Annual Census data was linked to 311 calls using zip code, enabling analysis of call volume and complaint types relative to neighborhood demographics.

### Dashboard and Findings:

<a href="https://your-url.com" target="_blank">Dashboard Link</a>

<img src="{{ site.baseurl }}/images/311_service_requests.png" alt="Dashboard" width="800">

The top 10% of ZIP codes generate 62.7% of all complaints — a Gini coefficient of 0.81. Just 19% of neighborhoods generate 80% of all demand. This is not accidental: it reflects where residents live and how well urban infrastructure holds up.

The departments of Streets and Sanitation, Aviation, and Transportation account for around 80% of all 311 requests. Streets & Sanitation alone represents ~40%, Aviation ~27%, and Transportation ~18% of all civic demand citywide.

<img src="{{ site.baseurl }}/images/311_by_census.png" alt="Dashboard" width="800">

South Side and West Side neighborhoods consistently top the per-capita complaint ranking — with rates 3 to 4 times the city average. This is not statistical noise: the same ZIP codes appear at the top year after year. 

There aren't significant changes in the sources of 311 service requests when comparing 2019 and 2024 at the zip code level. We see higher volumes of requests being made from more populated areas in the south and west sides of Chicago. We also observe areas with higher populations having higher volumes of service requests throughout the city which aligns with expectations that more people leads to more use, need, and requests for city services. Overall, service requests totaled 970,790 in 2019 and 679,351 in 2024 (excluding the aforementioned categories).

<img src="{{ site.baseurl }}/images/311_map.png" alt="Dashboard" width="800">

South and West Side neighborhoods with lower incomes show rates 3–4 times the city average. The cause may be deteriorating infrastructure, higher density of urban problems, or greater reliance on 311 as the only available channel for resolution.

If lower-income neighborhoods also have longer closure times, the inequality compounds: more complaints filed AND slower service received. This analysis requires crossing resolution data with ZIP-level data — currently, time-to-close percentiles are available by department only, not by neighborhood.

<img src="{{ site.baseurl }}/images/budget_yoy.png" alt="Dashboard" width="800">

Budget data for the city of Chicago covers a 10-year window from 2016–2026, centered around the COVID global pandemic. From 2019–2022 the Chicago Department of Public Health budget quadrupled to manage the crisis and roll out testing city-wide. The Office of Budget and Management grew exponentially from 2020–2022 as it became a pass-through vehicle for federal COVID relief through the CARES Act. Unrelated to COVID, the budget for the Department of Water Management jumped 85% in a single year (2025–2026) driven by federal Disaster Recovery grants to address flood mitigation following severe storms in 2023 and 2024.

<img src="{{ site.baseurl }}/images/budget_311_yoy.png" alt="Dashboard" width="800">

This chart examines the 12 departments common between the City of Chicago budget and 311 call data, comparing the number of 311 calls to the budget of the following year. We would expect budget to move in the same direction as 311 call volume, just with a flatter slope. For many departments, both variables move in the same direction. However, there are examples like the Department of Transportation where the department quadruples its budget while call volumes decreased steadily by almost 70%. Contrary to expectations, some departments show significant budget spikes pointing to drastic policy changes across administrations and various factors including the COVID-19 pandemic.


### Video Walkthrough

<iframe src="https://www.youtube.com/watch?v=lx7YycQWmUw" frameborder="0" allowfullscreen></iframe>
