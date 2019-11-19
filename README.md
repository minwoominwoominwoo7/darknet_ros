## Description
I forked below git link. and I modified code.  
https://github.com/Affonso-Gui/darknet_ros.git  

## How to download this git link.    
git clone --recursive https://github.com/Affonso-Gui/darknet_ros.git 


## Modified Point.  
1. I modified BoundingBox.msg to add X, Y, Z.  
   X is center x value of detected object.   
   Y is center y value of detected object.   
   Z is center depth value of detected object by D435.   
2. Added use_platform option to run Gazebo.  
3. Only wine glass and cup Object can be published as BoundingBox.msg.   
4. Also changed label image that publishes only wine glass and cup objects to JSK pacakges.  
5. Reduced label image area for publishing to JSK pacakges to reduce depth erro  

## Tip  
If you want to remove the debug log from the darknet source, modify as below.  
```bash
darknet_ros/darknet/src/image.c
printf("%s: %.0f%%\n", names[j], dets[i].prob[j]*100);
-> //printf("%s: %.0f%%\n", names[j], dets[i].prob[j]*100);
```
