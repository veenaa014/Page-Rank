# Page-Rank
Implementation of Page Rank algorithm in Apache Spark

There are 100 nodes (n = 100) in the small graph and 1000 nodes (n = 1000) in the full graph, and m = 8192 edges, 1000 of which form a directed cycle (through all the nodes) which ensures that the graph is connected. It is easy to see that the existence of such a cycle ensures that there are no dead ends in the graph. There may be multiple directed edges between a pair of nodes, and your solution should treat them as the same edge. The first column in graph-full.txt refers to the source node, and the second column refers to the destination node.

Implementation: 
Assume the directed graph G = (V,E) has n nodes (numbered 1,2,...,n) and m edges, all nodes have ositive out-degree, and M = [Mji]n×n is a 𝑛 × 𝑛 matrix as defined in class such that for any 𝑖,𝑗 ∈⟦1, 𝑛⟧:
Mji = { 1/deg(i), if i -> j ∈ E,  0 otherwise

Here, deg(i) is the number of outgoing edges of node i in G. If there are multiple edges in the same direction between two nodes, treat them as a single edge. By the definition of PageRank, assuming 1−β to be the teleport probability, and denoting the PageRank vector by the column vector r, we have the following equation:
    r =(1−β)/n + βMr
    
Matrix M can be large and should be processed as an RDD in your solution.
    
Compute the followings for the larger dataset:
* List the top 5 node ids with the highest PageRank scores.
* List the bottom 5 node ids with the lowest PageRank scores.


