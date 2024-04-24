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



    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

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
