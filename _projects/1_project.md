---
layout: page
title: Is python fast or slow?
description: Identify if python is fast or slow by comparing it to the numpy library.
img: 
importance: 1
category: programming
related_publications: true
---
<H1>Purpose</H1>

The purpose of the assignment was to evaluate the impact of utilizing Python libraries, specifically focusing on NumPy, through an experiment comparing the efficiency of matrix multiplication operations using both iterative methods and NumPy functions. The primary goal was to assess the processing time difference between these two approaches and understand how it varies with the dimensionalities of the arrays.

The hypothesis posited that utilizing NumPy would significantly enhance the efficiency of matrix operations compared to the iterative method due to NumPy's implementation in machine language (C language), potentially resulting in faster computation times.
 
The experiment involved setting up various scenarios involving the multiplication of 1-D and 2-D arrays with different dimensionalities. For each scenario, the processing time was measured using the `timeit` library for both the iterative method and NumPy, and the results were compared.

Here is a small extraction of the code used to measure the impact of the utilization of numpy and iterative methods:

{% raw %}

```python
import timeit
def dot_product(v1, v2): # Dot product
return sum(v1[i] * v2[i] for i in range(len(v1)))
def matrix_vector_product(matrix, vector): result = []
for row in matrix: # Dot product
result.append(dot_product(row, vector)) return result
# Medium arrays
v1_medium = [i for i in range(1, 50)]
v2_medium = [i for i in range(1, 50)]
matrix_medium = [[i for i in range(1, 50)] for _ in range(1, 50)]
# Timing the execution
start_time = timeit.default_timer()
product_v_medium = dot_product(v1_medium, v2_medium) product_mv_medium = matrix_vector_product(matrix_medium, v1_medium) end_time = timeit.default_timer()
print(f"Dot product: {product_v_medium}")
# For large arrays, printing the entire product may not be practical, so we'll limit the output print_limit = min(len(product_mv_medium), 5)
print(f"Matrix-Vector dot product: {product_mv_medium[:print_limit]}")
print(f"Execution time for medium arrays: {end_time-start_time} seconds")
```

{% endraw %}


    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Table-1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The table has the values of the time taken to execute the operations.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Grafica-1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The graph compares the time execution of the two methods used.
</div>

The results of the experiment indicated that for dimensionalities below 10, both methods exhibited similar processing times, with a slight advantage towards NumPy. However, as the dimensionalities increased, NumPy showcased a substantial advantage over the iterative method, maintaining a consistent order of magnitude in processing times while the iterative method experienced significant increases.

The analysis of the results, coupled with insights from existing literature, attributed NumPy's superior performance to several factors: 
1. NumPy arrays store homogenous data types contiguously in memory, optimizing data retrieval efficiency.
2. NumPy's capability for parallel processing allows for simultaneous execution of tasks, leveraging computational power more efficiently.
3. NumPy functions are implemented in compiled languages like C, C++, and Fortran, which inherently have shorter processing times compared to Python's interpreted nature.
 
In conclusion, the experiment demonstrated the significance of utilizing external libraries like NumPy for computational efficiency, especially in handling large-scale data operations. The results underscored the importance of incorporating libraries into data-intensive tasks to achieve optimal performance.

<b>You can find the repository of this project in the respositories tab</b>

