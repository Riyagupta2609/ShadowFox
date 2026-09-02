# Visualization Libraries Documentation

## A Practical Guide to Matplotlib and Seaborn

---

# 1. Introduction

Data visualization is an essential part of data analysis and machine learning. It helps transform raw numerical data into graphical representations that are easier to understand and interpret. Python provides several powerful visualization libraries, among which **Matplotlib** and **Seaborn** are two of the most commonly used.

This guide introduces both libraries, explores the different types of graphs they can generate, and provides simple code examples for beginners.

---

# 2. Matplotlib

## 2.1 Overview

Matplotlib is one of the most popular and foundational data visualization libraries in Python. It provides extensive control over plots and allows users to create highly customized static, animated, and interactive visualizations.

Matplotlib is particularly useful when precise control over graph elements such as axes, labels, colors, legends, and styles is required.

### Key Features

* Supports a wide variety of graph types.
* Highly customizable.
* Works well with NumPy and Pandas.
* Suitable for publication-quality visualizations.
* Provides both simple and advanced plotting capabilities.

### Installation

```python
pip install matplotlib
```

### Import

```python
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
```

Official documentation: [Matplotlib Quick Start Guide](https://matplotlib.org/stable/users/explain/quick_start.html?utm_source=chatgpt.com)

---

## 2.2 Line Plot

A line plot displays data points connected by straight lines. It is commonly used to visualize trends over time.

### Use Case

Tracking stock prices, temperature changes, or sales trends.

### Example

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]

plt.plot(x, y)
plt.title("Line Plot")
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.show()
```

---

## 2.3 Scatter Plot

A scatter plot represents the relationship between two numerical variables using individual points.

### Use Case

Analyzing correlation between study hours and exam scores.

### Example

```python
import matplotlib.pyplot as plt

hours = [1, 2, 3, 4, 5]
scores = [45, 50, 65, 70, 90]

plt.scatter(hours, scores)
plt.title("Scatter Plot")
plt.xlabel("Study Hours")
plt.ylabel("Exam Score")
plt.show()
```

---

## 2.4 Bar Chart

A bar chart compares values across different categories.

### Use Case

Comparing sales of different products.

### Example

```python
import matplotlib.pyplot as plt

products = ['Laptop', 'Phone', 'Tablet', 'Watch']
sales = [50, 80, 40, 60]

plt.bar(products, sales)
plt.title("Product Sales")
plt.xlabel("Products")
plt.ylabel("Sales")
plt.show()
```

---

## 2.5 Horizontal Bar Chart

A horizontal bar chart displays categories along the vertical axis.

### Use Case

Comparing values when category names are long.

### Example

```python
import matplotlib.pyplot as plt

products = ['Laptop', 'Phone', 'Tablet', 'Watch']
sales = [50, 80, 40, 60]

plt.barh(products, sales)
plt.title("Horizontal Bar Chart")
plt.xlabel("Sales")
plt.ylabel("Products")
plt.show()
```

---

## 2.6 Histogram

A histogram represents the frequency distribution of numerical data.

### Use Case

Understanding the distribution of student marks or customer ages.

### Example

```python
import matplotlib.pyplot as plt

marks = [45, 50, 55, 60, 62, 65, 70, 72, 75, 80, 85, 90]

plt.hist(marks, bins=5)
plt.title("Distribution of Marks")
plt.xlabel("Marks")
plt.ylabel("Frequency")
plt.show()
```

---

## 2.7 Pie Chart

A pie chart represents the proportion of different categories as sections of a circle.

### Use Case

Showing market share or budget distribution.

### Example

```python
import matplotlib.pyplot as plt

labels = ['Python', 'Java', 'C++', 'JavaScript']
sizes = [40, 25, 20, 15]

plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title("Programming Language Popularity")
plt.show()
```

---

## 2.8 Box Plot

A box plot displays the distribution of numerical data and helps identify the median, quartiles, and outliers.

### Use Case

Detecting outliers in salary or exam score datasets.

### Example

```python
import matplotlib.pyplot as plt

data = [10, 12, 15, 18, 20, 22, 25, 30, 100]

plt.boxplot(data)
plt.title("Box Plot")
plt.ylabel("Values")
plt.show()
```

---

## 2.9 Area Plot

An area plot is similar to a line plot but fills the area between the line and axis.

### Use Case

Visualizing cumulative quantities over time.

### Example

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]

plt.fill_between(x, y)
plt.title("Area Plot")
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.show()
```

---

## 2.10 Multiple Line Plot

Multiple line plots allow comparison between different datasets.

### Use Case

