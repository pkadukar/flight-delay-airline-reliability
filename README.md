# Flight Delay and Airline Reliability Analysis

A data analysis project using U.S. Bureau of Transportation Statistics (BTS) flight performance data to examine airline reliability and traveler-facing delay patterns.

The project focuses on nonstop flights between **JFK and LAX** during the winter holiday travel period and compares reliability across airlines, travel direction, scheduled departure time, and holiday travel phases.

> **Status:** In Progress  
> Current milestone: December 2024 pilot analysis completed.

---

## Project Objective

The goal of this project is to help travelers understand historical flight reliability trade-offs rather than assign airlines a single overall score.

The analysis examines:

- On-time arrival performance
- Severe delays
- Cancellations
- Diversions
- Typical delay duration
- Recorded delay causes
- Airline differences
- Route direction
- Scheduled departure period
- Holiday travel phase

The full project will analyze multiple holiday seasons from **2021–22 through 2025–26**.

---

## Current Pilot Scope

The completed pilot analyzes:

- **Route:** JFK ↔ LAX
- **Flight type:** Nonstop scheduled flights
- **Period:** December 18–31, 2024
- **Scheduled flights:** 754
- **Airlines:** American Airlines, JetBlue, and Delta Air Lines

January 1–2, 2025 will later be added to complete the intended holiday return window.

---

## Reliability Definitions

Flights are classified into mutually exclusive primary outcomes:

- **On Time:** arrival delay < 15 minutes
- **Delayed:** arrival delay between 15 and 45 minutes
- **Severe Delay:** arrival delay > 45 minutes
- **Cancelled**
- **Diverted**

The primary on-time rate uses **all scheduled flights as the denominator**, reflecting the perspective of a traveler choosing a scheduled flight.

---

## December 2024 Pilot Findings

Across the 754 scheduled JFK ↔ LAX flights:

- **84.22%** arrived on time
- **8.62%** experienced a severe delay
- **0%** were cancelled
- **2 flights** were diverted
- Median delay among flights delayed at least 15 minutes: **52 minutes**
- Mean delay among delayed flights: **81.06 minutes**
- Maximum observed arrival delay: **808 minutes**

The difference between the mean and median reflects a right-skewed delay distribution containing several extremely long delays.

### Delay Causes

Among the 117 flights delayed at least 15 minutes:

- Carrier delay affected **64.96%**
- NAS delay affected **56.41%**
- Late-aircraft delay affected **27.35%**
- Weather delay affected **4.27%**
- Security delay affected **0%**

A single flight may contain multiple recorded delay causes.

Of the total recorded delay-cause minutes:

- Carrier: **49.0%**
- NAS: **25.5%**
- Late aircraft: **22.5%**
- Weather: **3.0%**
- Security: **0%**

---

## Airline Comparison

| Airline | Scheduled Flights | On-Time Rate | Severe Delay Rate | Median Delay When Delayed |
|---|---:|---:|---:|---:|
| American Airlines | 244 | 86.89% | 7.79% | 61.5 min |
| JetBlue | 291 | 86.25% | 6.87% | 40.5 min |
| Delta Air Lines | 219 | 78.54% | 11.87% | 56.0 min |

These results describe only the December 2024 pilot window and should not be interpreted as overall airline rankings.

---

## Additional Comparisons

The pilot also analyzes reliability by:

### Direction

- JFK → LAX
- LAX → JFK

### Scheduled Departure Period

- Morning: 3:00 AM–11:59 AM
- Afternoon: 12:00 PM–4:59 PM
- Evening: 5:00 PM–8:59 PM
- Late Night: 9:00 PM–2:59 AM

### Holiday Travel Phase

- Outbound Window
- Christmas Period
- Between Phases
- Return Window

The current pilot Return Window contains only December 30–31. January 1–2 will be incorporated when the January 2025 dataset is added.

---

## Tools and Technologies

- Python
- pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Git / GitHub

---

## Repository Structure

```text
flight-delay-airline-reliability/
├── docs/
│   └── Flight_Delay_Analysis_Project_Blueprint.docx
├── notebooks/
│   └── 01_december_2024_data_validation.ipynb
├── src/
├── .gitignore
└── README.md


Data Source
Flight data comes from the U.S. Bureau of Transportation Statistics (BTS) TranStats On-Time Performance dataset.
The raw datasets are not stored in this repository because of their size. Analysis notebooks operate on locally downloaded BTS files.


Next Steps
Planned development includes:
- Add January 2025 data to complete the 2024–25 holiday window
- Generalize the processing pipeline across all five holiday seasons
- Compare reliability across years
- Analyze airline consistency across seasons
- Expand direction, departure-time, and holiday-phase comparisons
- Create reusable processing and analysis functions
- Produce final traveler-facing visualizations and conclusions


Project Motivation
This project was built to strengthen practical experience with:
- real-world data validation and cleaning
- exploratory data analysis
- feature engineering
- statistical reasoning
- pandas and NumPy
- data visualization
- reproducible analytical workflows
- communicating findings without overstating conclusions
