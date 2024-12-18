# Matplotlib_analyss_02
# Data Analysis and Visualization Using Matplotlib

This guide introduces the basics of data analysis and visualization using the Matplotlib library in Python. Matplotlib is a powerful library for creating static, animated, and interactive visualizations.

---

## Table of Contents
1. **Introduction**
2. **Installation**
3. **Basic Plot Types**
    - Bar Plot
    - Line Plot
    - Scatter Plot
    - Pie Chart
    - Box Plot
    - Histogram
    - Violin Plot
    - Stem Plot
    - Stack Plot
    - Step Plot
4. **Advanced Features**
    - Legends
    - Subplots
5. **Saving Plots**
6. **Example Code**

---

## 1. Introduction
Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. It provides an object-oriented API for embedding plots into applications and supports a variety of plot types and customization options.

---

## 2. Installation
To install Matplotlib, use the following command:

```bash
pip install matplotlib
```

For Jupyter Notebook users, ensure that `ipympl` is installed for interactive visualizations:

```bash
pip install ipympl
```

---

## 3. Basic Plot Types
Below are some commonly used plot types in Matplotlib:

### Bar Plot
Used to compare categorical data:
```python
import matplotlib.pyplot as plt
categories = ['A', 'B', 'C']
values = [10, 20, 15]
plt.bar(categories, values)
plt.title('Bar Plot')
plt.show()
```

### Line Plot
Used to visualize data trends over intervals:
```python
x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]
plt.plot(x, y)
plt.title('Line Plot')
plt.show()
```

### Scatter Plot
Used to display the relationship between two variables:
```python
x = [5, 7, 8, 7, 2]
y = [99, 86, 87, 88, 100]
plt.scatter(x, y)
plt.title('Scatter Plot')
plt.show()
```

### Pie Chart
Used to display proportions:
```python
sizes = [30, 20, 50]
labels = ['A', 'B', 'C']
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
plt.title('Pie Chart')
plt.show()
```

### Box Plot
Used to visualize data distribution:
```python
import numpy as np
data = [7, 8, 6, 5, 6, 7, 8, 10]
plt.boxplot(data)
plt.title('Box Plot')
plt.show()
```

### Histogram
Used to display the frequency distribution:
```python
data = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5]
plt.hist(data, bins=5)
plt.title('Histogram')
plt.show()
```

### Violin Plot
Combines box plot with KDE:
```python
import seaborn as sns
data = [7, 8, 6, 5, 6, 7, 8, 10]
sns.violinplot(data=data)
plt.title('Violin Plot')
plt.show()
```

### Stem Plot
Used to emphasize discrete data points:
```python
x = [1, 2, 3, 4]
y = [10, 20, 15, 25]
plt.stem(x, y)
plt.title('Stem Plot')
plt.show()
```

### Stack Plot
Used to show composition over time:
```python
x = [1, 2, 3, 4]
y1 = [1, 2, 3, 4]
y2 = [2, 3, 4, 5]
plt.stackplot(x, y1, y2, labels=['A', 'B'])
plt.legend()
plt.title('Stack Plot')
plt.show()
```

### Step Plot
Useful for visualizing step changes:
```python
x = [1, 2, 3, 4, 5]
y = [10, 15, 20, 25, 30]
plt.step(x, y)
plt.title('Step Plot')
plt.show()
```

---

## 4. Advanced Features

### Legends
Add context to plots:
```python
plt.plot([1, 2, 3], label='Line A')
plt.plot([3, 2, 1], label='Line B')
plt.legend()
plt.title('Plot with Legend')
plt.show()
```

### Subplots
Multiple plots in one figure:
```python
fig, axs = plt.subplots(2, 2)
axs[0, 0].plot([1, 2, 3])
axs[0, 1].bar([1, 2, 3], [3, 2, 1])
axs[1, 0].scatter([1, 2, 3], [3, 2, 1])
axs[1, 1].pie([1, 2, 3])
plt.tight_layout()
plt.show()
```

---

## 5. Saving Plots
Save plots to your system as a PDF or JPG:

### Save as PDF:
```python
plt.plot([1, 2, 3])
plt.title('Save as PDF')
plt.savefig('plot.pdf')
```

### Save as JPG:
```python
plt.plot([1, 2, 3])
plt.title('Save as JPG')
plt.savefig('plot.jpg')
```

---

## 6. Example Code
Here is a complete example that combines multiple plots:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
plt.figure(figsize=(10, 6))

# Line Plot
plt.plot(x, np.sin(x), label='Sine Wave')

# Scatter Plot
plt.scatter(x, np.random.rand(len(x)), color='red', label='Random Points')

# Add Legend
plt.legend()

# Save the Plot
plt.title('Combined Plot Example')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.savefig('combined_plot.jpg')
plt.show()
```

---

Happy Visualizing!

