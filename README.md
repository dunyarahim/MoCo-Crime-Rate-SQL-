# Montgomery County Crime Database (Group SQL Project)

This group project analyzes over 300,000 reported crimes in Montgomery County, Maryland, using structured SQL queries to uncover patterns, biases, and trends related to location, policing, and crime types. The goal is to challenge assumptions about crime perception and provide a data-driven foundation for community safety analysis.

## Project Overview

Crime affects how we perceive neighborhoods, make housing decisions, and understand safety. But are certain areas truly more dangerous, or are stereotypes and enforcement patterns shaping those perceptions? Our project aims to answer this question by exploring reported crimes across Montgomery County by ZIP code.

We used publicly available crime data from Montgomery County's Open Data Portal, tracking incidents since 2016. The database includes crimes categorized by type, location, and police agency involvement. By focusing on zip codes, police district data, and area-level demographics, we provide a nuanced view of crime distribution and reporting practices.

This was originally a group project for an academic course. My primary contribution involved designing the ERD and normalization structure, writing and optimizing SQL queries, and developing views to analyze crime trends by ZIP code, agency, and offense category.

## Target Audience

This database is designed for:
- Citizens and residents deciding where to live
- Civil rights groups assessing over-policing
- Journalists and researchers investigating bias in reporting
- Law enforcement optimizing resource allocation
- Businesses evaluating crime risks
- Policymakers shaping safer, more equitable communities

## Key Questions the Database Answers

- What are the most common types of crimes in Montgomery County?
- How many crimes have occurred in a specific ZIP code over time?
- Which cities or ZIP codes show the highest and lowest crime rates?
- How do police response times vary by area and crime type?
- Are crimes more prevalent on specific days of the week?
- Do wealthier ZIP codes report fewer crimes?
- What types of crimes are most common in commercial vs. residential areas?
- How have crime rates shifted from 2019–2024?
- Which addresses or neighborhoods experience repeated offenses?
- Are drug or society-related crimes clustered in certain districts?

## Entity-Relationship Design
Our database includes 10+ normalized tables such as:

- `Crime_Type` – Categories of crimes (e.g., drug offenses, crimes against society)
- `Case_Report` – Individual crime incidents
- `Location` – Crime locations including latitude, longitude, and address
- `Zip_Code` – Links ZIP codes to city and crime region
- `Agency` – Police department or agency that handled the case
- `Police_District` – Police jurisdictions involved
- `Case_Offense` – Link table between case reports and offenses
- `Offense_Code` – Classification of criminal offenses

## Entities Not Included

To keep the project focused, we excluded:
- Real-time victim identities or personally identifiable information
- Media coverage tracking
- Full community demographic surveys
- Internal police logs or officer names

## Sample SQL Views

This repository includes example views such as:
- `query_takomapark` – Crimes that occurred in Takoma Park
- `query_rcpd` – Crimes responded to by RCPD
- `query_dv` – Drug/narcotic-related crimes
- `query_cas` – Crimes against society
- `query_citycount` – Total crimes per city
- `query_crimenamecount` – Frequency of specific crimes
- `query_addresscount` – Locations with repeat crimes
- `query_offense_linked` – Linking case reports to offense codes

## Diversity, Equity & Inclusion (DEI)

Our design acknowledges the challenges of analyzing crime by ZIP code, which can hide neighborhood-level disparities. We aimed to prevent reinforcing bias by allowing for integration of income, race, and housing data alongside crime statistics. Our goal is to highlight structural causes—not just geographic clusters—to avoid skewed conclusions.

## Ethical Considerations

We avoided storing specific addresses or GPS coordinates in public form to protect privacy. Our dataset is sourced from public portals and complies with fair use guidelines. Future users should ensure the data is used responsibly, especially when drawing conclusions that impact communities.



