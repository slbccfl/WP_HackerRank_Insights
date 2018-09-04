---
ID: 66
post_title: Big Sorting, JavaScript Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/big-sorting/big-sorting-javascript-solution/
published: true
post_date: 2018-08-28 06:52:24
---
### Strategy: {#strategy} To sort numbers correctly, a comparator must be used. The following function is the typical "trick" used to sort an array of numbers: array.sort((a,b) => (a - b));.  This passes the function "(a,b) => (a - b)" as the comparitor for the sort. Without this function, the array will be sorted as strings instead of numbers. For this HackerRank problem, the strings are too long to be evaluated correctly has JavaScript numbers. Therefore we must compare the strings character by character to determine which is larger. But we do not have to do this character by character inspection for all of every pair of strings, If one string is longer than the other, then we know that the longer string is the larger number. Only when the strings are the same length do we begin to inspect character by character. But even then, we don't have to necessarily inspect everything pair of characters in the strings. As soon as we find one numeric character is greater than the other, we know that the string with the higher numeric character is also the larger overall numeric string. At that point we can break out of the loop. In my code I simply return the result, which also breaks the loop. I struggled a bit with the idea that we are passing a function as the parameter for the array sort() method, not 

*calling* the function. I wrote a named function to perform the comparisons. Of course the function required two parameters, one for each string that the sort method compares. But "arr.sort(compareFunction(a,b));", would not be correct. The function is passed as the parameter of the sort function. Including parameters for the passed function, indicates that the function should be called. We don't want to call compareFunction, we just should just pass the function to the sort method, like this: "arr.sort(compareFunction);".  The sort method uses the function we passed for each pair of array elements it compares. So the sort method will used the provided function, calling it as many times as it needs, to compare the array elements, to complete the sorting process.   
### <a href="https://github.com/slbccfl/hackerrank/blob/master/javascript/big-sorting/solution.js" target="_blank" rel="noopener">My Solution in GitHub</a>