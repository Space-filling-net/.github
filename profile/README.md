The space-filling problem, in its discrete form, can be understood as the problem of structuring or reordering spatial data so that geometric processing, such as triangulation, can be performed more efficiently.

A common approach is to reorder the data using space-filling curves. These curves have the remarkable property of traversing the entire multidimensional domain through a one-dimensional ordering, making it possible to process spatial data as if it were one-dimensional.

However, reducing a multidimensional point set to a one-dimensional ordering inevitably comes at a cost: part of the local spatial structure is lost during the unfolding process. Points that are close in the original space may become distant in the resulting ordering.

To better align the representation with the intrinsic spatial structure of the point cloud, we propose the concept of a Space Filling Net: instead of searching for a one-dimensional traversal of the domain, we search for a regular multidimensional grid that passes through all points of the set.

Each point can then be assigned a multidimensional index, such as $[i,j,k,\ldots]$, providing a discrete coordinate system that preserves the local structure of the original point cloud as faithfully as possible.

This organisation is organised as follow:

- `Squarenet` provides a python package implementation that fills the gap between the raw point set given as a flat [N, D] dataset and it's grided view [n1, n2,...,nd, D] based on the net.
- `Cartesian-Grid-Sort` details the mathematical optimization algorithm used inside the package, to make it fully understandable for intersted users.
