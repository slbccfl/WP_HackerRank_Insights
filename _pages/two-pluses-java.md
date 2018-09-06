---
ID: 249
post_title: 'Ema&#8217;s Supercomputer, Java Solution'
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/two-pluses/two-pluses-java/
published: true
post_date: 2018-09-04 07:59:11
---
### Methods: {#methods}

#### main {#main} The main method is almost exclusively dedicated to loading the STDIN data. The inputs for this problem are loaded into integer variables “rows” and “columns” and the matrix of letters are loaded into a two dimensional array (char[][]) called “matrix” using nextLine and charAt to get each character. Then the required STDOUT is provided by a println of the returned value from a method “findOptimalScorePair”. 

#### findOptimalScorePair {#findoptimalscorepair} In “findOptimalScorePair” the code iterates through each row and column. For each cell with a ‘G’, a score for the cell is determined. The score is the area of the first plus. For each ‘G’ cell a “maxRange” is set by a method “scoreCell”. Next maxRange is decremented to 0, setting tempMaxRange. For each value “tempMaxRange”, a tempMatrix is cloned from matrix, and “findMatrixHighScore” is called to return the highest scoring second plus. The method “tagPlus” is used to temporarily mark out the cells used by the first plus. A highScore is updated if the product of a pair of scores is greater. The variable highScore is returned by this method. 

#### findMatrixHighScore {#findmatrixhighscore} For each temporary matrix passed to this method, with a first plus marked out by “tagPlus”, this method iterates through all rows and columns and scores each ‘G’ cell as a potential host for the second plus. “scoreCell” is used by this method to determine the maxRange available to each cell and the calculates a cell score that is the area of the plus (1 + (maxRange * 4)). The cell score is compared to the high cell score found so far, is is assigned to “highScore” if the new score is higher than any prior. “highScore” is returned after all cells have been evaluated. 

#### tagPlus {#tagplus} tagPlus takes parameters that define the current first plus being evaluated and a temporary matrix. The method then marks the cells occupied by the first plus with ‘+’ so that “scoreCell” will consider these cells unavailable when it looks for non-‘G’ cells when evaluating where a second plus can be placed. 

#### scoreCell {#scorecell} “scoreCell” examines the current ‘G’ cell in the context of the matrix to determine how long each “arm” of a plus could be in each of the cardinal directions from the current ‘G’ cell. To do this a “maxRange” is established by setting the minimum distance to the edges of the matrix. Then the distance from the ‘G’ cell is incremented up to the maxRange from the current ‘G’ cell and checking each of the four directions for whether and cell value not equal to ‘G’ is encountered. When a non-‘G’ cell is encountered, maxRange is updated to reflect the lower value for the maximum arm length of the plus and a break from the loop is executed. The maxRange is returned to the calling method “findOptimalScorePair”. 

### Data Structures: {#data-structures} This solution object uses simple two dimensional arrays to contain the matrix of ‘B’ and ‘G’ letters given as part of the initial input, to track candidate first pluses and is cloned to make temporary versions of matrix for scoring and evaluating the potential placement of the second plus. These are primitive array variables, as opposed declaration of an ArrayList within an ArrayList. This made cell referencing very straight forward and we can expect that the performance in accessing these arrays to be very good. The primary matrix was declared as char[][] rather than string[][]. Since only a single letter is ever used in a cell, this kept things tight and avoided making any mistakes of entering more than one character in a cell as a string[][] array would have allowed. Rows and columns were made available to all methods as package variables, since these would be of common interest across most methods and they would be constant throughout a run. You may ignore the package variable score[][]. This appears to be a remnant of an unused idea and I’m not taking time to remove references to it and resubmit.