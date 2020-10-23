# A checklist of exploratory data analysis steps for networks

## Basic structural questions to ask yourself

- Is the graph directed or undirected?
- Is the graph fully observed? In particular, are you working with an induced subgraph of a much larger graph?
- Does the graph have any special structure (i.e. it is a tree, a forest, etc)?
- Can nodes connect to themselves with an edge?
- Are edges weighted, or are multiple edges between the same pair of nodes allowed? This is a key thing to check, since lots of edgelist contain duplicates that shouldn't be there

## Basic counts

- How many nodes are there?
- How many edges are there?
- What is the density of the graph?
- What is the clustering coefficient of the graph? What portion of triangles are closed?
- How many components are there in the graph and how big are they?
- What is the diameter of the graph
- How many isolated singletons are there?

## Check the degree distribution

- Plot histograms of the in-degree and out-degree distributions of the network
- Look at the ~30 nodes with the highest and lowest in-degree and out-degree

## Check the spectral decomposition

- Check the left and right singular vectors for localization with an IPR pairs plots
- If feasible, plot the singular vectors themselves to check for patterns like orthogonal polynomials
- Make a screeplot of the top singular values
- Estimate the rank of the adjacency matrix if possible

## Node covariates

- Check how much covariate information is missing
- Check for patterns in missingness according to node orders (through time), or as a function of node degree
