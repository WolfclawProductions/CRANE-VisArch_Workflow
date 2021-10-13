---
Title: A Workflow for Visualizing Archeological Data
tags: #crane #NRC 
type: Zettel Note
project: CRANE
---
[[Noah Chapman]]
Date: 2021-09-30

# A Workflow for Visualizing Archeological Data
This is intended to be a living document as I refine this process

I was asked to find a workflow for bringing published archaeological data into _TwinMotion_, an architectural visualization program published by Epic Games. Using Data found at [The Pompeii Mapping Project](https://digitalhumanities.umass.edu/pbmp/?page_id=273). 

## Basemap and GIS Data
[Pompeii Basemap]![[ArcGIS_Pompeii.PNG]]

I pulled a number of layers from the Pompeii Mapping Project and created a map that includes the Architectures, Buildings, Topography, and Streets, as well as a basic satellite basemap (**Monte_Mario_Italy_2** projection for those trying to replicate). 

## 3D Creation
### Supplemental Document:  [[VisArch Supplement_Blender GIS]]

[Blender Whitebox]![[BlenderGIS_Pompeii.PNG]]

After exporting the required mapping layers I took them into Blender, a popular and open-source 3D engine. Using the tools provided by [Blender GIS](https://github.com/domlysz/BlenderGIS), I first created a plane and projected the correct topography into 3D space, so the hills and elevation of the site should be relatively accurate. Next, I imported my ArcGIS layers into Blender, hiding the ones I didn't need for the moment. I kept the streets and buildings. Since the layers only import as simple lines, I extruded the points into a raised street map, imbedding the geometry into the plane. This creates a sense of buildings and streets interacting with the topography. 

## Twinmotion/Unreal Engine 
[Twinmotion Whitebox]![[TwinMotion_Pompeii.png]]

Exporting to TwinMotion was extremely simple, the Blender file was exported to .fbx format and imported directly into TwinMotion. This unlocks some really powerful lighting and visualization options, but another feature is that TwinMotion projects are compatable with Unreal Engine, allowing actual interactive experiences to be created with this data. 


### Next Steps
- Improved fidelity of basemaps
- Inclusion of 3D Models
- Textures
- Export to Unreal Engine




