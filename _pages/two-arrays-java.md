---
ID: 269
post_title: Permuting Two Arrays, Java Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/two-arrays/two-arrays-java/
published: true
post_date: 2018-09-04 08:22:38
---
My solution was to sort both arrays, the first array in ascending order and the second array in descending order. Then traverse the arrays, adding pairs of values in sequence. As soon as a pair sums to less then the value k, a “NO” can be returned. If the traversal of the arrays completes, a “YES” is returned, indicating that there is a valid permutation has been found. 
### Methods:

##### validatePermutations Includes a loop to traverse the arrays as described above, comparing the summed values to 

*k*.