---
ID: 267
post_title: >
  Permuting Two Arrays, JavaScript
  Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/two-arrays/permuting-two-arrays-javascript-solution/
published: true
post_date: 2018-09-04 08:21:04
---
### Functions:

##### twoArrays My solution was to sort both arrays, the first array in ascending order and the second array in descending order. Then traverse the arrays, adding pairs of values in sequence. As soon as a pair sums to less then the value k, a “NO” can be returned. If the traversal of the arrays completes, a “YES” is returned, indicating that there is a valid permutation has been found.