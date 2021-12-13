---
layout: case
title: Lab2 Case Discription.
image_path: ""
thumb: lab2.jpg
main-pic: ScreenShot_ImprovingDemo.jpg
summary: Here is a detailed description of Lab2's functionality and analysis.
nav-class: case-studies
permalink: case-studies/one/
date: 2021-12-12 2:32:00 -0600

---

Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua.

* For the Table class, it represents a table with a certain number of dishes, so it needs to contain
the maximum number of dishes that can hold, the current number of dishes, and the content
variables of the dishes (randomly generated during construcKon).
* For the Customer class, it represents a customer who has a demand for dishes, so it needs to
contain the maximum number of wanted, the current number of wanted, and the variable of
the wanted content (randomly generated during construcKon).
* For the TipBox class, it represents a box for storing Kps, so a variable that contains the current
number of Kps is needed.

When the three objects are successfully constructed, the first dish of the Table is taken out in each cycle to determine whether this dish is needed in the customer's wanted. If it is needed, remove the corresponding wanted and put a random amount of Kps into the TipBox , And then enter the next cycle; if the dish is not needed in wanted, then enter the next cycle. UnKl at least one of Table or Customer is empty.

> In figure2, we can see that the lower right corner of the screenshot of the demo application running on the web side shows the execution time of each run after 40 runs. We can easily find that after 27 runs, the next run time is much larger than the previous run time, which leads to our data performance
is not good enough. After consulting the information, I found that the :innerHTML attribute consumes memory and CPU during the execution of the "+=" operation, causing the subsequent operations to be slower than the previous ones. Optimization idea: Add the data that needs to be printed to the web page in each loop before the end of each loop, and then use the "+=" operation to add to the innerHTML attribute. Finally, the optimized result is shown in figure3 (the pre-optimized part is annotated in the js code main.js, and the optimized code is added as the final code, which is saved in main.js in the code folder):
