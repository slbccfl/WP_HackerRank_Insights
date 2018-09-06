---
ID: 465
post_title: 'Dijkstra: Shortest Reach 2, Java Solution'
author: slbarnes
post_excerpt: ""
layout: page
permalink: >
  http://localhost/index.php/dijkstrashortreach/dijkstrashortreach-java/
published: true
post_date: 2018-09-04 18:29:24
---
This solution implements the Dijkstra algorithm for finding the path. See the following references for descriptions and graphics of Dijkstra’s algorithm. <a href="https://en.wikipedia.org/wiki/Dijkstra's_algorithm" target="\_blank">Wikipedia</a> <a href="http://www.geeksforgeeks.org/greedy-algorithms-set-6-dijkstras-shortest-path-algorithm/" target="\_blank">GeeksforGeeks</a> 
### Classes outside the Solution class: {#classes-outside-the-solution-class}

#### Edge {#edge} A class defined to represent an edge in the graph, includes attributes for weight, starting node and ending node. 

#### Node {#node} A class defined to represent a node in the graph. Attributes include the nodeID, as defined by the input, distance from the starting point in the graph, and an adjacencyList of the egdes that link to this node. When a node is instantiated, distance is set to Long.MAX_VALUE, to represent infinity, and a new HashMap is instantiated for the adjacencyList. An edge is optionally passed to the constructor for the node. If an edge is included, the node being instantiated is identified as the starting or ending node of the edge and the other node is set as the adjacentNode and put in the adjacencyList for the node. 

### Solution Class fields: {#solution-class-fields}

#### graph {#graph} A HashMap that is the internal representation of the graph. 

#### settled {#settled} A HashMap used to track what nodes have been settled per the Dijkstra algorithm. 

#### numberOfNodes and numberOfEdges {#numberofnodes-and-numberofedges} The initial inputs for the current run. 

#### startTime {#starttime} This field is used for timing the algorithm and is not directly relevant to the solution. 

### Methods: {#methods}

#### main {#main} The main method acts as something of a wrapper for the primary method in this solution, dijkstraSPT. The STDIN data is loaded before executing that method, and then constructing and outputting the STDOUT string after. One thing to note in the solution is the use of BufferedReader to read STDIN in an attempt to gain efficiency. Similarly, StringBuilder is used to compose the STDOUT string, also in an attempt to gain efficiency there. 

#### timeStamp {#timestamp} The timeStamp method is a method only used during development to evaluate efforts to optimize the code efficiency. 

#### addToGraph {#addtograph} This method is used to add edges to the internal representation of the graph during the initial load of data from STDIN by the main method. 

#### dijkstraSPT {#dijkstraspt} This method uses a TreeMap (nodesQueue) to collect and hold the nodes to be evaluated on the frontier of analysis. queueNodeEdges is initilized, using queueNodeEdges to load the startNode. And then a loop runs findLowestEdge and queueNodeEdges until there are no more unsettled nodes in nodesQueue to process. At this point the Dijkstra algorithm has been completed. 

#### queueNodeEdges {#queuenodeedges} Broadly, this method takes in and returns the nodesQueue, also taking in a node to be added to this queue. But it’s more complicated than that. The method iterates through each of the edges that link to the node being enqueued. For each adjacent node that has not been previously settled, the distance of the current node + the weight of the connecting edge is compared to the distance the adjacent node currently has and updates that distance if the new value is lower. And the adjacent node is enqueued in nodesQueue under the new distance value. 

#### findLowestEdge {#findlowestedge} The method takes in the TreeMap nodesQueue and disqueues the node in nodeQueue with the lowest distance. While getting the lowest distance node should just be a matter of executing the nodesQueue.pollFirstEntry() method. Polling has to continue until a node that is settled is found and the LinkedList of nodes for a given value has to be maintained too. The LinkedList within nodesQueue takes into account that there may be multiple nodes that are the same distance from the starting node. 

### Data Structures: {#data-structures}

#### TreeMap<Long, LinkedList>nodesQueue {#treemaplong-linkedlistnodesqueue} This structure is used to store the nodes to be evaluated along the frontier of analysis. The Long key is used to store distance from the startNode. The LinkedList then allows for multiple nodes having the same distance from the startNode. The 

<a href="https://docs.oracle.com/javase/7/docs/api/java/util/TreeMap.html" target="\_blank">TreeMap</a> data structure is just about perfect for managing a queue of nodes where we want the lowest distance node from that collection. The <a href="https://docs.oracle.com/javase/7/docs/api/java/util/TreeMap.html#pollLastEntry()" target="\_blank">pollFirstEntry</a> method of this class “Removes and returns a key-value mapping associated with the least key in this map, or null if the map is empty.” 
## TestSolution - junit testing method {#testsolution---junit-testing-method}

### Methods: {#methods-1}

#### testAddToGraph {#testaddtograph}

#### testQueueNodeEdges {#testqueuenodeedges}

#### testDijkstraSPT {#testdijkstraspt}