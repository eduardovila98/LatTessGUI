# LatTess User Guide

## Introduction
![Overall Screenshot](/docs/Screenshots/Overall.png)

## Tab Group
### Dimensions tab
<p align="center">
  <img src="/docs/Screenshots/DimTab.png" height="400"><br/>
</p>

1. In the first panel, the unit cell edge length is chosen. It should be a numeric value in mm.
2. Next, chose amongst **Low**, **Intermediate** or **High** resolution. This has a direct impact on the generation time.
3. To fully define the domain, information about the box is required. The user can either choose how many unit cells should be tessellated along each dimension, or the desired box dimensions - as multiples of the unit cell edge length.

Finally the **Confirm** button should be pressed

### Latticing Tab
<p align="center">
  <img src="/docs/Screenshots/LatTab.png" height="400"><br/>
</p>

High densities (more than ~0.4) lead to long times for FEA. Therefore, there is an option for either **Quick** or **Detailed** Analysis.  
The user should choose one of the three Latticing Strategies:
1. **Uniform** - this uses the same volume fraction throughout the box.
2. **Scalled** - Using values for density in the eight vertices, interpolation is done.
3. **Graded** - Allows for the use of a custom density map.

### Advanced Tab
<p align="center">
  <img src="/docs/Screenshots/AdvTab.png" height="400"><br/>
</p>

Here is where Advanced features can be added:
1. **Hierarchical** - allows for the use of different-sized unit cells, the scalling factor is decided in the **Regions** Tab.
2. **Morphing** - allows for the use of different unit cell types, as long as they belong to the same family (M, N or S). Unit cell type is decided in the **Regions** Tab.
3. **Hierarchical & Morphing** - enables both advanced features simultaneously.

## Live Preview
![Live Preview](/docs/Screenshots/Preview.png)  
A constantly refreshing 3D plot is used to represent the tesselation domain. Can be manually refreshed using the **Refresh** button.
When in the **Latticing** Tab, it displays where the 8 nodes are. When in the **Regions** Tab, each numbered region is displayed.
