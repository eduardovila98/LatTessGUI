# LatTess User Guide

## Introduction
![Overall Screenshot](/docs/Screenshots/Overall.png)  
  
The user is supposed to go through the 6 Stages in the Tab group, having an updating representation in the **Live Preview**. Each stage should be confirmed using the **Confirm** button. At the last stage, the output is created.

## Tab Group
### Dimensions tab
<p align="center">
  <img src="/docs/Screenshots/DimTab.png" height="400"><br/>
</p>

1. In the first panel, the unit cell edge length is chosen. It should be a numeric value in mm.
2. Next, chose amongst **Low**, **Intermediate** or **High** resolution. This has a direct impact on the generation time.
3. To fully define the domain, information about the box is required. The user can either choose how many unit cells should be tessellated along each dimension, or the desired box dimensions - as multiples of the unit cell edge length.

Finally, the **Confirm** button should be pressed.

### Latticing Tab
<p align="center">
  <img src="/docs/Screenshots/LatTab.png" height="400"><br/>
</p>

High densities (more than ~0.4) lead to long times for FEA. Therefore, there is an option for either **Quick** or **Detailed** Analysis.  
The user should choose one of the three Latticing Strategies:
1. **Uniform** - This uses the same volume fraction throughout the box.
2. **Scalled** - Using values for density in the eight vertices, interpolation is done.
3. **Graded** - Allows for the use of a custom density map.

### Advanced Tab
<p align="center">
  <img src="/docs/Screenshots/AdvTab.png" height="400"><br/>
</p>

Here is where Advanced features can be added:
+ **Hierarchical** - allows for the use of different-sized unit cells, the scalling factor is decided in the **Regions** Tab.
+ **Morphing** - allows for the use of different unit cell types, as long as they belong to the same family (M, N or S). Unit cell type is decided in the **Regions** Tab.
+ **Hierarchical & Morphing** - enables both advanced features simultaneously.
The user should create planes, across which the change in unit cell (type and/or size) takes place. These are orthogonal and are created as follows:
1. Click on e.g. **Create XY** Plane
2. Input the position in the normal direction (in this case Z), from the origin, in mm.
3. Click **Confirm Plane**.
4. Planes can be removed altogether by clicking **Remove all Planes.**

### Unit Cells Tab
<p align="center">
  <img src="/docs/Screenshots/UnitTab.png" height="400"><br/>
</p>

From the three families - **Matrix surface**, **Network surface** and **Strut based** - unit cells can be selected for use. Only one unit cell should be chosen, except if **Morphing** is enabled, in which case, multiple (but from the same family) can be used.

### Regions Tab
<p align="center">
  <img src="/docs/Screenshots/RegTab.png" height="400"><br/>
</p>
For each region (more than one, if planes were created), the Hierarchical scalling factor and unit cell type have to be chosen from the drop-down lists.  

### Output Tab
<p align="center">
  <img src="/docs/Screenshots/OutTab.png" height="400"><br/>
</p> 
Here there is the option to either:

+ Make it a dogbone specimen;  
+ Instersect the domain with a custom shape (STL file).  

There are the following export options:

+ **STL file** with the a **Fractional Triangle Reduction** setting.  
+ **Images** or **Voxels**  
+ **FEA Mesh** that can be used for either Abaqus or Nastran.  
Finally, the **Confirm** button should be pressed.

## Live Preview
<p align="center">
  <img src="/docs/Screenshots/Preview.png" height="400"><br/>
</p> 

A constantly refreshing 3D plot is used to represent the tesselation domain. Can be manually refreshed using the **Refresh** button.
When in the **Latticing** Tab, it displays where the 8 nodes are. When in the **Regions** Tab, each numbered region is displayed.
