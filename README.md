# matplotlib_learning
# 📊 Matplotlib Learning Tutorial

A beginner-friendly and placement-oriented repository for learning **Matplotlib in Python** through practical examples in **Google Colab**.

This repository covers Matplotlib fundamentals, different visualization techniques, customization, subplots, Pandas integration, EDA, and visualization best practices.

---

## 📌 About Matplotlib

**Matplotlib** is a Python library used for creating data visualizations.

It can be used to create:

* Line charts
* Bar charts
* Histograms
* Scatter plots
* Pie charts
* Box plots
* Heatmaps
* Multiple plots and subplots

Matplotlib provides both a simple `pyplot` interface and an object-oriented approach using **Figure** and **Axes**.

---

## 🎯 Learning Objectives

By completing this repository, you will learn how to:

* Understand the basics of Matplotlib
* Use `matplotlib.pyplot`
* Create different types of charts
* Customize visualizations
* Work with Figure and Axes
* Create multiple subplots
* Integrate Pandas with Matplotlib
* Perform basic Exploratory Data Analysis (EDA)
* Save and export visualizations
* Choose appropriate charts for different situations
* Prepare for Matplotlib and data-visualization interview questions

---

# 📚 Topics Covered

## 1. Introduction to Matplotlib

* What is Matplotlib?
* Why Matplotlib is used
* Importing Matplotlib
* Introduction to `pyplot`
* `plt` alias

```python
import matplotlib.pyplot as plt
```

---

## 2. Line Charts

Learn how to visualize trends and relationships using line charts.

Topics:

* Basic line chart
* Titles
* X-axis and Y-axis labels
* Markers
* Line styles
* Line colors
* Line width
* Multiple lines
* Legends
* Grid
* Axis limits

Example:

```python
plt.plot(x, y)
plt.title("Sales Trend")
plt.xlabel("Day")
plt.ylabel("Sales")
plt.show()
```

---

## 3. Bar Charts

Bar charts are useful for comparing different categories.

Topics:

* Basic bar chart
* Horizontal bar chart
* Bar colors
* Edge colors
* Line width
* Bar width
* Adding values above bars
* Grouped bar charts
* Stacked bar charts

Example:

```python
plt.bar(products, sales)
plt.title("Product Sales")
plt.xlabel("Product")
plt.ylabel("Sales")
plt.show()
```

---

## 4. Histograms

Histograms are used to understand the distribution of numerical data.

Topics:

* Creating histograms
* Understanding bins
* Choosing the number of bins
* Histogram customization
* Edge colors
* Transparency
* `density=True`

Example:

```python
plt.hist(scores, bins=5)
plt.title("Score Distribution")
plt.xlabel("Score")
plt.ylabel("Frequency")
plt.show()
```

---

## 5. Scatter Plots

Scatter plots are useful for analyzing relationships between numerical variables.

Topics:

* Basic scatter plots
* Positive relationships
* Negative relationships
* No obvious relationship
* Marker size
* Marker style
* Transparency
* Color-based visualization
* Trend lines

Example:

```python
plt.scatter(hours, scores)
plt.title("Study Hours vs Score")
plt.xlabel("Study Hours")
plt.ylabel("Score")
plt.show()
```

---

## 6. Pie Charts

Pie charts are used to show parts of a whole.

Topics:

* Basic pie chart
* Labels
* Percentages
* `autopct`
* `startangle`
* `explode`
* Shadows
* Choosing when to use a pie chart

Example:

```python
plt.pie(
    users,
    labels=platforms,
    autopct="%1.1f%%",
    startangle=90
)

plt.show()
```

---

## 7. Box Plots

Box plots summarize the distribution of numerical data.

Topics:

* Minimum
* Q1
* Median
* Q3
* Maximum
* Interquartile range
* Outliers
* Vertical box plots
* Horizontal box plots

Example:

```python
plt.boxplot(scores)
plt.title("Score Distribution")
plt.ylabel("Scores")
plt.show()
```

---

## 8. Heatmaps

Heatmaps represent numerical values using colors.

Topics:

* `imshow()`
* Color maps
* `cmap`
* `colorbar`
* Displaying values inside cells

Example:

```python
plt.imshow(data, cmap="viridis")
plt.colorbar()
plt.show()
```

