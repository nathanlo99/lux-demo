# Lox

Lox (latin for light) started out as the final project for the computer graphics course (CS488) at the University of Waterloo. After adding an almost unnecessary number of features and optimizations, it has become one of my proudest projects. Unfortunately though, since the source code contains proprietary source code owned by the university, I am not allowed to share the source code, but figured it would be nice to outline some of the awesome things it can do!

## First things first: show me the images!

The following two images demonstrate almost every feature present in my raytracer. 

The first depicts a famous Go game: the 4th game between AlphaGo and Lee Sedol, with the famous "Divine" 78th move by White highlighted in yellow. It also depicts a fun mate in 10+ played between me and one of my friends. This demonstrates texture loading, mesh loading, reflective and refractive objects, as well as soft shadows.

![sample 2](https://user-images.githubusercontent.com/12538060/115157288-7e358380-a056-11eb-9a2d-5331eab29dfd.png)

The second image depicts a glass queen along with a reflective gold king, demonstrating the raytracer's ability to handle reflective surfaces as well as refractive surfaces efficiently with detailed and large meshes.

![glass-queen](https://user-images.githubusercontent.com/12538060/115157292-81c90a80-a056-11eb-9e14-e8373a324c76.png)

## Features:

My raytracer implements the following features, presented roughly in order of complexity:

- Support for basic geometric primitives (Spheres, Cubes, Planes)
- Importing specifications of scenes with a Lua script (the framework for which was provided in the original assignment)
- Reflective and matte surfaces
- Arbitrarily many light sources and soft shadows
- Anti-aliasing with uniform multisampling
- Phong shading
- Glossy surfaces
- Support for importing 3d models as meshes (.obj files)
- Texture maps and bump maps
- Collision optimization with efficient KD-trees
- Refractive surfaces, keeping track of the index of refraction of the current material
- Constructive Solid Geometry
- Per-pixel and per-chunk (8x8 or 16x16 tile) parallelization with OpenMP
