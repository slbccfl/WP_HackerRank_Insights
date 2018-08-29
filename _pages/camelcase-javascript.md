---
ID: 86
post_title: CamelCase, JavaScript
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/camelcase/camelcase-javascript/
published: true
post_date: 2018-08-28 17:35:26
---
### Strategy: {#strategy} In my solution I convert all characters in the string to lowercase in a copy of the original string. I then compare each character in the original and copied strings to determine the number of capital letters. Add one more to this total and you have the number of words represented by the CamelCase string. 

###  {#data-structures}