Comparing sales performance of multiple companies.

### Example

```python
import matplotlib.pyplot as plt

months = [1, 2, 3, 4, 5]
company_a = [10, 20, 30, 40, 50]
company_b = [15, 25, 28, 35, 45]

plt.plot(months, company_a, label='Company A')
plt.plot(months, company_b, label='Company B')

plt.title("Company Sales Comparison")
plt.xlabel("Month")
plt.ylabel("Sales")
plt.legend()
plt.show()
```

---

# 3. Seaborn

## 3.1 Overview

Seaborn is a high-level Python visualization library built on top of Matplotlib. It simplifies the creation of attractive and informative statistical graphics.

Seaborn provides built-in themes, color palettes, and functions specifically designed for exploring relationships and distributions in datasets.

### Key Features

* Built on top of Matplotlib.
* Provides attractive default styles.
* Simplifies statistical visualization.
* Integrates well with Pandas DataFrames.
* Supports advanced plots with minimal code.

### Installation

```python
pip install seaborn
```

### Import

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
```

Official documentation: [Seaborn Introduction and Tutorial](https://seaborn.pydata.org/tutorial/introduction.html?utm_source=chatgpt.com)

---

## 3.2 Line Plot

Seaborn's line plot is used to visualize changes and trends between numerical variables.

### Use Case

Visualizing changes in sales or temperature over time.

### Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]

sns.lineplot(x=x, y=y)

plt.title("Line Plot using Seaborn")
plt.show()
```

---

## 3.3 Scatter Plot

A scatter plot visualizes the relationship between two numerical variables.

### Use Case

Finding relationships between income and spending.

### Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 15, 20, 18, 25]

sns.scatterplot(x=x, y=y)

plt.title("Scatter Plot using Seaborn")
plt.show()
```

---

## 3.4 Bar Plot

Seaborn bar plots are useful for comparing values between categories and can automatically calculate statistical estimates.

### Use Case

Comparing average marks of students from different departments.

### Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

data = {
    'Department': ['CSE', 'AI', 'ECE', 'IT'],
    'Marks': [85, 90, 75, 88]
}

sns.barplot(x='Department', y='Marks', data=data)

plt.title("Average Marks by Department")
plt.show()
```

---

## 3.5 Count Plot

A count plot displays the number of observations in each categorical group.

### Use Case

Counting the number of students in different departments.

### Example

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

data = pd.DataFrame({
    'Department': ['CSE', 'AI', 'CSE', 'IT', 'AI', 'CSE']
})

sns.countplot(x='Department', data=data)

plt.title("Student Count by Department")
plt.show()
```

---

## 3.6 Histogram

Seaborn provides histograms for visualizing the distribution of numerical data.

### Use Case

Analyzing the distribution of customer ages.

### Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

ages = [18, 20, 21, 22, 25, 27, 30, 32, 35, 40]

sns.histplot(ages, bins=5)

plt.title("Age Distribution")
plt.show()
```

---

## 3.7 KDE Plot

A Kernel Density Estimate (KDE) plot shows the probability density distribution of continuous data.

### Use Case

Understanding the shape and density of a dataset.

### Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

data = [10, 12, 15, 18, 20, 22, 25, 30]

sns.kdeplot(data, fill=True)

plt.title("KDE Plot")
plt.show()
```

---

## 3.8 Box Plot

Seaborn box plots are useful for analyzing distributions and identifying outliers.

### Use Case

Comparing salary distributions across different departments.

### Example

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

data = pd.DataFrame({
    'Department': ['CSE', 'CSE', 'AI', 'AI', 'IT', 'IT'],
    'Salary': [8, 10, 12, 15, 9, 11]
})

sns.boxplot(x='Department', y='Salary', data=data)

plt.title("Salary Distribution")
plt.show()
```

---

## 3.9 Violin Plot

A violin plot combines characteristics of a box plot and KDE plot. It shows both the distribution and density of data.

### Use Case

Comparing score distributions across multiple groups.

### Example

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

data = pd.DataFrame({
    'Group': ['A', 'A', 'A', 'B', 'B', 'B'],
    'Score': [60, 70, 80, 65, 75, 90]
})

sns.violinplot(x='Group', y='Score', data=data)

plt.title("Violin Plot")
plt.show()
```

---

## 3.10 Heatmap

A heatmap represents numerical values using different color intensities.

### Use Case

Visualizing correlation between features in a machine learning dataset.

### Example

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

data = pd.DataFrame({
    'Math': [80, 85, 90, 75],
    'Science': [78, 88, 92, 70],
    'English': [82, 84, 89, 76]
})

correlation = data.corr()

sns.heatmap(correlation, annot=True)

plt.title("Correlation Heatmap")
plt.show()
```

