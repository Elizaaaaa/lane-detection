# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps. 
1. Transfer the image into Canny image
2. Find the potential lines in Canny image
3. Disgard the lines that are (a)horizontal or (b) out of the interested zone
4. Group the lines base on its slope (>0 or <0)
5. Extrapolating the lines to make it have a pair of solid left-line and right-line
6. Averaging the current line with previous lines to make the prediction more stable

### 2. Identify potential shortcomings with your current pipeline

It will be better if I have more time to tune the hough line parameters.
For the Challenging video, I can see the canny image can detect left boundaries. But when it comes to Extrapolating and Averaging, the left line suddenly disappears. I suspect it relates to the hough line parameter not setup correctly.


### 3. Suggest possible improvements to your pipeline

As I described in the above section, the hough image parameters definatly needs more fine tuning.
