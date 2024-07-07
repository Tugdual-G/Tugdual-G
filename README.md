# Conformal transformations of triangular meshes : [transformal](https://github.com/Tugdual-G/transformal)
Why are computer graphics nerds obsessed with turning rabbits into spheres? I think I've figured it out.

<img src="https://raw.githubusercontent.com/Tugdual-G/transformal/main/animation_crop.gif" align="center" width="50%"></img>

# Real-time rendering of the Mandelbrot set gost-points : [budack](https://github.com/Tugdual-G/budack)
I don´t think of fractals as being aesthetically interesting, nevertheless this one caught my interest so I tried to make it look good :

<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/graysclezoom1.png" align="center" width="100%"></img>

#  Parallel multigrid Solver : [multigrid](https://github.com/Tugdual-G/multigrid)
The hello world equation with a twist.

The solution of the Poisson equation depends on the global information over the domain, therefore finding a good parallel computing scheme is far from trivial.

<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/vismulti.png" width="50%"></img>


#  Cubed sphere
**Parallel computing on the gnomonic equiangular grid, performed by modifying [pyRSW](https://github.com/pvthinker/pyRSW), a discrete exterior calculus based model.**

Out of the box pyRSW can compute flow on curved surfaces but cannot handle skewed grids, moreover the topology of the cubed sphere asks for tailor-made parallel communications between processes.
For this purpose, the module uses a "stairway" cube net in order to simplify the implementation of the communications (see the image below). 
For now, the cubed sphere module is able to compute surfaces waves correctly. More work is needed to find a consistent reconstruction of fluid velocity at the grid vertices to handle the vorticity induced by the rotation of the sphere. 
This issue is due to the severe non-orthogonality at the corners of the cube's faces. [Link to the AGU article](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2021MS002663)

<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/animvue2.gif" width="33%"></img>
<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/animsphere.gif" width="33%"></img>
<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/snapsphere.png" width="33%"></img>

#  Surface tension module for [Fluid2d](https://github.com/Tugdual-G/Fluid2d/tree/droplet)
**With the help of [Malo Kerebel](https://github.com/Malo-Kerebel)**

This is one of the first projects I participated in.

Here we tried to implement an Eulerian description of the droplet interface using the level-set method in the context of the Boussinesq approximation of the  Navier-Stockes equations, i.e., for small changes of buoyancy.
This led us to :
- Painfully rediscover the Eötvös number (_Eo_, which we called _α_ in the image below).
- With dismay, find by a simple geometric argument that in order to get an _O(h²)_ convergence, _O(h⁴)_ convergence is needed on the interface location.
- For small Eötvös numbers, i.e., when the volume forces are small in comparison to the surface tension, it is extremely difficult to find a stable numerical scheme.
- Conclude that using a vorticity based model and the Boussinesq approximation is one of the worst cases to implement a multiphase flow simulation.
  
<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/collection.png" align="center" width="100%"></img>

# 2d flow fluid simulation : [Vortex](https://github.com/Tugdual-G/Vortex)

My first personal code project, which I implemented after getting a bit too interested in the vorticity equation. 
This program is old and may seem naive, however its implementation uses a less common description of the fluid, which leads to an extremely simple implementation.
Nevertheless, the scheme uses finite differences and an explicit time step, which is quite unstable.
<img src="https://raw.githubusercontent.com/Tugdual-G/Tugdual-G/main/images/medusevortex.png" width="33%"></img>
<img src="https://raw.githubusercontent.com/Tugdual-G/Vortex/main/vortex.gif" width="33%"></img>