---

# 🎨 9. Plot Customization

Learn how to make visualizations clearer and more professional.

Topics:

* `color`
* `linewidth`
* `linestyle`
* `marker`
* `markersize`
* `alpha`
* `edgecolor`
* `label`
* `legend()`
* `grid()`
* Figure size

Example:

```python
plt.plot(
    x,
    y,
    color="blue",
    linewidth=2,
    linestyle="--",
    marker="o",
    markersize=8
)
```

---

# 🧩 10. Figure and Axes

Learn Matplotlib's object-oriented approach.

### Figure

The complete canvas containing the visualization.

### Axes

The actual area where data is plotted.

Common approach:

```python
fig, ax = plt.subplots()
```

Example:

```python
fig, ax = plt.subplots(figsize=(10, 5))

ax.plot(x, y)

ax.set_title("Sales Trend")
ax.set_xlabel("Day")
ax.set_ylabel("Sales")

plt.show()
```

---

# 📊 11. Subplots

Learn how to create multiple visualizations inside one Figure.

Topics:

* `plt.subplots()`
* Rows and columns
* 1 × 2 layouts
* 2 × 1 layouts
* 2 × 2 layouts
* Accessing individual Axes
* `tight_layout()`

Example:

```python
fig, ax = plt.subplots(2, 2, figsize=(10, 8))

ax[0, 0].plot(x, y)
ax[0, 1].bar(x, y)
ax[1, 0].scatter(x, y)
ax[1, 1].hist(y)

plt.tight_layout()
plt.show()
```

---

# 🐼 12. Pandas + Matplotlib

Learn how to visualize data stored in Pandas DataFrames.

Topics:

* Creating DataFrames
* Selecting DataFrame columns
* Plotting DataFrame columns
* Line charts
* Bar charts
* Scatter plots
* Basic data analysis

Example:

```python
plt.plot(df["Month"], df["Sales"])

plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales")

plt.show()
```

---

# 🚀 13. Advanced Plotting

Topics:

* Multiple lines
* Axis limits
* `set_xlim()`
* `set_ylim()`
* Custom ticks
* `set_xticks()`
* `set_yticks()`
* `text()`
* `annotate()`
* Error bars
* `errorbar()`

Example:

```python
ax.annotate(
    "Highest Sales",
    xy=("Jun", 200),
    xytext=("Apr", 220),
    arrowprops=dict(arrowstyle="->")
)
```

---

# 💾 14. Saving and Exporting Figures

Learn how to save visualizations for reports, presentations, and projects.

Topics:

* `savefig()`
* PNG
* JPG/JPEG
* PDF
* SVG
* DPI
* `bbox_inches="tight"`

Example:

```python
plt.savefig(
    "sales_chart.png",
    dpi=300,
    bbox_inches="tight"
)
```

You can also save through the Figure object:

```python
fig.savefig("sales_chart.png", dpi=300)
```

---

# 🧠 15. Visualization Best Practices

Learn how to create clear and meaningful visualizations.

Topics:

* Choosing the correct chart
* Meaningful titles
* Axis labels
* Appropriate scales
* Using colors effectively
* Using legends
* Avoiding unnecessary decoration
* Avoiding misleading visualizations
* Keeping charts readable
* Correlation vs causation

### Chart Selection Cheat Sheet

| Goal                  | Recommended Chart |
| --------------------- | ----------------- |
| Compare categories    | Bar chart         |
| Show trend over time  | Line chart        |
| Show distribution     | Histogram         |
| Show relationship     | Scatter plot      |
| Show parts of a whole | Pie chart         |
| Find outliers         | Box plot          |
| Show matrix values    | Heatmap           |

---

# 🔍 16. Exploratory Data Analysis (EDA)

Apply Matplotlib and Pandas together on a dataset.

EDA workflow:

```text
Dataset
   ↓
Load Data
   ↓
Inspect Data
   ↓
Check Missing Values
   ↓
Analyze Data
   ↓
Create Visualizations
   ↓
Identify Patterns
   ↓
Find Outliers
   ↓
Draw Insights
```

Topics practiced:

