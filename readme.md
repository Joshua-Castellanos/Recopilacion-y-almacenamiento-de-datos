# Zuber: Chicago Trip Analysis

This practicum project consists of a data analysis for **Zuber**, a new ride-sharing company launching in Chicago. The main objective is to understand passenger preferences and the impact of external factors, such as weather, on trips.

## 🎯 Project Objectives

*   Identify the top 10 taxi companies with the highest number of trips in Chicago.
*   Determine the most popular neighborhoods as final trip destinations.
*   Test the hypothesis that the average duration of trips from the Loop to O'Hare International Airport changes on rainy Saturdays.

## 📊 Dataset Descriptions

The project uses three main datasets:

1.  **`project_sql_result_01.csv`**:
    *   `company_name`: name of the taxi company.
    *   `trips_amount`: number of trips for each taxi company on November 15-16, 2017.
2.  **`project_sql_result_04.csv`**:
    *   `dropoff_location_name`: Chicago neighborhoods where trips ended.
    *   `average_trips`: average number of trips that ended in each neighborhood in November 2017.
3.  **`project_sql_result_07.csv`**: Data on trips from the Loop to O'Hare Airport.
    *   `start_ts`: pickup date and time.
    *   `weather_conditions`: weather conditions at the time the trip started.
    *   `duration_seconds`: trip duration in seconds.

## 🛠️ Tools Used

*   **Python 3**
*   **Pandas**: For data manipulation and cleaning.
*   **Matplotlib & Seaborn**: For creating aesthetic and informative visualizations.
*   **Scipy**: Specifically the `stats` module for performing statistical hypothesis tests.

## 🚀 Workflow

### 1. Exploratory Data Analysis (EDA)
Company and neighborhood data were analyzed to identify demand patterns.
*   **Flash Cab** was identified as the leading company with a significant lead over the competition.
*   The **Loop** neighborhood was the most frequent destination, followed by River North and Streeterville.

### 2. Data Visualization
Bar charts were created to visually represent the Top 10 companies by trip count and the Top 10 neighborhoods by average arrivals.

### 3. Hypothesis Testing
An independent Student's t-test was performed to compare trip durations under different weather conditions.
*   **Null Hypothesis (H₀)**: The average duration of trips from the Loop to O'Hare International Airport is the same on rainy Saturdays as on sunny Saturdays.
*   **Alternative Hypothesis (H₁)**: The average duration of trips differs based on weather conditions.

## 💡 Key Conclusions

1.  **Market Dominance**: Flash Cab dominates the Chicago taxi market during the analyzed period.
2.  **Urban Concentration**: Trip activity is heavily concentrated in the financial and tourist center (Loop, River North).
3.  **Weather Impact**: The null hypothesis was rejected, concluding that **rainy weather significantly increases trip duration**, likely due to traffic and road conditions.

## ⚙️ How to Run
1. Clone this repository.
2. Ensure you have the dependencies installed: `pip install pandas matplotlib seaborn scipy`.
3. Run the notebook `Chicago_Trip_Analysis.ipynb` in a Jupyter environment.

---
*Project developed as part of the TripleTen data analysis bootcamp.*
