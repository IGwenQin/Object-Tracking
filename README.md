# Summer Camp 2022
This is the summer camp project for [Appearance Inspection Algorithm Contest 2022](http://alcon.itlab.org/detail/).

## Task Summary
- Detect, track and count swimming fishes in the water. 
## Object
- Swimming fish in the tank.
## Grade Items
- Accuracy and processing time of counting fish
## Program Overview
-There are five types of fish.
1. Fish number 1: Medaka
2. Fish number 2: Kingfish (black)
3. Fish number 3: Small gold (red)
4. Fish number 4: Small gold (black)
5. Fish number 5: Eyeball

# Installation
Clone this project and open with Unity.


# Sample
1. Open Assets/Sample/SampleScene.unity
2. Click "Render" botton in Assets/Sample/SampleCylinder.asset (wait for several seconds)
3. Images will be generated in output/


# Usage
## Generation of custom cylinder
1. Right click on Unity and select Create/CylinderData

2. Set parameters for generation of cylinder
    - **material**  
      the material of cylinder
    - **circle resolution**  
      the number of vertices of circle meshes
    - **height resolution**  
      the number of vertices of height meshes
    - **spatial resolution** [m/vert]  
      the length per one vertex
    - **smooth texture**  
      refine uv-mesh in connection of vertices
    - **sommth normal**  
      refine normal vector in connection of vertices
    - **generate zenith**  
      if true, generate zenith (top of cylinder)

<p></p>

3. Click "Save" and "Generate" botton to generate cylinder object  
  Note that: Game object in scene and asset correspond to each other. Therefore, if you want to create the other, create new CylinderData.

4. If parameters change, click "Update" botton

## Generation of custom camera arrangement
1. Right click on Unity and select Create/CylinderCameraData

2. Set parameters for camera arrangement
    - **cylinder data**  
      target cylinder data asset for shooting
    - **position offset** [m]  
      the offset of camera arrangement (0 m means same height with zenith)
    - **sampling resolution** [/s]  
      shooting resolution per second (frame per second)
    - **camera velocity** [m/s]  
      the falling velocity of camera
    - **camera rotation velocity** [euler/s]  
      the rotation velocity of camera (euler angle)
    - **render size**  
      output image size
    - **render path**  
      output images path

<p></p>

3. Click "Save" and "Generate" botton to generate camera objects  
  Note that: Semilar to cylinder, game object in scene and asset correspond to each other. Therefore, if you want to create the other, create new CylinderCameraData.

4. If parameters change, click "Update" botton

5. Click "Render" botton to shoot images  
  It may be several seconds. The output images will be generated in render path.


# Author
- Yuki Sakamura
- sakamura.yuki@image.iit.tsukuba.ac.jp
- Computer vision and image media lab.