* `head()`
* `info()`
* `describe()`
* `isnull()`
* Creating new columns
* Finding maximum/minimum values
* Line charts
* Bar charts
* Scatter plots
* Histograms
* Box plots
* EDA dashboards

---

# 🧪 Mini EDA Dashboard

The repository includes a practical dashboard containing:

* Sales trend
* Expenses trend
* Monthly profit
* Customers vs sales

Example:

```python
fig, ax = plt.subplots(2, 2, figsize=(12, 8))

ax[0, 0].plot(df["Month"], df["Sales"])
ax[0, 0].set_title("Sales Trend")

ax[0, 1].plot(df["Month"], df["Expenses"])
ax[0, 1].set_title("Expenses Trend")

ax[1, 0].bar(df["Month"], df["Profit"])
ax[1, 0].set_title("Monthly Profit")

ax[1, 1].scatter(df["Customers"], df["Sales"])
ax[1, 1].set_title("Customers vs Sales")

plt.tight_layout()
plt.show()
```

---

# 📁 Repository Structure

```text
matplotlib-learning/
│
├── README.md
│
└── Matplotlib_Learning_Tutorial.ipynb
```

### `README.md`

Contains an overview of the repository, concepts learned, examples, and learning objectives.

### `Matplotlib_Learning_Tutorial.ipynb`

Google Colab notebook containing:

* Explanations
* Python code
* Visualizations
* Practice questions
* Placement-oriented concepts
* EDA examples

---

# 🛠️ Technologies Used

* **Python**
* **Matplotlib**
* **NumPy**
* **Pandas**
* **Google Colab**
* **Jupyter Notebook**

---

# ▶️ How to Use

### Option 1 — Google Colab

1. Open the notebook in Google Colab.
2. Run the cells from top to bottom.
3. Modify the examples.
4. Practice the exercises.
5. Experiment with different datasets.

### Option 2 — Local Jupyter Notebook

Install the required libraries:

```bash
pip install matplotlib pandas numpy jupyter
```

Then open the notebook using Jupyter:

```bash
jupyter notebook
```

---

# 🎯 Placement Preparation

This repository is designed not only to learn syntax but also to prepare for technical interviews.

Important questions covered include:

* What is Matplotlib?
* What is Pyplot?
* What is the difference between a bar chart and histogram?
* What is a scatter plot used for?
* What is a box plot?
* What is an outlier?
* What is a heatmap?
* What is the difference between Figure and Axes?
* What does `fig, ax = plt.subplots()` do?
* What is `alpha`?
* What does `cmap` mean?
* What is `dpi`?
* What does `bbox_inches="tight"` do?
* How do you create multiple subplots?
* How do you save a Matplotlib figure?
* How do you use Matplotlib with Pandas?
* Which visualization should be used for a particular problem?

---

# 📌 Learning Approach

The notebook follows a practical learning pattern:

```text
Concept
   ↓
Syntax
   ↓
Simple Example
   ↓
Explanation
   ↓
Customization
   ↓
Practice
   ↓
Placement Question
   ↓
Real-World EDA
```

---

# 🚀 Future Improvements

Planned additions to this repository:

* More real-world datasets
* Advanced Matplotlib techniques
* Seaborn integration
* Advanced EDA
* Statistical visualizations
* Interactive visualizations
* More placement questions
* Matplotlib mini projects
* Data-analysis projects

---

# 📚 Key Takeaway

Matplotlib is not just about creating charts.

The important skill is understanding:

> **What data do I have → What question am I asking → Which visualization communicates the answer best?**

This repository focuses on building that understanding through practical Python examples.

---

## ⭐ Author

**Ojaswi**

Learning Python, Data Analysis, and Data Visualization through hands-on projects and placement preparation.

---

## 📈 Learning Progress

```text
☑ Matplotlib Basics
☑ Pyplot
☑ Line Charts
☑ Bar Charts
☑ Histograms
☑ Scatter Plots
☑ Pie Charts
☑ Box Plots
☑ Heatmaps
☑ Customization
☑ Figure & Axes
☑ Subplots
☑ Pandas + Matplotlib
☑ Advanced Plotting
☑ Saving Figures
☑ Visualization Best Practices
☑ EDA

⬜ Advanced Seaborn
⬜ Advanced EDA Projects
⬜ Visualization Projects
```
