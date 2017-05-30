## Project: Search and Sample Return

---

**The goals / steps of this project are the following:**  

### Notebook Analysis
- In the provided Jupyter Notebook I modified ``color_thresh`` function to work with two color thresholds - above threshold and below threshold.
- Using GIMP I picked up color thresholds for yellow rocks - (110, 115, 0) and (250, 250, 100)
![alt text][image3]
- Here is transformed threshed calibration images for terrain, obstacles and rocks 
![alt text][image1]
- Modified the `process_image()` function with the appropriate image processing steps (perspective transform, color threshold etc.) to get from raw images to a map.
- The output video processed by `moviepy` on the saved dataset with the `process_image()` function:
[![Watch the video](./calibration_images/example_rock1.jpg)](./output/test_mapping.mp4)

### Autonomous Navigation and Mapping
* I changed the `perception_step()` function within the `perception.py` script with the appropriate image processing functions to create a map and update `Rover()` data (similar to what you did with `process_image()` in the notebook).    
* Launched in autonomous mode my rover mapped 60% of the environment with 60% fidelity. And also found three rock samples.
![alt text][image2]

### Problems 
* I was unable to run Rover simulator on Ubuntu 16.04 so i had to switch to the MacOS
* Due to the OS localization (I'm in Europe) some functions from the Notebook and from the supporting_functions.py were produce errors. 

[//]: # (Image References)
[image1]: ./output/warped_threshed.jpg
[image2]: ./output/autonomous.png
[image3]: ./calibration_images/example_rock1.jpg 

