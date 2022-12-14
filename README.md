# Summer Camp 2022
This is the summer camp project for [Appearance Inspection Algorithm Contest 2022](http://alcon.itlab.org/detail/).

## Task Summary
  - Objective: Detect, track and count swimming fishes in the water using provided videos
  - Target: Swimming fish in the tank
  - Grade Items: Accuracy and processing time of counting fish

*Note: There are five types of fish. They are Medaka, Kingfish (black), Small gold (red), Small gold (black) and Eyeball.*



# How to solve the problem
First, detect the fish, then track, and finally classify them all. </br></br>
![](image/1.jpg)</br></br>
1. Fish Detection: Use YOLOv5 to detect the fish, however, sometimes the bubbles are detected as fish. Therefore, counting all the bbox numbers and the most frequent number is the number of fish. </br></br>
![](image/2.jpg)</br></br>
2. Dataset Expansion: Expanding the complexity of the dataset can increase the accuracy of fish counting. 
   - For occlusion </br>
      - Use a fractured tree to simulate the seaweed, whereas the bubbles’ size, angle, and color vary from time to time as well. </br></br>
  ![](image/3.jpg)</br></br>
      - Add bubbles and seaweed to the images. </br></br>
  ![](image/5.jpg )</br></br>
   - For increasing numbers of images </br>
      - Download images from Google and change the color of the fish. </br></br>
  ![](image/4.jpg) </br></br>
3. Tracking: Apply StrongSORT to the program to separate each case. 
4. Classification: Deep Metric Learning 


