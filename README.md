# Airline Data Analytics Project


## Problem Statement

You are consulting for an airline company looking to enter the United States domestic market which has identified medium and large airports as their desired operating locations. The company believes that it has a competitive advantage in maintaining punctuality, so it plans on making this a big part of its brand image with a motto, “On time, for you.” To kick start operations, the company has decided to start with 5 round trip routes. An example of a round trip route is the combination of JFK to ORD and ORD to JFK. The opposite order of the route, ORD to JFK and JFK to ORD, would be considered the same round trip. 
You have been tasked with analyzing 1Q2019 data to identify: 
1. The 10 busiest round-trip routes in terms of number of round-trip flights in the quarter. Exclude canceled flights when performing the calculation. 
2. The 10 most profitable round trip routes (without considering the upfront airplane cost) in the quarter. Along with the profit, show total revenue, total cost, summary values of other key components and total round trip flights in the quarter for the top 10 most profitable routes. Exclude canceled flights from these calculations. 
3. The 5 round trip routes that you recommend investing in based on any factors that you choose.
4. The number of round-trip flights it will take to breakeven on the upfront airplane cost for each of the 5 round trip routes that you recommend. Print key summary components for these routes. 
5. Key Performance Indicators (KPI’s) that you recommend tracking in the future to measure the success of the round-trip routes that you recommend.

\
You have been given a metadata document and three datasets that you should use to inform your decision: 
1. Flights dataset: Contains data about available routes from origin to destination. For occupancy, use the data provided in this dataset. 
2. Tickets dataset: Ticket prices data (randomly sampled data only as the original dataset data is huge). Consider only round trips in your analysis. 
3. Airport Codes dataset: Identifies whether an airport is considered medium or large sized. Consider only medium and large airports in your analysis.
\
\
You can make the following assumptions: 
- Each airplane is dedicated to one round trip route between the 2 airports 
- Costs: 
  - Fuel, Oil, Maintenance, Crew - $8 per mile total 
  - Depreciation, Insurance, Other - $1.18 per mile total
  - Airport operational costs for the right to use the airports and related services are fixed at $5,000 for medium airports and $10,000 for large airports. There is one charge for each airport where a flight lands. Thus, a round trip flight has a total of two airport charges. 
  - Delays that are 15 minutes or less are free, however each additional minute of delay costs the airline $75 in added operational costs. This is charged separately for both arrival and departure delays. 
  - Each airplane will cost $90 million
- Revenue: 
  - Each plane can accommodate up to 200 passengers and each flight has an associated occupancy rate provided in the Flights data set. Do not use the Tickets data set to determine occupancy. 
  - Baggage fee is $35 for each checked bag per flight. We expect 50% of passengers to check an average of 1 bag per flight. The fee is charged separately for each leg of a round trip flight, thus 50% of passengers will be charged a total of $70 in baggage fees for a round trip flight. 
  - Disregard seasonal effects on ticket prices (i.e. ticket prices are the same in April as they are on Memorial Day or in December)

## Steps followed 

   The complete data analysis process was performed using python.

   STEPS:

- Load data from csv files to pandas dataframe.

- Use Python libraries (datetime, re, numpy, sqlite3) in conjuction with statistical techniques for data wrangling to rectify data quality issues and create a consolidated round-trip dataset.

- Use vectorized functions to perform analytics calculations on the large round-trip dataset.

- Use visualization libraries (seaborn and matplotlib) to create charts that visualize insights related to project goals.

- Create powerpoint slides that summarize the outcome of the data analytics project to stakeholders

## Insights Gained

The following inferences were drawn from the analysis process

### [1] 10 busiest round-trip routes in terms of number of round-trip flights in the quarter.

   ![Busiest Round-trips](https://github.com/Jucodez/Airline-Data-Analytics-Project/assets/102746691/8ea3297e-e9aa-4bf4-8928-d0534032ffc4)
           
### [2] The 10 most profitable round-trip routes (without considering the upfront airplane cost) in the quarter.

   ![Most Profitable Round-trip](https://github.com/Jucodez/Airline-Data-Analytics-Project/assets/102746691/c8843630-72e1-4da6-be59-16da35d4f024)
 
### [3] The 5 round-trip routes recommended for investments based on any factors that you choose.

   ![Recommended round-trips](https://github.com/Jucodez/Airline-Data-Analytics-Project/assets/102746691/7496b9ce-fe52-4e43-bd98-3f6f6786f11d)

### [4] The number of round-trip flights needed to breakeven on the upfront airplane cost for recommended round trip routes.

   ![Breakeven Analysis](https://github.com/Jucodez/Airline-Data-Analytics-Project/assets/102746691/df2116ab-0942-4e21-8169-e67e53225b6e)

### [5] Recommended Key Performance Indicators (KPI’s) to be tracked in the future to measure the success of the recommended round-trip routes.

   From the analysis carried out above it can be seen that these parameters help to determine the overall cost, reveune and then profit associated with a route.

- Number of round trips (ROUND_TRIP_COUNT)

- Average occupation rate per flight (AVG_OCCUPANCY_RATE)

- Average cost of ticket for different airlines ( AVG_ITIN_FARE)

- Average penalizable initial depature delay (AVG_PEN_INITIAL_DEP_DELAY)

- Average penalizable initial arrival delay (AVG_PEN_INITIAL_ARR_DELAY)

- Average penalizable final depature delay (AVG_PEN_FINAL_DEP_DELAY)

- Average penalizable final arrival delay (AVG_PEN_FINAL_ARR_DELAY)

- Revenue per flight (REVENUE_PER_FLIGHT)

- Cost per flight (COST_PER_FLIGHT)

- Profit per flight (PROFIT_PER_FLIGHT)

- Total revenue (TOTAL_REVENUE)

- Total cost (TOTAL_COST)

- Total profit (TOTAL_PROFIT)
