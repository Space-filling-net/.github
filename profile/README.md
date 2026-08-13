The discrete space-filling problem consists in organizing spatial data so that geometric processing can be performed efficiently.

Space-filling curves solve this by mapping multidimensional data to a one-dimensional ordering. However, this unfolding can break local spatial relationships: nearby points may become distant in the resulting order.

We propose Space Filling Nets: instead of reducing the data to one dimension, we construct a regular multidimensional grid passing through all points. Each point receives a multidimensional index $[i,j,k,\ldots]$, preserving the spatial structure of the original point cloud.

The project is split into two repositories:

- "Squarenet": Python implementation for converting $[N,D]$ point clouds into structured grids.
- "Cartesian-Grid-Sort": mathematical details of the optimization algorithm.
