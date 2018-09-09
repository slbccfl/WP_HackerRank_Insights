---
ID: 312
post_title: Missing Numbers, JavaScript Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/missing-numbers/missing-numbers-javascript/
published: true
post_date: 2018-09-04 08:55:04
---
### Functions:

##### function missingNumbers(arr, brr) I sort both arrays ("

*arr*" and "*brr*"), using a comparitor since the cell values are numbers. Also a *resultArr* is initialized as an empty array. An outer loop iterates through the *brr* array, with an index *i*. Remember that *brr* is guaranteed to be as long or longer than *arr*. As *brr* is traversed, if the values indexed by *brr[i]* and *arr[j]* are not equal, values are pushed from the brr array into the resultArr, and i incremented until the values are equal again. This results in duplicate values being skipped in creating the *resultArr*. After the outer loop completes, *resultArr* is returned.