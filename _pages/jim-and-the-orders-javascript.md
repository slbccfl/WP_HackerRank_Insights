---
ID: 285
post_title: Jim and the Orders, JavaScript Solution
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/jim-and-the-orders/jim-and-the-orders-javascript/
published: true
post_date: 2018-09-04 08:42:32
---
### Functions:

##### jimOrders I create an array servings and calculate the serving time (

*serveTime*) for each customer. For each customer in the orders array, a servings array entry is created with with customer number and the *serveTime*, resulting in a new two dimensional array. I then sort this array by serving time. Note the use of a comparitor in the sort, necessary for correct sorting of numbers in JavaScript. The resulting new order is used to push customer numbers into an array of customer numbers in the required order (*returnArr*).