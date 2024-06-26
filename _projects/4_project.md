---
layout: page
title: The 8 queens and puzzle problem
description: Evaluate the performance of different search algorithms
img:
importance: 3
category: programming
---

<H1>Purpose</H1>

The assignment aimed to evaluate the performance of different local search algorithms in solving two classic AI problems: the 8-puzzle and the 8-queens problem. The primary objective was to measure the search cost and the percentage of solved problems for each algorithm across many instances. Four algorithms were evaluated: Hill Climbing (Steepest-Ascent and First-Choice variants), Hill Climbing with Random Restart, and Simulated Annealing.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/puzzle.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/queens.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The 8-puzzle problem involves arranging tiles to a specified configuration in a 3x3 grid, aiming to achieve the goal state. On the other hand, the 8-queens problem requires placing eight queens on an 8x8 chessboard such that no two queens threaten each other. Hypotheses were formulated based on the theoretical background of the algorithms, anticipating that Simulated Annealing would outperform the others due to its probabilistic nature, while hill climbing variants might struggle due to their susceptibility to local optima.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/results-8queens.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The results confirmed the hypotheses, demonstrating that Simulated Annealing was the most effective algorithm for both problems, albeit with higher computational time. The hill climbing variants struggled due to their deterministic nature and vulnerability to local optima. The variability in results highlighted the importance of selecting the right algorithm for a given problem and conducting thorough testing to assess its effectiveness.
 
In conclusion, the experiment emphasized the significance of algorithm selection and testing in problem-solving scenarios. While Simulated Annealing emerged as the most optimal choice for these problems, the trade-off between solution quality and computational time must be considered when choosing an algorithm.

<b>You can find the repository of this project in the respositories tab</b>
