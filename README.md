# Analyzing-Network-graphs-in-r-programming-
#Analyzing network graphs 
install.packages("sna")
install.packages("igraph")
pacman::p_load(pacman, sna, igraph)

philant <- sample_pa(12, power = 1, directed = FALSE)
plot(philant)

###showing the degree of wach nodes in the graphs
degree(philant)

### measuring the betweennes of graphs 
philant <- sample_pa(n = 20, power = 1, directed = FALSE)
plot(philant)

### calculating the bewtweeness
betweenness(philant)

### calculating network densities
philant <- sample_pa(n = 12, power = 1, directed = FALSE)
plot(philant)

###checking the edge density 
philant <- sample_pa(n = 12, power = 1, directed = FALSE)
plot(philant)
philant_edge <- edge_density(philant, loops = FALSE)
philant_edge

### 20 nodes 
philant <- sample_pa(n = 20, power = 1, directed = FALSE)
plot(philant)
philant_edge <- edge_density(philant, loops = FALSE)
philant_edge

### 40 nodes 
philant <- sample_pa(n = 40, power = 1, directed = FALSE)
plot(philant)
philant_edge <- edge_density(philant, loops = FALSE)
philant_edge

### using gnp  with 20 nodes 
philant_gnp <- sample_gnp(20, 0.3, directed = FALSE, loops = FALSE)
plot(philant_gnp)
philant_edge <- edge_density(philant_gnp, loops = FALSE)
philant_edge


philant_gnp <- sample_gnp(20, 0.3, directed = FALSE, loops = FALSE)
plot(philant_gnp)
philant_edge <- edge_density(philant_gnp, loops = FALSE)
philant_edge


### identifying cliques in a graph
### creating a random graph 
philant_gnp <- sample_gnp(20,0.3, directed = FALSE, loops = FALSE)
plot(philant_gnp)

## calculate the size of the large size of the graph
clique_num(philant_gnp)

### displaying the number of cliques that are of a pariticular size
cliques(philant_gnp, min = 4)

cliques(philant_gnp, min = 3, max = 4)


### 
### creating a random graph 
philant_gnp <- sample_gnp(20,0.6, directed = FALSE, loops = FALSE)
plot(philant_gnp)

## calculate the size of the large size of the graph
clique_num(philant_gnp)

### displaying the number of cliques that are of a pariticular size
cliques(philant_gnp, min = 5)

cliques(philant_gnp, min = 4, max = 6)

### finding the components of a graph
philant_gnp <- sample_gnp( n = 30, p = 0.08, directed = FALSE, loops = FALSE)
plot(philant_gnp) 

### finding the components 
components(philant_gnp)

### taking a random walk on a graph 
philant <- sample_gnp(n = 30, p = 0.08, directed = FALSE, loops = FALSE)
plot(philant)
random_walk(philant,start = 26, steps = 8, stuck = "return")
random_walk(philant, start = 15, steps = 6, stuck = "return")
random_walk(philant, start = 11, steps = 6, stuck = "return")

