# Calculate Ricci Curvature Tensors from Spacetime Metrics

# Files:
The |*Metric2Ricci.mlx*| code contains the function that does the computations 
using the MATLAB® Symbolic Math Toolbox™. 

The |*ExamplesOfMetrics.mlx*| code describes and sets up some examples of 
metric tensors and spacetime metrics.

# Purpose:
The primary purpose of this code is to assist academics in solving Einstein's 
field equations:

$$R_{\mu\nu} - \frac{1}{2} R g_{\mu\nu} = \frac{8\pi G}{c^4} T_{\mu\nu}$$

or

$$R_{\mu\nu} - \frac{1}{2} R g_{\mu\nu} + \Lambda g_{\mu\nu} = \frac{8\pi 
G}{c^4} T_{\mu\nu}$$

This can be a cumbersome task if done by hand. This code allows the user to 
input a spacetime metric or metric tensor of their own design and output the 
Christoffel symbols, Ricci tensor and Ricci scalar. They can then, for example, 
test if the metric is a valid solution to Einstein's field equations.
Details:
Einstein’s Theory of General Relativity describes how matter and energy curve/deform 
spacetime, giving rise to what we observe as gravitational forces. To get the 
magnitude of a vector $x$ in euclidean space, you take the dot product $x_\mu 
x^\mu$. If the space becomes curved, we need to describe that curvature with 
a metric $g$, and the dot product comes $g_{\mu\nu}x^\mu x^\nu$.

If we want to see if a given metric is a solution to the Einstein field equations, 
we compute the Einstein tensor. The Einstein tensor $G_{\mu\nu}$ describes the 
curvature of spacetime in how it relates to the presence of mass and energy 
described in the stress-energy tensor $T_{\mu\nu}$.

$$G_{\mu\nu} = \frac{8\pi G}{c^4} T_{\mu\nu}$$

The Einstein tensor itself is composed of the Ricci curvature tensor $R_{\mu\nu}$ 
and Ricci scalar $R$ and spacetime metric $g_{\mu\nu}$.

$$G_{\mu\nu} = R_{\mu\nu} - \frac{1}{2} R g_{\mu\nu}$$

The Ricci curvature tensor and Ricci scalar are both composed of Christoffel 
symbols $\Gamma^\beta_{\mu\nu}$, which are derived from the spacetime metric:

$$\Gamma^\beta_{\mu\nu} = \frac{1}{2} g^{\beta\alpha} (g_{\alpha\mu,\nu} + 
g_{\alpha\nu,\mu} - g_{\mu\nu,\alpha})$$

The comma signifies a partial derivative: $\frac{\partial g_{\alpha\beta}}{\partial 
x^\mu} = g_{\alpha\beta,\mu}$

The Christoffel symbols play an explicit role in the geodesic equation:

$$\frac{d^2 x^\beta}{ds^2} + \Gamma^\beta_{\mu\nu} \frac{d x^\mu}{ds} \frac{d 
x^\nu}{ds}$$

The Ricci curvature tensor and scalar can then be described in terms of the 
Christoffel symbols and spacetime metric:

$$R_{\alpha\beta} = \partial_\rho \Gamma^\rho_{\beta\alpha} - \partial_\beta 
\Gamma^\rho_{\rho\alpha} + \Gamma^\rho_{\rho\lambda} \Gamma^\lambda_{\beta\alpha} - \Gamma^\rho_{\beta\lambda} \Gamma^\lambda_{\rho\alpha}$$

$$R = g^{\alpha\beta}R_{\alpha\beta}$$


Matthew E Chasco

Mathworks
