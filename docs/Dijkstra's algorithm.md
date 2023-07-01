- generally for finding shortest paths btwn nodes in a graph
- grows like a circular wavefront (visits all closest nodes first, no leap of exploration)
	- relatively slow in certain topologies

- procedure
	1. mark all nodes unvisited (infinite cost)
	2. relabel paths w cost at every intersection, mark each node as visited
	3. continue until destination is found
	4. trace your way back by following each node's parents up to staring node