---
ID: 259
post_title: Maximizing XOR, Java Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/maximizing-xor/maximizing-xor-java/
published: true
post_date: 2018-09-04 08:08:01
---
### Strategy: {#strategy} Requires use of long, since unsigned integer is not supported in Java, and masking out the sign bit. This IS accomplished by reading the input into a long varible after performing the bitwise operation to mask the sign bit. The bitwise operation outputs a 64-big (long) result. Then a pair of loops is used to evaluate all combinations of 

*l* to *r*, and perform a bitwise compare of the combinations, keeping track of the highest value found resulting from this operation in the variable "maxXor".