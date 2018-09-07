---
ID: 100
post_title: Flipping bits, JavaScript
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/flipping-bits/flipping-bits-javascript/
published: true
post_date: 2018-08-28 18:14:00
---
### Strategy: {#strategy}

### Functions: {#methods}

##### flippingBits(N) The solution in JavaScript is accomplished with some very brief code. The function just returns "(~N) >>> 0", where N is the number passed to the function. The problem requires the bits of a 32-bit unsigned integer be flipped. In JavaScript numbers are 64-bit floating point numbers. Javascript bitwise operations convert to these to 32-bit signed integers for bitwise operations and then  convert result back into a JavaScript number.  The above bit of code performs two bitwise operations available in JavaScript. The ~N portions performs an XOR function on the variable "N" to "flip" the bits. This includes flipping an unwanted sign bit. The ">>> 0" portion is doing a "Zero-fill right shift" for 0 positions. Which has no effect on the bits representing the number, but has the by-product of always setting the sign bit to 0.