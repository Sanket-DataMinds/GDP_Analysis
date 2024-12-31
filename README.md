# GDP Analysis using Python (Pandas, Plotly, Numpy)

## Overview
Gross Domestic Product (GDP) is a crucial economic indicator representing the total value of goods and services produced within a country over a specific period, usually a year. This project aims to analyze GDP data to gain insights into economic performance, growth rates, and comparisons between countries using Python libraries such as Pandas, Plotly, and Numpy.

## Key Features
1. **Dataset Walkthrough**:
   - Understand the structure and content of the dataset.
   - Use `df.head()` to display the first few rows of the dataset for an overview.

2. **GDP Growth Calculation**:
   - GDP growth rate is calculated using the formula:
     
     ```python
     GDP growth rate = (GDP in current period - GDP in previous period) / GDP in previous period * 100
     ```
   - For example, if GDP was 100 in 2020 and 105 in 2021, the growth rate is:
     
     ```
     GDP growth rate = (105 - 100) / 100 * 100 = 5%
     ```

3. **Visualization Using Plotly**:
   - Create interactive and dynamic graphs for better data visualization.
   - Utilize `plotly.express` and `plotly.graph_objects` for plotting.

4. **World GDP Growth Rate Analysis**:
   - Visualize GDP growth trends across all countries in the dataset.

5. **Country-wise GDP Comparison**:
   - Compare GDP across countries to understand relative economic performance.
   - Focused comparison of GDP growth between India and China:
     
     ```python
     c1 = df[df['Country Name'] == 'China']
     c2 = df[df['Country Name'] == 'India']
     df_pr = pd.concat([c1, c2], axis=0)
     fig = px.line(df_pr, x='Year', y='Value', title='GDP Comparison | India & China', color='Country Name')
     pyo.plot(fig, filename='IND|CHN.html')
     ```

## Libraries Required
1. **Pandas**: For data manipulation and analysis.
2. **Plotly**: For creating interactive and visually appealing plots.
3. **Numpy**: For numerical operations and calculations.

## Installation
1. Install the required libraries:
   ```bash
   pip install pandas plotly numpy
   ```

2. Set up Plotly account (if required) at [plotly.com](https://plotly.com/).

## Instructions
1. Load the dataset using Pandas and explore its structure with `df.head()`.
2. Calculate GDP growth rates for the dataset using the formula provided.
3. Use Plotly to create:
   - Global GDP growth visualizations.
   - Comparisons across countries.
   - Focused comparisons between India and China.
4. Save the interactive plots locally (e.g., `IND|CHN.html`).

## Insights
- Visualization of GDP trends highlights differences in economic growth across countries.
- Comparing India and China’s GDP illustrates how China’s GDP has grown significantly faster than India’s over the analyzed period.

## Outputs
1. Interactive plots showcasing:
   - Global GDP growth rates.
   - Country-wise GDP comparisons.
   - India vs. China GDP trends.

## Example Code Snippets
### GDP Growth Calculation
```python
# Example calculation of GDP growth rate
gdp_growth_rate = (current_gdp - previous_gdp) / previous_gdp * 100
```

### Plotly Visualization
```python
import plotly.express as px
import pandas as pd

c1 = df[df['Country Name'] == 'China']
c2 = df[df['Country Name'] == 'India']
df_pr = pd.concat([c1, c2], axis=0)
fig = px.line(df_pr, x='Year', y='Value', title='GDP Comparison | India & China', color='Country Name')
fig.show()
```

## Conclusion
This project leverages Python's data analysis and visualization libraries to analyze GDP data, providing valuable insights into economic growth and inter-country comparisons. The interactive plots enable users to explore data dynamically and make informed conclusions about global and country-specific economic trends.

