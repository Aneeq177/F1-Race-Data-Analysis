# Formula 1 Race Data Analysis

## Project Description
This project analyzes Formula 1 race data from 1950 to 2023, covering drivers, circuits, constructors, and race results. The analysis includes loading data from multiple CSV files, merging relevant datasets, and calculating key performance metrics such as driver wins and average finishing positions. The project also identifies the most frequent winning drivers and constructors, and analyzes race results.

## Data Sources
The data is sourced from multiple CSV files:
- `circuits.csv`: Contains information about F1 circuits.
- `drivers.csv`: Contains information about F1 drivers.
- `constructors.csv`: Contains information about F1 constructors.
- `races.csv`: Contains information about F1 races.
- `results.csv`: Contains F1 race results.

## Data Loading and Merging
The project loads the data from the CSV files into Pandas DataFrames.  The code then merges these DataFrames to create a comprehensive dataset for analysis.  Key merges include:
- Merging `results.csv` with `races.csv` on `raceId`.
- Merging the result with `drivers.csv` on `driverId`.
- Merging the result with `constructors.csv` on `constructorId`.
- Merging the result with `circuits.csv` on `circuitId`.

## Data Analysis
The project performs the following analyses:
1.  **Top Drivers by Wins:** Calculates and displays the top 10 drivers with the most wins using `value_counts()` on the `driver_name` column where `positionOrder` is 1. A bar plot is generated to visualize the top 10 drivers.
2.  **Average Finishing Position for a Driver:** Calculates the average finishing position for a specified driver.
3.  **Wins per Constructor:** Calculates and displays the top 10 constructors with the most wins. A bar plot visualizes the top 10 constructors.

## Visualization
The project includes the following visualizations:
- Bar plot of the top 10 drivers by wins.
- Bar plot of the top 10 constructors by wins.

## Dependencies
The project uses the following Python libraries:
- Pandas
- Matplotlib
- Seaborn

## Code Overview

**1. Import Libraries:**
   - Imports necessary libraries: `pandas`, `matplotlib.pyplot`, and `seaborn`.

**2. Load Data:**
   - Loads data from CSV files into Pandas DataFrames:
     - `circuits.csv` into `df_circuits`
     - `drivers.csv` into `df_drivers`
     - `constructors.csv` into `df_constructors`
     - `races.csv` into `df_races`
     - `results.csv` into `df_results`
   - Prints the first 5 rows and info of each dataframe.

**3. Merge Data:**
    - Merges the dataframes to create a combined dataframe for analysis.

**4. Analyze Data:**
   -  `calculate_driver_wins(df)`: Calculates and prints the top 10 drivers with the most wins, and plots the results.
   -  `calculate_average_finishing_position_for_driver(df, target_driver_name)`: Calculates and prints the average finishing position for a specified driver.
   -  `calculate_constructor_wins(df)`: Calculates and prints the top 10 constructors with the most wins, and plots the results.

**5. Main Execution Block:**
    -  Calls the data loading and analysis functions.
    -  Sets the target driver name and calls the function to calculate the average finishing position for that driver.

## Results
The analysis provides insights into driver and constructor performance in Formula 1 racing history, including:
- The top 10 drivers with the most wins.
- The average finishing position for a selected driver.
- The top 10 constructors with the most wins.

