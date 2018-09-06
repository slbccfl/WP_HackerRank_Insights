---
ID: 239
post_title: 'Ema&#8217;s Supercomputer'
author: slbarnes
post_excerpt: ""
layout: page
permalink: http://localhost/index.php/two-pluses/
published: true
post_date: 2018-09-04 07:53:32
---
## <a href="https://www.hackerrank.com/challenges/two-pluses" target="_blank" rel="noopener">Problem Description on HackerRank</a> Uses two dimensional arrays to finds the optimal placement of two pluses on a matrix to maximize the product of the areas covered by the pluses. 

### Strategy: {#strategy} This solution iterates through the matrix of ‘B’ and ‘G’ letters and scores each cell that has a ‘G’ for potentially hosting the first of the two pluses. When I say a cell potentially hosts a plus I mean that the cell would be the point at which the two segments cross. Or put another way, the cell from which the four arms of the plus originate from. All the potential sizes,lengths of arms, of each plus is considered at each location too. And as each of these pluses are considered, the solution examines and scores all the remaining cells as the potential host of the second plus. In evaluating the second plus, the maximum size of plus is all that has to be considered. It is important to vary the size of the first plus as it’s maximum size (arm length) will not necessarily yield the optimal result, “…the maximum product of their areas.” It is possible that a smaller first plus, at a given location, would allow a second plus to be larger, where the increase in area of the second plus outweighs the reduction in area of the first plus. 

## [JavaScript Solution][1]

## [Java Solution][2]

 [1]: /index.php/two-pluses/two-pluses-javascript
 [2]: /index.php/two-pluses/two-pluses-java