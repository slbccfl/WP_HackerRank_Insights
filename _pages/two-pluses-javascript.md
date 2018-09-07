---
ID: 247
post_title: 'Ema&#8217;s Supercomputer, JavaScript Solution'
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/two-pluses/two-pluses-javascript/
published: true
post_date: 2018-09-04 07:58:31
---
### Methods: {#methods}

##### main {#main} The main method is provided code that loads the STDIN data into an array "grid" and calls a function twoPluses that the we are to write. 

##### twoPluses {#findoptimalscorepair} In twoPluses the code iterates through each row and column. For each cell with a ‘G’, a score for the cell is determined. The score is the area of the first plus. For each ‘G’ cell a maxRange is set by a method scoreCell. Next maxRange is decremented to 0, setting tempMaxRange. For each value tempMaxRange, a tempGrid is cloned from grid,  and findGridHighScore is called to return the highest scoring second plus. The method tagPlus is used to temporarily mark out the cells used by the first plus. A highScore is updated if the product of a pair of scores is greater. The variable highScore is returned by this method. Note that "cloning" the grid is accomplished by using using "grid[r2].slice(0)" on each row. The slice(0) method will take of copy the array in row "r2". If the row "grid[r2]" had been assigned to tempGrid[r2], "grid[r2]" would be a reference variable, a pointer referring to the the same row. Meaning we would not have a copy, but be changing the same row regardless of whether we referred to it as "grid[r]" or "tempGrid[r]". 

##### findGridHighScore {#findmatrixhighscore} For each temporary grid passed to this method, with a first plus marked out by “tagPlus”, this method iterates through all rows and columns and scores each ‘G’ cell as a potential host for the second plus. “scoreCell” is used by this method to determine the maxRange available to each cell and the calculates a cell score that is the area of the plus (1 + (maxRange * 4)). The cell score is compared to the high cell score found so far, and is assigned to “highScore” if the new score is higher than any prior. “highScore” is returned after all cells have been evaluated. 

##### tagPlus tagPlus takes parameters that define the current first plus being evaluated and a temporary matrix. The method then marks the cells occupied by the first plus with ‘+’ so that “scoreCell” will consider these cells unavailable when it looks for non-‘G’ cells when evaluating where a second plus can be placed. 

##### scoreCell “scoreCell” examines the current ‘G’ cell in the context of the matrix to determine how long each “arm” of a plus could be in each of the cardinal directions from the current ‘G’ cell. To do this a “maxRange” is established by setting the minimum distance to the edges of the matrix. Then the distance from the ‘G’ cell is incremented up to the maxRange from the current ‘G’ cell and checking each of the four directions for whether and cell value not equal to ‘G’ is encountered. When a non-‘G’ cell is encountered, maxRange is updated to reflect the lower value for the maximum arm length of the plus and a break from the loop is executed. The maxRange is returned to the calling method “findGridHighScore”. 

### Data Structures: {#data-structures} This solution object uses simple two dimensional arrays to contain the matrix of ‘B’ and ‘G’ letters given as part of the initial input, to track candidate first pluses and is cloned to make temporary versions of matrix for scoring and evaluating the potential placement of the second plus. While each row remains a string, strings can be referenced as an array. So references like "grid[r][c]" are valid in the code. Rows and columns were made available to all methods as global variables, since these would be of common interest across most methods and they would be constant throughout a run.