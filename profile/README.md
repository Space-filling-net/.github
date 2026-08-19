The discrete space-filling (or serialization) problem consists in organizing spatial data so that geometric processing can be performed efficiently. One want to sort a dataset in a spatially coherent way rather than just arbitrary as they come up in memory.

Space-filling curves solve this by mapping multidimensional data to a one-dimensional ordering. However, this unfolding can break local spatial relationships: nearby points may become distant in the resulting order.

`Space-filling nets`, instead of reducing the data to one dimension, construct a regular multidimensional grid passing through all points. Each point receives a multidimensional index $[i,j,k,\ldots]$, preserving the spatial structure of the original point cloud. Thus a space-filling net is nothing more but a `multi-dim sorting algorithm` with a grid based storage instead of standard linear $0,1,2,\ldots$ storage. Kind of an adaptative, bijective voxel structure.

The project is split into two repositories:

- [Squarenet](https://github.com/Space-filling-net/SquareNet): Python implementation for converting $[N,D]$ point clouds into structured grids.
- [Cartesian Grid Sort](https://github.com/Space-filling-net/Cartesian-Grid-Sort): mathematical details of the optimization algorithm.


![Space Filling Net](https://raw.githubusercontent.com/Space-filling-net/.github/main/mesh.jpg)
