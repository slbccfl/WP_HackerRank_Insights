---
ID: 646
post_title: Cavity Map, Java Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/cavity-map/cavity-map-java/
published: true
post_date: 2018-09-06 16:21:12
---
Traverse each cell and check the adjacent cells values in comparison to the current cell. Set a boolean array to indicate those that are “cavities”. Since cells not on the borders of the grid cannot be “cavities” I traversed only those inside the borders. A boolean array is used to track cavities because altering the original grid would interfere with subsequent cell evaluations. After the relevant cells have been evaluated, output the original grid, character by character. But check if the cell position is “true” on the “cavities” boolean array. If so, output an “X” instead.