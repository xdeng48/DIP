Unfaulting seismic images
==========================
Our project focused on unfaulting seismic image using our improved Canny edge detection algorithm and new approach to eliminate the fault in those images. <br/>

Getting started
------------------
Please get these prerequisites prepared before running our samples.<br/>

### Prerequisites
* MATLAB R2016a
* Seismic Images

Running the tests
------------------
By running drawing.m and following instructions shown in user interface, all results in our paper could be obtained. Here are some details about each part of our project.  

### Creating User Interface
Firstly, user need import testing image, change the directory in corresponding part of code. See following examples:<br>
* Mac OS<br>
  folder = '/Users/dengxuanliang/Desktop/6258project/';<br>
  baseFileName = '2.jpg';<br>
* Win OS<br>
folder = 'D:\document\GTech\ECE 6258\Project\GUI\images';<br>
baseFileName = '2.jpg';<br>

After changing directory and click run, the GUI will pop up and user can draw the line by his/her intuition. If user thinks the line about fault is not good enough, he/she should close the window and draw again by running this program<br>

### Running Improved Canny Edge Detection
Secondly, ImprovedCanny function wrapped in drawing.m will be called to detect edges in image after user has drawn the line.<br>

(1) Usage: 
* [Canny, e] = ImprovedCanny(I, method)

(2) Functionality:
* Dectect edges in seismic images

(3) Input:<br>
* I: Gray image<br>
* method: 'rich' - The image contains lots of edge information, 'weak' - The image contains little edge information<br>  

(4) Output:<br>
* Canny: Output image containing only edges<br>
* e: noise of original image<br>

### Faulted Image Reconstruction
Thirdly, this program will continues its work after obtaining canny edge image. Use both edge image and fault line drawn by user, it will start reconstruction step and stops when it finds the best matching points.



  

