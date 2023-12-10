---
layout: post
title: MSFS Addon Development
subtitle: "Scenery addons of Shenzhen and Guangzhou developed for Microsoft Flight Simulator"
date: 2022-05-03
categories: virtual-environment
author: Yuxuan Huang
cover: /assets/img/posts/msfs/MSFS_Cover.jpg
tags: 
- MSFS SDK
- Blender
- Sketchup
- Modeling
- Game Dev
lang: en
---

## Shenzhen Scenery Addon

> This is a MSFS scenery pack I created for my hometown, Shenzhen, China. Over 150 landmarks of Futian, Luohu and Nanshan districts are included. [The addon](https://flightsim.to/file/21593/shenzhen-scenery-pack) is highly rated by the community and can be downloaded for free.

<iframe type="text/html" width="100%" height="385" src="https://www.youtube.com/embed/k7EGl7S8dJU" frameborder="0"></iframe>


### Procedure

#### Modeling
The building models used in this projects were either modeled from scratch in Blender, or modified based on 3D warehouse models.<br />
Exporting 3D warehouse models from Sketchup to Blender can be very tricky: 1) Exporting as fbx is usually the best practice, 2) Faces with incorrect normals need to be fixed before exporting, otherwise the textures will be missing, 3) If, for some reason the export produces incorrect results, e.g., with missing faces, export as dae instead, 4) Models exported as dae come with duplicated faces, i.e., overlapping faces with normals pointing in opposite directions, which takes time to fix. The scales are also incorrect, which need to be fixed.

#### Texturing
3D warehouse models are typically textured per face, while MSFS requires the model to be textured as a whole. This can be achieved in Blender by creating a copy of the model, UV unwrap it properly, and bake the diffuse color from the original model to the copy.<br />
MSFS uses PBR materials. I usually used the base texture as albedo, and edit the roughness, metalness, and emissive channels in Gimp based on the albedo.<br />
Texture sizes can be reduced without introducing visible artifacts by unwrapping the UVs cleverly. The trick is to the area based on the richness of the visual details rather than the size of the faces, i.e., assign larger area to faces with more details, e.g., texts, and they will look sharp even with a small texture size.

#### LODs
LODs were made to ensure a stable performance. The lowest LOD for 90% of the buildings have ~100 triangles.

#### Appearance Fine Tuning
One thing about this addon that really stands out is the night scenery, thanks to the manually drawn emissive textures and careful placement of lightsources to faithfully represent the LEDs billboards of the realworld counterparts of the skyscrapers and to create the atmosphere of what it feels like at night in the city of Shenzhen.

### Gallery
![Futian CBD](/assets/img/posts/msfs/MSFS_1.jpg)
![Central Park](/assets/img/posts/msfs/MSFS_2.jpg)
![Honghu Park](/assets/img/posts/msfs/MSFS_3.jpg)
![Window of the World](/assets/img/posts/msfs/MSFS_4.jpg)
![Futian CBD](/assets/img/posts/msfs/MSFS_5.jpg)
![Shennan East Road](/assets/img/posts/msfs/MSFS_6.jpg)
![Futian CBD](/assets/img/posts/msfs/MSFS_7.jpg)
![Panorama](/assets/img/posts/msfs/MSFS_8.jpg)

### Reference
Some building models in the Shenzhen addon was modified based on 3D warehouse models by 
[Brady Cloud](https://3dwarehouse.sketchup.com/by/3dmodelsbybradycloud), 
[Evan H.](https://3dwarehouse.sketchup.com/user/a8b38c02-f4b9-4cf1-b782-a13b89ae0b8d/Evan-H), 
[Simba Xu](https://3dwarehouse.sketchup.com/user/1738923191286251691521376/Simba-Xu), 
[David Z.](https://3dwarehouse.sketchup.com/user/1225501310576899873065371/David-Z), 
[xz H.](https://3dwarehouse.sketchup.com/user/0574991660866459293049083/xz-H), 
[Daniel G.](https://3dwarehouse.sketchup.com/user/0474550786855026421405040/Daniel-G), 
[SchulzeModelos](https://3dwarehouse.sketchup.com/user/1158072639310083925037396/SchulzeModelos), 
[Stefan L.](https://3dwarehouse.sketchup.com/user/0230731127377007708663868/Stefan-L),
[china build](https://3dwarehouse.sketchup.com/user/0992015006409495490445359/china-build), and 
[jendliang](https://3dwarehouse.sketchup.com/user/1654779381322096624516576/jendliang).


## Guangzhou Scenery Addon
> I also made a mini scenery pack for Guangzhou, China that includes 4 landmarks of the city. [The addon](https://flightsim.to/file/21685/guangzhou-scenery-pack) can also be downloaded for free.

### Reference
The building models in the Guangzhou addon was modified based on 3D warehouse models by 
[Filip Michalowski](https://3dwarehouse.sketchup.com/user/0973046409669036277820028/Filip-Michalowski),
[Sebastian S.](https://3dwarehouse.sketchup.com/user/0597843197407614654222928/Sebastian-S), and
[Alpha Virtual World](https://3dwarehouse.sketchup.com/user/1317421059891422302646981/Alpha-Virtual-World).