---

## 3.11 Pair Plot

A pair plot creates scatter plots between multiple numerical variables and helps analyze relationships within a dataset.

### Use Case

Exploratory Data Analysis (EDA) of machine learning datasets.

### Example

```python
import seaborn as sns

iris = sns.load_dataset("iris")

sns.pairplot(iris)
```

---

## 3.12 Joint Plot

A joint plot combines a scatter plot with histograms or density plots.

### Use Case

Analyzing the relationship and distribution of two variables simultaneously.

### Example

```python
import seaborn as sns

iris = sns.load_dataset("iris")

sns.jointplot(
    data=iris,
    x="sepal_length",
    y="petal_length"
)
```

---

## 3.13 Regression Plot

A regression plot displays the relationship between variables along with a regression line.

### Use Case

Analyzing linear relationships between variables.

### Example

```python
import seaborn as sns

iris = sns.load_dataset("iris")

sns.regplot(
    data=iris,
    x="sepal_length",
    y="petal_length"
)
```

---

# 4. Comparison Between Matplotlib and Seaborn

| Feature                   | Matplotlib | Seaborn                                      |
| ------------------------- | ---------- | -------------------------------------------- |
| Ease of Use               | Moderate   | Easy                                         |
| Customization             | Very High  | High                                         |
| Default Appearance        | Basic      | Attractive                                   |
| Statistical Plots         | Limited    | Excellent                                    |
| Interactivity             | Limited    | Limited                                      |
| Learning Curve            | Moderate   | Easy for beginners                           |
| Large Dataset Performance | Good       | Depends on underlying Matplotlib             |
| Integration with Pandas   | Good       | Excellent                                    |
| Advanced Customization    | Excellent  | Can use Matplotlib for further customization |

---

## 4.1 Matplotlib Strengths

* Provides complete control over every element of a graph.
* Supports a large variety of visualization types.
* Suitable for highly customized and publication-quality figures.
* Works efficiently with NumPy arrays and Pandas DataFrames.
* Acts as the foundation for many other visualization libraries.

### Weaknesses

* Requires more code for complex visualizations.
* Default graphs may appear less visually appealing.
* Statistical visualizations require more manual implementation.

---

## 4.2 Seaborn Strengths

* Easy to use for beginners.
* Produces visually attractive graphs with minimal code.
* Excellent for statistical data visualization.
* Provides built-in datasets and themes.
* Works seamlessly with Pandas DataFrames.
* Includes advanced plots such as heatmaps, violin plots, pair plots, and regression plots.

### Weaknesses

* Offers less low-level control compared to Matplotlib.
* Primarily focused on statistical visualization.
* Complex customizations may require using Matplotlib functions.

---

# 5. When Should You Use Which Library?

### Use Matplotlib when:

* You need complete control over graph customization.
* You want to create highly customized visualizations.
* You are working with basic plots such as line charts, scatter plots, and bar charts.
* You need publication-quality figures.

### Use Seaborn when:

* You want attractive visualizations with less code.
* You are performing Exploratory Data Analysis (EDA).
* You need statistical visualizations.
* You are working extensively with Pandas DataFrames.
* You want to analyze relationships between multiple variables.

---

# 6. Conclusion

Matplotlib and Seaborn are powerful and complementary Python visualization libraries.

Matplotlib provides flexibility and detailed customization, making it suitable for creating almost any type of static visualization. Seaborn, built on top of Matplotlib, simplifies the process of creating attractive and informative statistical graphics.

For beginners, Seaborn is useful for quickly generating visually appealing plots, while learning Matplotlib is important for understanding the fundamentals and gaining complete control over visualization design. In practical data science workflows, both libraries are often used together.

---

# 7. Resources

1. Matplotlib Official Documentation
   [Matplotlib Documentation](https://matplotlib.org/stable/users/explain/quick_start.html?utm_source=chatgpt.com)

2. Seaborn Official Documentation
   [Seaborn Documentation](https://seaborn.pydata.org/tutorial/introduction.html?utm_source=chatgpt.com)

3. Plotly Python Documentation
   [Plotly Python Documentation](https://plotly.com/python/distplot/?utm_source=chatgpt.com)

4. Bokeh Documentation
   [Bokeh User Guide](https://docs.bokeh.org/en/latest/docs/user_guide/basic.html?utm_source=chatgpt.com)

5. Pandas Documentation
   [Pandas User Guide](https://pandas.pydata.org/docs/user_guide/index.html?utm_source=chatgpt.com)

