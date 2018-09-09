---
ID: 302
post_title: Sherlock and Array, JavaScript Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/sherlock-and-array/sherlock-and-array-javascript/
published: true
post_date: 2018-09-04 08:50:49
---
### Methods:

##### balancedSums This function traverses left to right and right to left in the array "

*arr*" concurrently, accumulating *leftSum* and *rightSum*. A right index ("*r*") traverses "up", from the left, and a left index ("*l*") traverses "down", from the right. If they cross (*l* < *r*) the loop terminates. For each loop, the left and right sums are compared. If the *leftSum* is greater than the *rightSum*, the next cell value referenced by the right index ("*r*") is added to *rightSum*, and *r* is decremented. Conversely, if the *rightSum* is greater than the *leftSum*, the next cell value referenced by the left index ("*l*") is added to the *leftSum* and* l* is incremented. If neither of these is true, *leftSum* and *rightSum* are equal, the  next value from the left and right cells are compared and whichever is less is added to it's respective sum and it's respect index is incremented or decremented. And finally, if these are equal too, both are added to the sums and both indexes are progressed. After this loop completes, a "YES" is returned if the left and right sums are equal and the indexes are equal. Otherwise a "NO" is returned.