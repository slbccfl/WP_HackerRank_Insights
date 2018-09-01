---
ID: 66
post_title: Big Sorting JavaScript Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/big-sorting/big-sorting-javascript-solution/
published: true
post_date: 2018-08-28 06:52:24
---
### Strategy: {#strategy} To sort numbers correctly, a comparator must be used. This function is the typical "trick" for this: array.sort((a,b) => (a - b));  For this problem, the strings are too long to be evaluated correctly has JavaScript numbers. Therefore we must compare the strings character by character to determine which is larger. We do not have to do this character by character inspection every pair of strings, If one string is longer than the other, then we know that the longer string is the larger number. If the strings are the same length, only then do we begin to inspect character by character. But as soon as you find one numeric character is greater than the other, we know that the string with the higher numeric character is also the larger overall numeric string, and we can break out of the loop. In my code I simply return the result, which will also break the loop. I struggled a bit with the idea that we are passing a function as the parameter for the sort method, not calling the function. I wrote a named function to perform the comparisons. Of course the function required two parameters, one for each string that would be compared by the sort method. But "arr.sort(compareFunction(a,b));", would be incorrect. The function is passed as the parameter for sort, including parameters for the passed function, indicates that the function should be called. We don't call compareFunction, we just pass it to the sort method, like this: "arr.sort(compareFunction(a,b);".  The sort method uses the function we passed for each pair of array elements it compares, so the sort method will used the provided function, calling it as many times as it needs, to compare the array elements, to complete the sorting process. 

<a href="https://github.com/slbccfl/hackerrank/blob/master/javascript/big-sorting/solution.js" target="_blank" rel="noopener">My Solution</a> 
### Methods: {#methods}

#### main {#main} The main method is … 

### Data Structures: {#data-structures}