# Summer Camp 2022
This is the summer camp project for [Appearance Inspection Algorithm Contest 2022](http://alcon.itlab.org/detail/).

## Task Summary
  - Objective: Detect, track and count swimming fishes in the water using provided videos
  - Target: Swimming fish in the tank
  - Grade Items: Accuracy and processing time of counting fish
   <p>
   Note: There are five types of fish. They are Medaka, Kingfish (black), Small gold (red), Small gold (black) and Eyeball.




# How to solve the problem
First, detect the fish, then track, and finally classify them all. 
![](image/1.jpg)
1. Fish Detection: Use YOLOv5 to detect the fish, however, sometimes the bubbles are detected as fish. Therefore, counting all the bbox numbers and the most frequent number is the number of fish.
![](image/2.jpg)
2. Dataset Expansion: Expanding the complexity of the dataset can increase the accuracy of fish counting. 
 - For occlusion   
     Use a fractured tree to simulate the seaweed, whereas the bubbles’ size, angle, and color vary from time to time as well. 
![](image/3.jpg)
     <p>
     Add bubbles and seaweed to the images. 
![](image/5.jpg)
 - For increasing numbers of images   
     Download images from Google and change the color of the fish.
![](image/4.jpg)     
3. Tracking: Apply StrongSORT to the program to separate each case. 
4. Classification: Deep Metric Learning 


# Usage

1. Colon this project

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
