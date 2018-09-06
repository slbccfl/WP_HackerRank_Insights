---
ID: 293
post_title: Mark and Toys, Java Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/mark-and-toys/mark-and-toys-java/
published: true
post_date: 2018-09-04 08:46:47
---
## Solution: {#solution} I sorted the array and then subtract each element from k, in order of increasing value, until k < 0. Then break out of the loop and return the value i, the number of elements that could be subtracted from k.