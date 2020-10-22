# Degree Distributions

- Random graphs differ from real world networks as
  - Real world networks show strong clustering or network transitivity
    - A network shows clustering if the probability of two vertices being connected by an edge is higher when the vertices in question have a common neighbour
    - In many real world networks, clustering coefficients have a high value
  - In a random network, there will be very few nodes with a large degree, and with a small degree
    - Degree distribution for a graph generated by G(n, p)
      - Each node has (n-1) tries to get edges
      - Each try is a success with probability p
      - Binomial distribution gives us the probability that a node has degree k 
        - P(deg(v) = k) = <sup>n-1</sup>C<sub>k</sub> p<sup>k</sup>(1-p)<sup>n-1-k</sup>
      - The distribution is a Poisson distribution for large n
        - p<sub>k</sub> = (z<sup>k</sup>e<sup>-z</sup>)/k!
      - For large n, the distribution is independent of size
      - This distribution makes it deviate significantly from real world networks

- Limitations of Random Networks
  - Degree distribution differs from real world, which usually follow power-law
  - Clustering coefficients are too small in ER
  - Real world networks are not generated randomly