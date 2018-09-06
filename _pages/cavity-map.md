---
ID: 75
post_title: Cavity Map
author: slbarnes
post_excerpt: ""
layout: page
permalink: http://localhost/index.php/cavity-map/
published: true
post_date: 2018-08-28 07:06:45
---
Display a grid with "X" for each cell where each adjacent cell has a lower value (depth). 
## <a href="https://www.hackerrank.com/challenges/cavity-map/problem?h_r=internal-search" target="_blank" rel="noopener">HackerRank Problem Description</a>

## Solution: {#solution} Traverse each cell and check the adjacent cells values in comparison to the current cell. Set a boolean array to indicate those that are “cavities”. Since cells not on the borders of the grid cannot be “cavities” I traversed only those inside the borders. A boolean array is used to track cavities because altering the original grid would interfere with subsequent cell evaluations. After the relevant cells have been evaluated, output the original grid, character by character. But check if the cell position is “true” on the “cavities” boolean array. If so, output an “X” instead. 

## [Java Solution][1]

## [JavaScript Solution][2]

 [1]: /index.php/cavity-map/cavity-map-java
 [2]: /index.php/cavity-map/cavity-map-javascript