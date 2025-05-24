# 📊 Visualization Library Documentation: Matplotlib & Pandas

This guide provides a comprehensive overview of two popular Python libraries for data visualization: **Matplotlib** and **Pandas**. It includes descriptions of the different types of plots available in each library, practical use cases, and code examples.

## 🔹 Matplotlib Overview
[Matplotlib Quick Start Guide](https://matplotlib.org/stable/users/explain/quick_start.html#quick-start)

**Matplotlib** is a powerful library for creating static, animated, and interactive visualizations in Python.

- **Strengths**:
  - Fine control over plot elements
  - Extensive plotting capabilities
  - Customizable and flexible
- **Typical Use Cases**:
  - Scientific and engineering plots
  - Static charts for reports and publications


import matplotlib.pyplot as plt
import numpy as np

# Line Plot
x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 40]
plt.plot(x, y)
plt.title("Line Plot")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()

# Bar Chart
categories = ['A', 'B', 'C']
values = [5, 7, 3]
plt.bar(categories, values)
plt.title("Bar Chart")
plt.show()

# Histogram
data = np.random.randn(1000)
plt.hist(data, bins=30, color='skyblue', edgecolor='black')
plt.title("Histogram")
plt.show()

# Pie Chart
labels = ['Apples', 'Bananas', 'Cherries']
sizes = [30, 40, 30]
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title("Pie Chart")
plt.show()

## 🔹 Pandas Overview
[Pandas User Guide](https://pandas.pydata.org/docs/user_guide/index.html)


**Pandas** is primarily used for data manipulation but also provides convenient visualization functions through its `.plot()` method (which uses Matplotlib underneath).

- **Strengths**:
  - Easy plotting from DataFrames and Series
  - Integrates seamlessly with data manipulation
  - Simple syntax for quick visualizations
- **Typical Use Cases**:
  - Exploratory Data Analysis (EDA)
  - Time-series and trend visualizations


import pandas as pd

# Sample DataFrame
df = pd.DataFrame({
    'Year': [2018, 2019, 2020, 2021],
    'Sales': [250, 300, 400, 350]
})

# Line Plot
df.plot(x='Year', y='Sales', kind='line', title="Sales Over Years")

# Bar Plot
df.plot(x='Year', y='Sales', kind='bar', title="Sales by Year")

# Histogram
df['Sales'].plot(kind='hist', bins=5, title="Sales Distribution")

# Pie Chart (on single series)
df.set_index('Year')['Sales'].plot(kind='pie', autopct='%1.1f%%', title="Sales Pie Chart")

## 🔸 Comparison: Matplotlib vs Pandas

| Feature           | Matplotlib                          | Pandas                                 |
|-------------------|--------------------------------------|-----------------------------------------|
| Ease of Use       | More verbose and detailed            | Simplified syntax with DataFrames       |
| Customization     | Highly customizable                  | Limited customization                   |
| Interactivity     | Static plots                         | Static plots                            |
| Use Case          | Precise control for professional plots | Quick data exploration and EDA         |
