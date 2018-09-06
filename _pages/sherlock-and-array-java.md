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
I traversed the array left to right creating an array that accumulates the sum of the current and all prior values. Here is an example of a given array “a” and array I created “cumA” ——————— | 1 | 2 | 3 | 3 | ——————— | 1 | 3 | 6 | 9 | ——————— I then traverse back down the array a accumulating a “rightValue” the next cumA cell (a[i - 1]) is >= to the rightValue. A final check for whether the left and right values are equal to deterine if “YES” or “NO” will be returned.