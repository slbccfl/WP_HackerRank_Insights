---
ID: 91
post_title: Cavity Map, JavaScript
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/cavity-map/cavity-map-javascript/
published: true
post_date: 2018-08-28 17:42:47
---
### Strategy: {#strategy} A array of strings, each a line from the matrix, is passed to the function we are asked to write. I traverse the cells of the matrix, excluding those cells on the edges. The edge cells cannot be "cavities" in the definition of the problem, so I don't inspect them. The array is traversed for each row, and then each character of the string in that row is inspected using the string method "charAt" too. The edges are excluded because "cavities" are required to have higher values on all for sides. I then use a multi-line if statement to evaluate each cell to see if all the surrounding cells have higher values. If so, the cell value is replaced with an "X". This is done by replacing the row string, using the "substr" method to extract the strings before and after the cavity cell. Note that the a single parameter is used in the second substr call, returning all remaining characters in the string. I replaced the array passed, "grid", with a new array, "newGrid". I don't think I had to create a new array, I think I could have replaced the rows in the original array. But newGrid is returned in my solution to provide the expected output from the function.