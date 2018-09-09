---
ID: 305
post_title: Sherlock and Array, Java Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/sherlock-and-array/sherlock-and-array-java/
published: true
post_date: 2018-09-04 08:51:16
---
### Methods:

##### solve I first check if the array length is 1, and if so return "YES". If the array has only one cell those to the left and right sum to 0. I traversed the array left to right creating an array (

*cumA*) that accumulates the sum of the current and all prior values. Here is an example of a given array “a” and array I created “cumA” array *a*: | 1 | 2 | 3 | 3 | array *cumA*: | 1 | 3 | 6 | 9 | I then traverse back down the array a accumulating a “*rightValue*” until the next cumA cell (a[i - 1]) is >= to the *rightValue*, and break out of this backward traversal if so. And then a final check for whether the left and right values are equal to determine if “YES” or “NO” will be returned.