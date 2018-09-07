---
ID: 98
post_title: Flipping bits, Java
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/flipping-bits/flipping-bits-java/
published: true
post_date: 2018-08-28 18:12:47
---
### Strategy: {#strategy} Requires use of long, since unsigned integer is not supported in Java, and masking out the sign bit. This can be accomplished and output with this line alone: "System.out.println(~number & 0xffffffffl);" 

### Methods: {#methods}