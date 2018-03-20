# towerplacement implementation

1. we have to place tower  after getting the centers from clustering algorithm.
2. Eucledian distance has considered for placement.
3. This .java file contains only function **tower**.
4. You can add it to your code whose output is cluster centers and the clusters.

**Arguments in function 'tower'**
1. int[] medoid = array contains centers of clusters.
2. int[] tempclusters = array index as node number and the value corresponding to index shows that from which cluster this node belongs to.
3. int[][] a = Matrix with shortest pathway distances to each node for every node.
4. int [][] v = initial adjacency matrix of weighted undirected graph.
5. int n = no. of nodes in graph.
6. int k = no. of clusters.

**input**
1. adjacency matrix.
2. x and y coordinates of every node (for Eucledian distance calculation).

**output**
1. nodes, where we have to place tower.

**Algorithm**

1. first calculate Eucledian distance matrix.
2. find maximum and minimum form above matrix.
3. range=(maximum + minimumm)/2
4. find degree of each center.
5. consider MCS(master control system)=maximum degree center.
6. place first tower at MCS.
7. check next center, if it is in range claculated above 
8.    assign second tower 
9. else if check any other node of this cluster is in range of MCS if found
10.   assign tower to it
11. else
12.   check every node of this cluster which is in range of any tower already connected to MCS.
