---
layout: page
title: Search Algorithms
description: Explore different approaches to solve a problem
img: 
redirect:
importance: 1
category: programming
---

<H1>Purpose</H1>

The assignment focused on exploring fundamental concepts of search algorithms in Artificial Intelligence through the solution of two distinct problems.

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/polygons.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The first problem involved finding the shortest path between two points on a plane containing convex polygonal obstacles. The key considerations included determining the number of states and paths, understanding the necessity of straight-line segments in the shortest path, defining an appropriate state space, and implementing necessary functions for the search problem. Various search algorithms were applied to solve this problem, with A* and Uniform Cost Search demonstrating superior performance.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/missionaries.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The second problem, famously known as the Missionaries and Cannibals problem, required transporting three missionaries and three cannibals across a river using a boat with specific constraints. The problem formulation involved defining states, actions, the initial state, the transition model, the goal test, and the path cost. Different search algorithms were employed to solve this problem, and all algorithms produced optimal solutions due to the nature of the problem.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/results-poly.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The results for the first problem showed that both A* and Uniform Cost Search algorithms were the most effective in identifying the optimal path from the initial state to the goal state. A* particularly excelled due to its informed nature, leveraging heuristic information to efficiently navigate the solution space. The results for the second problem showed that all algorithms produced optimal solutions with the same number of steps, reflecting the inherent characteristics of the problem.

In summary, the detailed solutions for each problem demonstrated the effectiveness of various search algorithms in different problem domains. The selection of appropriate algorithms based on problem characteristics and constraints played a crucial role in achieving optimal solutions.

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
