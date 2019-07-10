

Voxelizer
------------------------------------------------
by Rama Hoetzlein (ramakarl.com)
This code is licensed CC0, public domain
<br><br>
The interface lets you move the vertices of the triangle.
Use A,S,D,F or space to change the technique.
<br><br>
Code gives the basic math for the 3D voxelization of a triangle.
<br><br>
Four techniques are provided. The first three are triangle-box intersection tests, and test the triangle against every voxel in the domain O(V^3). The last is a direct DDA Rasterizer, which only visits the voxels touched by the triangle O(Vt).
<br><br>
1- **Explicit edge tests**: Use edge fuctions to explicitly test each edge of triangle. 27 tests/voxel.<br>
2- **Schwarz-Seidel tests**: Recent paper that uses a reduced, efficient set of edge tests. 9 tests/voxel.<br>
3- **Akenine-Moller tests**: The first paper to provide efficient, exact voxelization. 18 tests/voxel.<br>
4- **DDA Rasterizer**: Starts at one corner and scans along the edges, performing a DDA (2D differential analyzer) to fill the interior of the triangle. This technique is much faster for voxelization as it only visits interior voxels.<br>

Sources:
Schwarz & Seidel, 2010, Fast Parallel Surface and Solid Voxelization on GPUs, http://research.michael-schwarz.com/publ/files/vox-siga10.pdf
Akenine-Moller, 2001, Fast 3D Triangle-Box Overlap Testing, https://fileadmin.cs.lth.se/cs/Personal/Tomas_Akenine-Moller/pubs/tribox.pdf
Pineda, 1998, A Parallel Algorithm for Polygon Rasterization (Edge Functions),  https://www.cs.drexel.edu/~david/Classes/Papers/comp175-06-pineda.pdf

<br><br>
Rama Hoetzlein (c) 2019

