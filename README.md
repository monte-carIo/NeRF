# NeRF
[NeRF](https://arxiv.org/pdf/2003.08934v2.pdf) is a novel approach for synthesizing novel views of a scene given only a sparse set of input images. It represents a scene as a continuous 3D function that models the radiance (color and intensity of light) at any point in space. This is in contrast to traditional methods that often rely on discrete 3D representations or point clouds.

Step to render from a particular viewpoint:

1. march camera rays through the scene to generate a sampled set of 3D points.
2. use those points and their corresponding 2D viewing directions as input to the neural network to produce an output set of colors and densities.
3. use classical volume rendering techniques to accumulate those colors and densities into a 2D image.
