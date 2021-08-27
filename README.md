# Blob Detection with a Magnetic Pendulum Summary

This project using blob the detection to track the trajectory of a pendulum (a magnet swinging on a string) under the influence of a configuration of magnets under its base. 

CAD designed and printed by my brother, Alex

More details about how the code works are provided in the code cells

I ran in Google Colab but one could also run it in Pycharm given the right libraries installed.

# Jump to

[Background and Purpose](#background/purpose)

[Equipment](#equipment-required)

[Procedure](#procedure)

# Background/Purpose

The purpose of this experiment is to see how magnetic fields in certain places influence the motion of a pendulum. To do this, we utilized blob detection code to detect the pendulum moving and then some code using matplotlib to graph the motion of the pendulum and find the regression (more detail in the procedure section). I also utilized a 3D printed stand to swing the magnet-string combo which will function as our pendulum, and also having spaces covered by a layer to house magnets. With this blob detection, you will need to know how to utilize RGB values. 

# Equipment Required

- A 3D-printed stand for pendulum and housing magnets (the one that I used is black, preferably the color should have an extremely low R, G, or B value). The CAD for it (in .stl form, made by my brother Alex) is available in this folder.  
- Magnets (small ones that could fit into your 3D-printed stand)
- String (preferably the same color as your stand)
- A phone or camera to take slowed down video
- Non-magnetic polish to color the magnets (preferably a color with an extremely high or extremely low R, G, or B value, depending on the color of the stand that you printed. For example, if the color of the stand you printed is pure green, pure red polish would be a good idea because it has an extremely high R value as opposed to pure green’s R value of 0)
- Random objects with the same color as the stand you printed big enough to fill up a background of a video.

# Procedure

1. Assemble your pendulum as follows:
 - Take your string and roll it around the part of the stand that is less thick than the other parts until the string can’t touch the bottom of the stand and then some.
 - Color your magnet with the polish of your choice.
 - Attach the magnet to your string (I did this by glue, but you can do it other ways). 
 - Attach the cover to the base so the pendulum stays stable. Do not add any magnets there yet.
2. Set up the background for the video you are going to take. Make sure that you have objects of all the same color covering the entire background of the video you are going to take. Make sure lighting is optimal. 
3. Set your magnet at the height of the stand to the direction that the string unrolls in, then start recording your video in slow-motion as soon as you drop the magnet. Record for 10-15 seconds.
4. Now add magnets in some of the spots of the pendulum stand and repeat Step 3. The number of magnets and the spots you want the magnets to be placed is something you should play with, but in the Data section it’ll show the amount of magnets and the spots of the magnets on the magnet base. You can test how many different combinations as you’d like, but for my sake, I tested 5 different combinations.
5. Now, time to use blob detection code to get the magnet’s x and y position for each frame of the video using this google colab code (make sure to import your video into google colab runtime). Your code should look something like the code found in this repository, or at least work the same way.
6. Now, with your detected blob and its coordinates (and the frames where the blob has those coordinates), you should be able to make all the graphs with that data you could possibly wish for! I have provided some sample code for graphs (with curve fits) in this Github folder. I have also provided some sample data in the code as well. 

