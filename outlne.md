# objectives

## inputs
- inspection data
	- point clouds
	- probability functions?
- model data
	- step files / breps
	- mesh files?
- tolerance data
	- proprietary?
	- is there a standard?
	- equivalent to light field?

## process

- do simple rotation and translation calcs on inspection data
	- rotations and translations are easy
	- find amount to rotate and translate by trickier. using best fit (least squares) trivial but technically (to the ASME Y14.5 standard) incorrect
	- automatic and manual outlier rejection of inspection data of irrelevant/non-mating surfaces
	- best fit/only highest points algorithms for DATUM simulators and GDNT position largest mating part

- have easy and intuitive UI for rotations and translations

- create tolerance data from step files and a traditional drawing
- be able to save tolerance data

- compare inspection data and tolerance data and print results in pleasing and easy to understand way

# outputs

- embedded save: zip file of all inspection data (e.g. for multiple parts) and model and tolerance data, and cached results and statistical analysis
- lightweight save: model and tolerance data, and cached results and statistical analysis

- inspection results, and formatted output of inspection results


----------

# how do section

## shapes

### shape primitives
0d -
- point
1d -
- line
- curve
2d -
- circle
- slot
- plane
- square
3d -
- cylinder
- sphere
- taper
- box

### shapes, conveniences
- chamfer
- screwform

### shape representations
- point cloud
- BREP
- point cloud <> BREP surf association
- poly meshes
	- stl
	- .obj

### tolerance zones
- gdnt
	- size
		- thickness
		- diameter
	- form
		- radius
	- location
	- complex
	- runout
- simple tolerancings
	- linear tolerance
	- circular
		- diametral tolerance
		- radial
		- contro/lled radius
	- sphereical