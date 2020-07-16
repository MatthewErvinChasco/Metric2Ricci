# Calculate Ricci Curvature Tensors from Spacetime Metrics

# Files:
The *Metric2Ricci.mlx* code contains the function that does the computations using the MATLAB® Symbolic Math Toolbox™. 

The *ExamplesOfMetrics.mlx* code describes and sets up some examples of metric tensors and spacetime metrics.

# Purpose:
The primary purpose of this code is to assist academics in solving Einstein's field equations:

![equation](https://latex.codecogs.com/gif.latex?R_%7B%5Cmu%5Cnu%7D%20-%20%5Cfrac%7B1%7D%7B2%7D%20R%20g_%7B%5Cmu%5Cnu%7D%20&plus;%20%5CLambda%20g_%7B%5Cmu%5Cnu%7D%20%3D%20%5Cfrac%7B8%5Cpi%20G%7D%7Bc%5E4%7D%20T_%7B%5Cmu%5Cnu%7D)

This can be a cumbersome task if done by hand. This code allows the user to input a spacetime metric or metric tensor of their own design and output the Christoffel symbols, Ricci tensor and Ricci scalar. They can then, for example, test if the metric is a valid solution to Einstein's field equations.

Matthew E Chasco

Mathworks



# Details:
Einstein’s Theory of General Relativity describes how matter and energy curve spacetime, giving rise to what we observe as gravitational forces. The curvature of spacetime can be described in a matrix known as a metric tensor ![equation](https://latex.codecogs.com/gif.latex?g_%7B%5Cmu%5Cnu%7D). If we want evaluate whether or not a given metric is a solution to the Einstein field equations, we compute the Einstein tensor. The Einstein tensor ![equation](https://latex.codecogs.com/gif.latex?G_%7B%5Cmu%5Cnu%7D) describes the curvature of spacetime in how it relates to the presence of mass and energy described in the stress-energy tensor ![equation](https://latex.codecogs.com/gif.latex?T_%7B%5Cmu%5Cnu%7D).

![equation](https://latex.codecogs.com/gif.latex?G_%7B%5Cmu%5Cnu%7D%20%3D%20%5Cfrac%7B8%5Cpi%20G%7D%7Bc%5E4%7D%20T_%7B%5Cmu%5Cnu%7D)

The Einstein tensor itself is composed of the Ricci curvature tensor ![equation](https://latex.codecogs.com/gif.latex?R_%7B%5Cmu%5Cnu%7D)
and Ricci scalar ![equation](https://latex.codecogs.com/gif.latex?R) and spacetime metric ![equation](https://latex.codecogs.com/gif.latex?g_%7B%5Cmu%5Cnu%7D).

![equation](https://latex.codecogs.com/gif.latex?G_%7B%5Cmu%5Cnu%7D%20%3D%20R_%7B%5Cmu%5Cnu%7D%20-%20%5Cfrac%7B1%7D%7B2%7D%20R%20g_%7B%5Cmu%5Cnu%7D)

The Ricci curvature tensor and Ricci scalar are both composed of Christoffel 
symbols ![equation](https://latex.codecogs.com/gif.latex?%5CGamma%5E%5Cbeta_%7B%5Cmu%5Cnu%7D), which are derived from the spacetime metric:

![equation](https://latex.codecogs.com/gif.latex?%5CGamma%5E%5Cbeta_%7B%5Cmu%5Cnu%7D%20%3D%20%5Cfrac%7B1%7D%7B2%7D%20g%5E%7B%5Cbeta%5Calpha%7D%20%28g_%7B%5Calpha%5Cmu%2C%5Cnu%7D%20&plus;%20g_%7B%5Calpha%5Cnu%2C%5Cmu%7D%20-%20g_%7B%5Cmu%5Cnu%2C%5Calpha%7D%29)

The comma signifies a partial derivative: ![equation](https://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cpartial%20g_%7B%5Calpha%5Cbeta%7D%7D%7B%5Cpartial%20x%5E%5Cmu%7D%20%3D%20g_%7B%5Calpha%5Cbeta%2C%5Cmu%7D)

The Christoffel symbols play an explicit role in the geodesic equation:

![equation](https://latex.codecogs.com/gif.latex?%5Cfrac%7Bd%5E2%20x%5E%5Cbeta%7D%7Bds%5E2%7D%20&plus;%20%5CGamma%5E%5Cbeta_%7B%5Cmu%5Cnu%7D%20%5Cfrac%7Bd%20x%5E%5Cmu%7D%7Bds%7D%20%5Cfrac%7Bd%20x%5E%5Cnu%7D%7Bds%7D) 

The Ricci curvature tensor and scalar can then be described in terms of the Christoffel symbols and spacetime metric:

![equation](https://latex.codecogs.com/gif.latex?R_%7B%5Calpha%5Cbeta%7D%20%3D%20%5Cpartial_%5Crho%20%5CGamma%5E%5Crho_%7B%5Cbeta%5Calpha%7D%20-%20%5Cpartial_%5Cbeta%20%5CGamma%5E%5Crho_%7B%5Crho%5Calpha%7D%20&plus;%20%5CGamma%5E%5Crho_%7B%5Crho%5Clambda%7D%20%5CGamma%5E%5Clambda_%7B%5Cbeta%5Calpha%7D%20-%20%5CGamma%5E%5Crho_%7B%5Cbeta%5Clambda%7D%20%5CGamma%5E%5Clambda_%7B%5Crho%5Calpha%7D)

![equation](https://latex.codecogs.com/gif.latex?R%20%3D%20g%5E%7B%5Calpha%5Cbeta%7DR_%7B%5Calpha%5Cbeta%7D)
